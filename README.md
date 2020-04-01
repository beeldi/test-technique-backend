
# Introduction

### La maintenance technique du bâtiment :

Les propriétaires de bâtiments ont besoin d’acteurs fiables leur permettant de gérer et de contrôler leurs biens. Satisfaire l’ensemble de ces exigences devient donc un véritable défi.
Qu’il s’agisse d’une résidence, d'un local commercial, d'un bureau, d’un entrepôt logistique ou d’un simple local de stockage, une bonne gestion technique des bâtiments est fondamentale.

La maintenance technique est la gestion technique des équipements et installations du bâtiment : chauffage, ventilation, climatisation, électricité, plomberie, ascenseur, etc.
Celle-ci requiert entre autres une bonne connaissance technique des équipements qui composent le bâtiment afin :

- de procéder réguliérement à leur contrôle technique ;
- d'identifier les défauts / malfonctions ou mauvais réglages ;
- d'assurer leur maintenance et prévoir leur remplacement.

# Sujet

Vous devrez décrire un design API RESTful qui pourra permettre de :

- Créer/Modifier des templates d'équipement génerique. Ces templates sont appelés `MetaEquipment`, ils sont la base constitutive d'un équipment réel. Les équipements génériques décrivent les équipements réels. Tout équipement réel a donc son équipement générique associé. Un `MetaEquipment` peut lui-même dériver d'un `MetaEquipment` parent. Exemple : 

        |BATIMENT| <-- |FACADE| <-- |FACADE LEGERE| 

    Nous voyons dans cet exemple qu'un équipement générique `façade légère` à pour parent une `façade` qui a lui-même pour parent `bêtiment`. 

- Créer/Modifier des templates de défaut générique. Ces templates sont appelés `MetaDefect`, ils sont la base constitutive d'un défaut réel d'un équipement réel.
Les défauts génériques décrivent les défauts réels. Tout défaut réel a donc son défaut générique associé. Un `MetaDefect` est associé.

- Créer/Modifier des templates de point de contrôle générique. Ces templates sont appelés `MetaCheckpoint`, ils sont la base constitutive d'un point de contrôle réel. Les points de contrôle génériques exposent les défauts génériques possibles pour un/plusieurs équipement(s) générique(s). Exemple :

        |BATIMENT|- - - - - - - - - - -|META DEFECT| 
                  \                   /
                   \                 /
                    |META CHECKPOINT|
                   /                 \
                  /                   \
             |CVC|- - - - - - - - - - -|META DEFECT|

    Nous voyons dans cet exemple qu'un point de contrôle générique rattaché aux équipements génériques Bâtiment et CVC expose deux défauts génériques qui sont propres à chacun de ces équipements génériques.

- Créer/Modifier des équipements réels et renseigner leurs informations. Les équipments peuvent également être accompagnés de `composants` qui sont fonction du `MetaEquipment` de l'équipement réel. Les `composants` sont un groupement d'informations logiques représantant une sous-partie fonctionnelle d'un équipement réel. 

- Compléter les points de contrôle d'un équipement réel.

- Ajouter un/des défaut(s) réel(s) à un équipement réel au travers (ou non) de ses points de contrôle.

Vous aurez à charge de définir le modèle des données à manipuler, il ne sera pas nécessaire d'être exhaustif. Cependant, nous serons attentifs à la pertinence des choix qui seront fait. 
Vous êtes libre de choisir les technologies qui vous sembleront les plus pertinentes, vous serez questionné sur ces choix et devrez donc être capable de les justifier. Ce sujet reste volontairement libre et nous attendons une certaine imagination et créativité de votre part. 

# Rendu

Ce test consiste à présenter un design d'API ainsi que le choix de la stack technique qui
devra la mettre en oeuvre. Pour ce faire, voici les livrables attendus :

- un document OpenAPI / Swagger qui décrit votre API ;
- une présentation de votre API / Stack qui étaye vos choix; des schémas explicatifs en support seront appréciés ;
- en option, un mini serveur géneré depuis votre document OpenAPI / Swagger afin de tester votre solution.

# One more thing

BON COURAGE !
