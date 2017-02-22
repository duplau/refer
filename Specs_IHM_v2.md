## Préambule

Ce mémo présente une suggestion d'interface pour notre projet de référencement. Il a peu à voir avec la première version que j'avais détaillée dans un autre document : d'une part il est plus concis afin de faciliter la compréhension, d'autre part il est aligné avec notre dernière discussion (le 20 février) dont sont sorties des specs assez différentes de la première itération.

## Stockage de données

Les données persistantes dans le système seront exclusivement :

1. Les référentiels système (i.e. les données propres au MESR ou venant d'une source externe mais maintenues et stockées dans notre équipe)
2. Les référentiels utilisateurs (i.e. celles fournies optionnellement dans les appels d'API)
3. Les données d'apprentissage (i.e. les choix de matching éventuellement fournis par l'utilisateur dans le mode interactif et utilisables par l'outil dedupe)
4. Les résultats de référencement (i.e. la sortie de notre système)

Noter que le stockage de 2, 3 et 4 est contingent à l'approbation de l'utilisateur.

## Fonctionnalités

Le système est utilisable en deux modes :
- Un mode API, c'est-à-dire par un appel à l'un des services web proposés en accès libre
- Un mode interactif, c'est-à-dire une interface graphique accessible par un navigateur web

Le mode interactif fournit les mêmes fonctionnalités que le mode API, ainsi que des fonctionnalités supplémentaires, à savoir celles qui nécessitent une interaction utilisateur (autrement dit une IHM) : en l'occurrence il s'agit uniquement de la phase d'apprentissage manuel.

Passons à la description de chaque fonctionnalité, que nous catégorisons en must-have et nice-to-have plutôt que d'introduire plusieurs versions du système :

### Fonctionnalités "must-have"

On a deux scénarios d'utilisation :
1. Associer un fichier source avec les référentiels internes : ce scénario prend en entrée un fichier source et des paramètres optionnels
2. Associer un fichier source avec un référentiel externe fourni en entrée: ce scénario prend en entrée un fichier source, un fichier de référence et des paramètres optionnels

Chacun de ces scénarios peut être invoqué en mode API ou en mode interactif. Dans chaque scénario, on a plusieurs phases :

* __Apprentissage manuel__ : seulement en mode interactif, réplique la phase d'apprentissage en ligne de commande de l'outil dedupe (on présente une paire de données à l'utilisateur qui répond par un choix ternaire identique / différent / incertain, puis on recommence, l'utilisateur pouvant interrompre cette phase à tout moment)
* __Paramétrage du référencement__ : soit en mode API (via un argument dans la requête envoyée) soit en mode interactif (via des composants graphiques de type sélection multiple et cases à cocher), en tout cas optionnel. Les paramètres disponibles sont :
    * _information de type ou nature d'une colonne_ : par exemple la colonne 3 est une adresse, ou la colonne 5 est un nom de structure
    * _information d'alignement entre colonnes_ : par exemple pour dire qu'une jointure entre la colonne 5 du fichier source et la colonne "Nom_chercheur" du référentiel fournit les associations souhaitées
    * _information sur le référentiel interne à utiliser dans le scénario 1_ : soit une mention générale à un domaine de référence (par exemple pour indiquer que les données sont relatives aux admissions post-bac) soit une mention plus spécifique (par exemple restreindre le référentiel des lycées aux lycées polyvalents à l'exclusion des lycées professionnels)
* __Référencement automatique__ : cette phase consiste essentiellement en la détermination des types de données source, normalisation, et association avec les données de référence.
* __Présentation des résultats__ : visuellement pour le mode interactif, et de façon synchrone ou asynchrone pour le mode API.

En sortie, quel que soit le scénario, le système produit comme résultats :
* le fichier référencé, qui est identique au fichier source mais avec des valeurs de colonnes supplémentaires pour indiquer les associations (donc on ne modifie ni supprime aucune valeur de colonne du fichier d'origine)
* une série de logs indiquant les normalisations et associations qui ont été réalisées, celles qui ont échoué (par exemple aucune association trouvée alors qu’on en attendait une, ou plusieurs trouvées pour une association avec contrainte d’unicité), ou un problème interne.

L'utilisation asynchrone permet de traiter les gros volumes de données et de gérer plus facilement les fichiers multiples. Par rapport à l'utilisation synchrone, deux requêtes supplémentaires sont disponibles :
- Une requête de « polling » indiquant le statut du traitement (en cours avec un indicateur de progression, achevée avec les informations pour
obtenir les résultats, ou en erreur avec des messages d’erreur)
- Une requête de téléchargement des résultats (si l’utilisateur ne souhaite pas les télécharger directement)

### Fonctionnalités "nice-to-have"

* Suggestions du système, par exemple restriction du domaine de référencement : ainsi dans le cas où toutes les données source correspondent à une institution de type laboratoire, il est inutile de faire tourner le processus sur l'ensemble de la base SIREN.

### Autres

__Charte d'utilisation__

Elle doit couvrir au moins :
- L'absence de garantie des résultats de référencement (par exemple taux de rappel et de précision inférieurs à 100%)
- L'approbation par l'utilisateur à la publication des données sur le web (tant celles fournies en entrée que les résultats en sortie du système)


