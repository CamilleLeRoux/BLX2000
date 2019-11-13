# BLX2000

## Vide-poches connecté

#### Cibles
- Particuliers

### Sujet

Le but du projet vise en la gestion et sécurisation du contenu d'un meuble d'entrée connecté que nous appellerons BLX.

Le BLX consistera au contrôle de moteurs permettant d'ouvrir, fermer ou bloquer les tiroirs de ce meuble. En cela le BLX aidera l'utilisateur à partir de chez lui avec le nécéssaire, c'est à dire, ses clés et ses papiers notamment. 

Par extension et avec l'aide de services de scheduling, de météo ou même de gps, le BLX pourra ouvrir de manière autonome la bonne séquence de tiroirs pour présenter à l'utilisateur le(s) contenu(s) dont il a besoin à un instant t. Par ailleurs s'il n'est pas explicitement prévu que le contenu d'un tiroir doive être consulter, le BLX pourra bloquer les moteurs du tiroir et maintenir ce dernier verrouillé. On vous volera plus vos clés !

Fonctionnalités :
- Présenter à l'utilisateur le(s) contenu(s) dont il a besoin pour circuler en exterieur selon son planning entre autres
- Permettre l'accès au contenu correspondant à l'utilisateur (même hors planning)
- Sécuriser le contenu des tiroirs 


### Liste matérielle 

TODO : mettre les pointeurs vers le matériel sélectionné et confirmer les choix
-	1 Raspberry
-	1 GrovePi
-	3 petits moteurs pour les 6 petits compartiments du prototype
-	1 capteur de présence
-	1 capteur de luminosité
- 1 capteur NFC
-	4 LED ou éclairage équivalent
-	1 bouton(s)
- (1 buzzer TBD)


### Scénario

Hypothèse : Une habitation de deux utilisateurs (JC et CL), un agenda présentant leur organisation (horaires de travail par exemple)

JC part le matin pour son travail, ceci étant spécifié dans son google agenda, le BLX a prévu l'ouverture des compartiments où sont les clés et les papiers de JC. Le BLX présente donc à JC, quand il sera prêt à partir, ses clés et ses papiers. Il allume l'éclairage dans les compartiments pour qu'ils soient plus visibile à JC car il fait sombre ce matin là. En parallèle de cela, le BLX a récupéré les informations de la météo, il va pleuvoir. Ainsi même si le lieu de travail de JC est proche et qu'il n'a habituellement pas besoin de ses papiers/clés de voiture, le BLX les lui présentera en plus de ses clés de maison. JC part de chez lui avec ses clés de maison et de voiture ainsi que ses papiers. Il n'a pas pu prendre les clés de CL car les compartiments dédiés à CL furent bloqués par les moteurs du BLX. CL plus tard se lève pour aller à son travail et le scénario se répète pour CL.
Quand JC et CL rentreront le soir, conformément à leur planning, le BLX ouvrira les compartiments qui leur sont attribués afin que JC et CL "se visent successivement les poches".
JC et CL prévoient à la dernière minute de partir en balade, cela n'est pas prévu dans le planning mais pas d'inquiétude JC peut faire scanner son badge NFC de secours pour que le contenu de ses compartiments lui soit présenté et que le couple puisse avoir un trousseau de clés avant de partir. (S'ils n'y pensent pas, le capteur de présence surveillant le départ pourra déclencher une petite alerte pour reppeler à JC et CL de ne pas oublier leurs clés entre autres TBD)

### Objectif de premier sprint

- Une chaine Node-Red pour mettre en oeuvre l'usage de quelques services dont nous auront besoin

### GANTT

![Gantt](https://github.com/CamilleLeRoux/BLX2000/blob/master/GANTT.png)

### Architecture Matérielle (Dessin pas up-to-date)

![Architecture Matérielle](https://github.com/CamilleLeRoux/BLX2000/blob/master/Dessin.png)

### Architecture Embarquée (Dessins pas up-to-date)

![Architecture Matérielle Embarquée](https://github.com/CamilleLeRoux/BLX2000/blob/master/archi_materielle_embarque.jpg)

![Architecture Logicielle Embarquée](https://github.com/CamilleLeRoux/BLX2000/blob/master/archi_log_embarque.jpg)

### Membres du projet

- Alexandre HOWARD
- Camille LE ROUX
- Quentin MOREAU
- Balsam CHIHI
