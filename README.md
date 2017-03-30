### Fonctionnalités de normalisation de données

Je donne ici des échantillons (aussi représentatifs que possibles sans en montrer un trop grand nombre) des cas les plus intéressants / les moins triviaux de normalisation de différents types de données.

Dans chaque tableau montrant la sortie du code, j'ai mis vers la fin les résultats problématiques (normalisation incorrecte ou pas réalisée).

__Inférence de type de données : Produits phytosanitaires__

[Exemple de résultats](https://github.com/duplau/refer/blob/master/eval/mention_licence.apb.resultats.md).

__Inférence de type de données : Mentions de choix APB__

[Exemple de résultats](https://github.com/duplau/refer/blob/master/eval/produit_phyto.acta.resultats.md).

__Normalisation d'adresses postales__

C'est un exemple de type de données composite, donc on voit ici que la valeur de l'adresse complète est extraite et normalisée, mais aussi chacune de ses composantes (voie, code postal, commune, etc.) 

|Colonne mystère 3|Entité Géo|Adresse|Commune|Code Postal|Voie|Pays|Région|Département|
|-|-|-|-|-|-|-|-|-|
|Museum National D'Histoire Naturelle 43 Rue Cuvier 75231 Paris Cedex 05|Museum National D'Histoire Naturelle 43 Rue Cuvier 75231 Paris Cedex 05|43rue cuvier75231paris cedex 05; 43 rue cuvier - 75231 - paris cedex 05|paris cedex 05|75231|rue cuvier; 43||||
|Mortain|Mortain|mortain|mortain||||||
|24 rue Saint Michel, 69007, Lyon|24 rue Saint Michel, 69007, Lyon|24 rue saint michel - 69007 - lyon; 24rue saint michel 69007 lyon|lyon|69007|24; rue saint michel; rue saint||||
|59 Avenue Lacassagne, 69003 Lyon|59 Avenue Lacassagne, 69003 Lyon|59avenue lacassagne 69003lyon; 59 avenue lacassagne - 69003 - lyon|lyon|69003|avenue lacassagne; 59||||
|IEA/IRD Université de Provence Case 58 - 3 place Victor HUGO - 13331 Marseille Cedex 3|IEA/IRD Université de Provence Case 58 - 3 place Victor HUGO - 13331 Marseille Cedex 3|place victor hugo 13331marseille cedex 3; place victor hugo - 13331 - marseille cedex 3|marseille cedex 3|13331|place victor hugo; place victor||||
|3, Route de Mende, 34199 Montpellier cedex 5|3, Route de Mende, 34199 Montpellier cedex 5|3 route de mende - cedex - 5; 3 route de mende cedex5|5|cedex|3; route de mende; route mende||||
|Université Paul-Valéry - Site de Saint-Charles - Route de Mende - 34 199 Montpellier Cedex 5|Université Paul-Valéry - Site de Saint-Charles - Route de Mende - 34 199 Montpellier Cedex 5|34 route de mende - 199 montpellier cedex - 5; route de mende 34199 montpellier cedex5|5|199 montpellier cedex|route de mende; route mende; 34||||
|Toulouse|Toulouse|toulouse; Toulouse|toulouse; TOULOUSE||||||
|121 boulevard du Danemark BP380 82003 Montauban Cedex|121 boulevard du Danemark BP380 82003 Montauban Cedex|bp380 boulevard du danemark - 82003 - montauban cedex; boulevard du danemarkbp38082003montauban cedex|montauban cedex|82003|bp380; boulevard du danemark||||
|Avenue François Mitterrand - BP 49 - F 17700 Surgères|Avenue François Mitterrand - BP 49 - F 17700 Surgères|17700; avenue francois 17700||17700|avenue francois||||
|La Nougerée, F-17770 Bercloux|La Nougerée, F-17770 Bercloux|bercloux|bercloux||||||
|23 rue Loess, 67034 Strasbourg|23 rue Loess, 67034 Strasbourg|23rue loess 67034strasbourg; 23 rue loess - 67034 - strasbourg|strasbourg|67034|rue loess; 23||||
|14 rue Kepler, 44240 La Chapelle-sur-Erdre|14 rue Kepler, 44240 La Chapelle-sur-Erdre|14rue kepler 44240lachapelle-sur-erdre; 14 rue kepler - 44240 - la - chapelle-sur-erdre|chapelle erdre; la|44240|rue kepler; 14|chapelle-sur-erdre|||
|Agropole, CS 45002, 86550 Mignaloux-Beauvoir, France|Agropole, CS 45002, 86550 Mignaloux-Beauvoir, France|cs 45002 - 86550 - mignaloux-beauvoir - france; cs 45002 86550mignaloux-beauvoir france|mignaloux beauvoir; mignaloux-beauvoir|86550|cs 45002|france|||
|46, rue d'Amsterdam|46, rue d'Amsterdam|46 rue d'amsterdam|||46; rue amsterdam; rue d'amsterdam||||
|7, rue de la Croix Martre, 91120 Palaiseau|7, rue de la Croix Martre, 91120 Palaiseau|7 rue de la croix martre 91120palaiseau; 7 rue de la croix martre - 91120 - palaiseau|palaiseau|91120|rue de la croix martre; rue croix; 7||||
|11-13 rue Joseph Caillé BP 30824 44008 NANTES Cedex 1|11-13 rue Joseph Caillé BP 30824 44008 NANTES Cedex 1|11-13 - 44008 - nantes cedex 1; 11-13rue joseph 44008nantes cedex 1|nantes cedex 1|44008|rue joseph; 11-13||||
|Université Paris 13, UFR de Santé, Médecine et Biologie Humaine, 74 rue Marcel Cachin, 93017 Bobigny Cedex.|Université Paris 13, UFR de Santé, Médecine et Biologie Humaine, 74 rue Marcel Cachin, 93017 Bobigny Cedex.|74rue marcel cachin 93017bobigny cedex.; 74 rue marcel cachin - 93017 - bobigny cedex.|bobigny cedex.|93017|74; rue marcel cachin; rue marcel||||
|UMR 6578 27 bd Jean Moulin 13385 MARSEILLE CEDEX 05|UMR 6578 27 bd Jean Moulin 13385 MARSEILLE CEDEX 05|27 bd jean moulin - 13385 - marseille cedex 05; 27bd jean moulin13385marseille cedex 05|marseille cedex 05|13385|27; bd jean moulin||||
|Avenue Agropolis TA A-104 / 01 34398 Montpellier Cedex 5|Avenue Agropolis TA A-104 / 01 34398 Montpellier Cedex 5|a-104 / 01 avenue agropolis ta - cedex - 5; avenue agropolis taa-104 / 01 cedex5|5|cedex|avenue agropolis ta; a-104 / 01; avenue agropolis||||
|40 bis rue Fabert, 75007 Paris|40 bis rue Fabert, 75007 Paris|40 bis rue fabert - 75007 - paris; 40 bisrue fabert 75007paris|paris|75007|rue fabert; bis rue; 40 bis||||
|200 Chemin des Ormeaux, 69578 LIMONEST|200 Chemin des Ormeaux, 69578 LIMONEST|200chemin des ormeaux 69578limonest; 200 chemin des ormeaux - 69578 - limonest|limonest|69578|200; chemin des ormeaux||||
|91190 Gif-sur-Yvette, France|91190 Gif-sur-Yvette, France|91190gif-sur-yvette france; 91190 - gif-sur-yvette - france|gif-sur-yvette; gif yvette|91190||france|||
|UFR de Chimie, Bâtiment B - UJF - BP 53 - 38041 Grenoble cedex 9|UFR de Chimie, Bâtiment B - UJF - BP 53 - 38041 Grenoble cedex 9|bp 53 38041grenoble cedex 9; bp 53 - 38041 - grenoble cedex 9|grenoble cedex 9|38041|bp 53||||
|UJF - Site Santé La Tronche - BP 170 - 38042 Grenoble Cedex 9|UJF - Site Santé La Tronche - BP 170 - 38042 Grenoble Cedex 9|170 38042grenoble cedex 9; 170 - 38042 - grenoble cedex 9|grenoble cedex 9|38042|170||||


__Normalisation de noms de personnes__

|Colonne mystère 1|Prénom|Nom|Nom de personne|
|-|-|-|-|
|Serge Linkès|Serge|Linkès|Serge|
|BAKHOUCHE Béatrice|Béatrice|BAKHOUCHE|BAKHOUCHE Béatrice|
|Charles, Loïc et Théré, Christine|Charles; Christine||Charles, Loïc et Théré, Christine|
|B. Grunberg [ed.],|B.|.||
|Christine Delory-Momberger|Christine|Delory-Momberger|Christine Delory-Momberger|
|Julien Garaud, Mikhail Volkov|Julien|Volkov; Garaud|Julien Garaud, Mikhail Volkov|
|CALLENS STEPHANE|STEPHANE|CALLENS|CALLENS STEPHANE|
|Saada Julie|Saada; Julie|Saada|Saada Julie|
|Claude Andrault-Schmitt|Claude|Andrault-Schmitt|Claude|
|Christian CHELEBOURG (editor)|Christian|CHELEBOURG (editor)|Christian|
|Xavier DESJARDINS|Xavier|DESJARDINS|Xavier DESJARDINS|

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
