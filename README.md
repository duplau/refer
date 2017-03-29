### Fonctionnalités de normalisation de données

Je donne ici des échantillons (aussi représentatifs que possibles sans en montrer un trop grand nombre) des cas les plus intéressants / les moins triviaux de normalisation de différents types de données.

Dans chaque tableau montrant la sortie du code, j'ai mis vers la fin les résultats problématiques (normalisation incorrecte ou pas réalisée).

__Normalisation de dates__

TODO example md output

__Normalisation d'adresses postales__

C'est un exemple de type de données composite, donc on voit ici que la valeur de l'adresse complète est extraite et normalisée, mais aussi chacune de ses composantes (voie, code postal, commune, etc.) 

TODO example md output

__Normalisation de noms de personnes__

TODO example md output

__Normalisation de dates__

|Date|Champ de départ|
|-|-|
|19/8/2007|le 19 août 2007|
|2/1/1960|02JAN1960|
|31/8/1946|31/08/1946|
|19/3/1968|19/03/1968|
|1/1/2013|1er janvier 2013 |
|25/1/2012|le 25 janvier 2012|
|2/1/1960|02/01/1960|
|31/8/2014|31 août 2014|
|2/1/2017|02 janvier|
|2013|2013|
|21/12/2011|21 décembre 2011|
||en date du 31 août 2014, je crois|
|en l'an de grâce 2013|en l'an de grâce 2013|
||Du 21 décembre 2011, date de la mise en service |

__Reconnaissance et normalisation d'identifiants__

On voit ici des exemples de dénominations d'UMR utilisant une multitude de syntaxes diverses et variées.

|parentName dans HAL|Normalisation - Numéro UMR|
|-|-|
|EOST\, UMR CNRS-ULP 7516||
|Praxiling UMR 5267|5267|
|Discours\, textualité et production de sens \, praxiling \, recherche en domaine occitan,Praxiling UMR 5267|5267|
|Praxiling UMR 5267,EducTICE|5267|
|Praxiling UMR 5267|5267|
|3UMR728 INSERM Unité d'immuno-hématologie (UIH) and laboratoire d'hématologie\, Hôpital St-Louis\, AP-HP|728|
|UMR-CNRS 6599|6599|
|UMR 5600 Environnement Ville Société|5600|
|Bases\, Corpus\, Langage (UMR 6039)|6039|
|Agro-M/INRA/CNRS/UM2 UMR5004|5004|
|UMR 6600|6600|
|Laboratoire de Catalyse en Chimie Organique\, CNRS UMR 6503|6503|
|Institut de Chimie des Milieux et Matériaux de Poitiers,Laboratoire de Catalyse en Chimie Organique\, CNRS UMR 6503|6503|
|CEA-iRTSV-LBBSI\, UMR 5092 CNRS\, UJF|5092|
|Laboratoire de Botanique\, Phytochimie et Mycologie\, Faculté de Pharmacie\, CEFE UMR 5175\, CNRSUniversité de Montpellier - Université Paul-Valéry Montpellier – EPHE|5175|
|Université Paris Diderot - Paris 7,AP-HP Hôpital Bichat - Claude-Bernard (Paris),UMR 1123|1123|
|UMR 5600 Environnement Ville Société|5600|
|CREDA - Centre de Recherche Et de Documentation sur les Amériques - UMR 7227|7227|
|Université Nice Sophia Antipolis\, UMR CNRS 7248 - Orange Labs La Turbie|7248|
|CNRS : UMR7048,Sciences Po|7048|
|Campus CNRS\, UMR 5175|5175|
|UMR MA 101 ULP-ENGEES|101|

__Reconnaissance des acronymes__

Quand un grand nombre d'acronymes sont repérés dans les valeurs d'un champ, chaque représentation sous forme d'acronyme resp. sous forme étendue est extraite dans son propre champ (autrement dit, même en l'absence d'inférence de type, 1 colonne en entrée en produit 3 en sortie ; avec un type inféré on en obtient 4 ; avec un type composite encore plus.)

TODO example md output

__Expansion des acronymes, synonymes et autres variantes__

TODO example md output

