## Tests sur le jeu de données "Produits phyto"


__Résultats au 27/02/2017__, cette fois avec l'algo fuzzywuzzy sous-jacent à notre méthode de matching ad-hoc, mais toujours sans gérer explicitement les acronymes (donc encore un peu marge de manoeuvre, même si les acronymes sont difficiles à gérer sur ce jeu de données qui est riche en noms de produits courts et écrits en capitale :  ADAC, NICO, OPUS, ROXY, etc...) :

* 1224 questions au total
* 1130 questions avec un objectif
* 1047 réponses correctes

----

__Résultats au 21/02/2017__, après une légère amélioration du matching (mais sans changer pour l'algo fuzzywuzzy qui au vu des quelques tests produit une précision bien inférieure) :
* 1224 questions au total
* 1130 questions avec un objectif
* 1006 réponses correctes

----

__Résultats au 16/02/2017__

* 1224 questions au total
* 1130 questions avec un objectif
* 955 réponses correctes

Réponses incorrectes :

|Question|Objectif|Réponse 1|Réponse 2|Réponse 3|
|--------|--------|---------|---------|---------
|ADAK-STERCO|ADAC|STERCO|
|alphac|ALFAC|SUMI ALPHA|
|APROACH + marathon 1.2 l|APLOMB 450|MARATHON (ANCIEN)|
|arial|ARIANE|AXIAL|AXIAL PRATIC|AXIAL ONE|AXIAL|AXIAL PRATIC|AXIAL ONE|AXIAL|AXIAL PRATIC|AXIAL ONE|
|c3|C3SUN|COURTEX C3|
|C5|C5SUN|CYCOCEL C5 BASF|COURTEPAILLE C5|C5 FLEX|CYCOCEL C5 BASF|COURTEPAILLE C5|C5 FLEX|CYCOCEL C5 BASF|COURTEPAILLE C5|C5 FLEX|
|chlor mefon|CHLORMEFLASH|CHLORO 500|chlore|
|chlore mephon|CHLORMEFLASH|CHLORO 500|chlore|
|CHLORTO|chlortoluron|CHLORO 500|chlore|
|CONTEX|CORTES SP|CONNEX|
|DANAO|TANHAO|DYNAO|
|DIT QU'IL NE CONNAIT PAS LE NOM DU PRODUIT|NSP|CONTACT 500|
|ISO|isoproturon|ISO-STEF GT|
|LIXUS|UNIX|LEXUS NRJ|LEXUS|LEXUS XPE|LEXUS NRJ|LEXUS|LEXUS XPE|LEXUS NRJ|LEXUS|LEXUS XPE|
|ne connait pas le nom du produit|nsp|CONTACT 500|
|SITEL|SCITEC|SATEL|
|super metrine|cypermethrine|FENOVA SUPER|DUPLOSAN SUPER|CONDOR SUPER 5|FENOVA SUPER|DUPLOSAN SUPER|CONDOR SUPER 5|FENOVA SUPER|DUPLOSAN SUPER|CONDOR SUPER 5|
|TICOTOP|TYPY TOP|PICOTOP|

Zéro réponse :

|Question|Objectif|
|--------|--------|
|actmite|ARTEMIS|
|ACTIBO|ACTIROB B|
|actim|ACTIMUM|
|AKIRA|AKARI|
|ALCION|ALCYONE|
|alicon|ALCYONE|
|alidrio|ALLIE DUO SX|
|alie|ALLIE|
|ALIER|ALLIE|
|ASMINE|ARVEST|
|atribu|ATTRIBUT|
|AXALIA PRATIQUE|AXIAL PRATIC|
|axirob|ACTIROB B|
|azur|ASUR|
|baa|BAIA|
|baa|BAIA|
|BAUA|BAIA|
|BAYA|BAIA|
|baya e|BAIA E|
|bayard|BAIA|
|beaifixe|BOFIX|
|beaufils|BOFIX|
|BEL|BELL (BASF)|
|C 5|CYCOCEL C5 BASF|
|CALPUCO|KAPULCO|
|calysouffre|QUALISOUFRE|
|cart|KART|
|carte|KART|
|ccc 5|CYCOCEL C5 BASF|
|CEQUOCEL|CYCOCEL C5 BASF|
|cron|CERONE|
|CEROQUET|CHEROKEE|
|CHEROT|CHEROKEE|
|CHERROKY|CHEROKEE|
|chiroci|CHEROKEE|
|CHIROKI|CHEROKEE|
|chlormefon|CHLORMEFLASH|
|chloronil|chlorothalonil|
|chlortosonne|CHLORTOSUN|
|CHORTOLOURN|chlortoluron|
|CIBEL|CYBELE|
|cicocelle|CYCOCEL C5 BASF|
|cicosy|CYCOCEL C5 BASF|
|CINTEL|SATEL|
|cloroduron|chlortoluron|
|congondor|COMMODORE|
|CORTOFIN|CLORTOSINT|
|CYCLAB|CYCLADE|
|daa|BAIA|
|dfi|DEFI|
|DESI|DEFI|
|DESIF|DEFI|
|DRUIDE|DROID|
|DUBLEX|DUBLETT|
|dudomen|DOLMEN|
|ETANAO|TANHAO|
|eterest|ETHEVERSE|
|FAUBERY|FOSBURI|
|FAUBURY|FOSBURI|
|fespery|FOSBURI|
|FIDEAL|PHYDEAL|
|fidal|PHYDEAL|
|fly|FLIGHT|
|FURBBURY|FOSBURI|
|furi|FURY 10 EW|
|fytockel|CYCOCEL C5 BASF|
|GALOP|GALLUP SPECIAL|
|glibhoflash|GLYFOFLASH|
|GLIFOGANT|GLYPHOGAN|
|GLIFOSATE|glyphosate|
|GOAO|JOAO|
|HALLOWEEN|ALLOWIN|
|harlon|ARELON DISPERSION|
|harol|AROLLE STAR (BASF)|
|ifosbery|FOSBURI|
|INQUANTO|ACANTO|
|IPUT|INPUT|
|isofosbery|FOSBURI|
|JE NE L AI PAS MARQU|nsp|
|je ne sais pas|nsp|
|JOHA|JOAO|
|junction|JONXION|
|kasar|QUASAR|
|KAZAR|QUASAR|
|KERESTEL|KESTREL|
|lbrasta|NEBRASKA|
|lvacci|LEGACY DUO|
|magnlo|MAGNELLO|
|MANIELO|MAGNELLO|
|mdax|MEDAX|
|micine|MIX-IN|
|minera|MENARA|
|MISTIQUE|MYSTIC EW|
|mixcrin|MIX-IN|
|MIXIN|MIX-IN|
|mixine|MIX-IN|
|MIXING|MIX-IN|
|mixtine|MIX-IN|
|MODIF|MODDUS|
|MYXINE|MIX-IN|
|NGATY|LEGACY DUO|
|NICO|NIKOS|
|OBAN|OPEN|
|Ollen|ONNEL|
|onel|ONNEL|
|otelo|OTHELLO|
|ozaro|PROSARO|
|PACKGINACTION|ZEN ACTION|
|packmultiz|MULTIZZ|
|pbucure|TEBUCUR 250|
|proclosone|PROCHLOSUN|
|PROKLORANE|PROCHLOBAN|
|psychocelle|CYCOCEL C5 BASF|
|psycocelle|CYCOCEL C5 BASF|
|QAZAR|QUASAR|
|RAPHAL|RAFALE S|
|RUNDDOP|ROUNDUP|
|senorgue|SUNORG|
|sheroki|CHEROKEE|
|silouette L77|SILWET L 77|
|silouhette|SILWET L 77|
|SILWOTTE|SILWET L 77|
|siwlhouet|SILWET L 77|
|skowe|SKYWAY XPRO|
|SKYMLIN|SKAELIM|
|slexyti|FLEXITY|
|stand up|STANDUP 3C|
|starpaire|STARTER|
|Stigmate|STICMAN|
|SUPERMAITRINE|cypermethrine|
|surfmax|SURF 2000|
|swingolds|SWING GOLD|
|sycoles|CYCOCEL C5 BASF|
|TABLEAU|TABLO 700|
|tahnao|TANHAO|
|talbo|TABLO 700|
|tanaho|TANHAO|
|tzoruze|THESORUS|
|thefers|ETHEVERSE|
|TONTEL|CONSTEL|
|tortulion|chlortoluron|
|TOUFIX|BOFIX|
|trasco|TRAXOS|
|TRASOFT|TRAXOS|
|tronflex|PRO PLEX 450|
|trse|TRS2|
|u46|U 46 D|
|U46B|U 46 D|
|U46D|U 46 D|
|U46M|U 46 M|
|UNIMAX|UNIX MAX|
|urican|HURRICANE|
|USAR|HUSSAR PRO|
|vauxan|VOXAN|
|XERIAC|CERIAX|
|znith|ZENIT|
|zozys|ZOXIS|