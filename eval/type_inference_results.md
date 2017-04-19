
	Test : inférence de type
	Données : le fichier "crado" des établissements publics fournis par Yann
	Date : 19/04/2017

Comment lire ces logs du système :
* ils indiquent les résultats de l'inférence sur les en-têtes puis sur les valeurs
* les valeurs décimales entre parenthèses sont des probabilités agrégées par colonne
* les champs entourés de "++" sont des champs "augmentés" créés par le système, le but est de fournir des valeurs normalisées afin d'une part d'aider l'outil de déduplication, d'autre part et accessoirement comme enrichissement partiel des données, le tout en conservant les champs originaux. 

```
Likeliest type for ETABLISSEMENT header: Etablissement
Likeliest type for VILLE header: Ville
Likeliest type for UAI header: UAI
Likeliest type for COMPO header: None
Likeliest type for COM_CODE header: None
Sorted types for ETABLISSEMENT : Etablissement (42.15686274509804) 
Likeliest type for ETABLISSEMENT values: Etablissement
Sorted types for VILLE : Adresse (96.36678200692042) ; Commune (94.57900807381776) ; Structure de recherche (49.30795847750865) 
Likeliest type for VILLE values: Commune
Sorted types for UAI : UAI (95.73241061130335) 
Likeliest type for UAI values: UAI
Sorted types for COMPO : UAI (93.3679354094579) 
Likeliest type for COMPO values: UAI
Sorted types for COM_CODE : Code Postal (95.67474048442907) 
Likeliest type for COM_CODE values: Code Postal
Normalizing values for ETABLISSEMENT
Output fields for ETABLISSEMENT: ['++Etablissement++', 'ETABLISSEMENT']
Normalizing values for VILLE
Output fields for VILLE: ['Commune', 'VILLE']
Normalizing values for UAI
Output fields for UAI: ['++UAI++', 'UAI']
Normalizing values for COMPO
Output fields for COMPO: ['COMPO', '++UAI++']
Normalizing values for COM_CODE
Output fields for COM_CODE: ['++Code Postal++', 'COM_CODE', 'Code Postal']
```
