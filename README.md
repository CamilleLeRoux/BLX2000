# BLX2000 Boîtes Logiques eXtra-smart 2000

## Tiroirs connectés

#### Cibles
- Particuliers

### Sujet

Le but du projet vise en la gestion et sécurisation du contenu d'un ensemble de tiroirs connectés que nous appellerons BLX.

Le BLX consistera au control de moteurs permettant d'ouvrir, fermer ou bloquer cet ensemble de tiroirs. En cela le BLX aidera l'utilisateur à ranger ses affaires dans les tiroirs qu’il a désigné, au BLX, comme étant conteneur d'un tel type d'affaire. 

Par extension et avec l'aide de services de scheduling, de météo ou même d'appareils connectés diffusant de l'information, le BLX pourra ouvrir de manière autonome la bonne séquence de tiroirs pour présenter à l'utilisateur le(s) contenu(s) dont il a besoin à un instant t. Par ailleurs s'il n'est pas explicitement prévu que le contenu d'un tiroir doive être consulter (et que le contenu est sensible), le BLX pourra bloquer les moteurs du tiroir et maintenir ce dernier verrouillé. 

Exemple 1 : 

Un rangement constitué d'un ensemble de tiroirs à vêtements. Le BLX aidera l'utilisateur à ranger les t-shirt à manche courtes puis les pull puis les jeans et ainsi de suite afin de permettre à l'utilisateur d'être facilement organisé.

De plus le matin, le BLX récupérera l'information de l'heure du levé par un réveil connecté ou un agenda et déclenchera son process. En récupérant l'information météorologique depuis un service météo et l'information de l'agenda de l'utilisateur, le BLX ouvrira la bonne séquence de tiroirs pour proposer à l'utilisateurs à peine réveillé uniquement les types de vêtements adaptés à sa journée. Ainsi l’utilisateur ne se fera plus surprendre par des imprévus (météorologiques entres autres). Exemple : beau temps => tenue légère, rendez-vous important => costume cravate. 

Couplé à cela un capteur de présence et de luminosité détermineront s’il est nécessaire d'allumer une lampe dans le tiroir pour aider l'utilisateur à y voir. 

Un capteur d'humidité entre autres fera remonter des alertes au web service du BLX en cas de compromission du contenu du tiroir. 
Ce même web service sert au monitoring et à la gestion de l'ensemble de tiroirs, soit du BLX (affectation des tiroirs, affichage des alertes, gestion du planning...). 

Si l'utilisateur ne veut plus qu'un autre membre de son entourage fouille dans ses affaires ou utilise son linge, il peut paramétrer les tiroirs comme étant sécurisés. De ce fait s'il n'est pas prévu dans le planning qu'un individu soit servi par le BLX, les moteurs bloqueront l'ouverture des tiroirs à moins de fournir une confirmation (authentifiée) via le web serveur.

Cet exemple peut être adapter pour une utilisation plus administrative. 

Exemple 2 :

Un rangement de documents, chaque tiroir est affecté par l’utilisateur à un type de document (exemple de documents : des livres de cours). Avec l’information du planning/agenda de l’utilisateur le BLX pourra savoir comment servir l’utilisateur.

Quand l’utilisateur rentre chez lui (horaire prévu dans l’agenda) le BLX pourra l’aider à ranger ses documents en ouvrant successivement les tiroirs correspondants aux types de documents que l’utilisateur à utilisé aujourd’hui (information de l’agenda). 

Ensuite le BLX pourra l’aider à préparer ses documents pour la journée suivante, encore une fois grâce à l’agenda de l’utilisateur. Ce dernier n’aura qu’à récupérer le contenu des tiroirs ouverts pour avoir les documents nécessaires à sa prochaine journée (sans avoir à tous les trier à la volée et à réfléchir en fonction de son planning pour les sélectionner). 

De plus si certains tiroirs contiennent des documents sensibles, l’utilisateur n’aura qu’à les paramétrer comme étant des tiroirs à sécuriser et ainsi les moteurs de ces tiroirs bloqueront leur ouverture en dehors des accès prévus.

### Liste matérielle 

TODO : mettre les pointeurs vers le matériel sélectionné et confirmer les choix
-	1 Raspberry
-	1 GroovePi
-	2 ou 4 petits moteurs pour les 2 tiroirs du prototype
-	1 capteur de présence
-	1 capteur de luminosité
-	(2 capteurs d’humidité, not sure)
-	2 ou + LED ou éclairage équivalent
-	1 ou + bouton(s)

Extension possible pour intégrer un petit équivalent de réveil connecté diffusant l’information sur l’heure du réveil de l’utilisateur
-	1 microcontrôleur type Genuino101 ou 1 Raspberry à voir


### Scénario

- Gontrand-Lucien se fait réveiller par son réveil connecté et s'exclame "J'ai bien dormi !! Quel temps fait-il aujourd'hui ?". En parallèle, le BLX 2000 est informé que Gontrand-Lucien vient de se réveiller, et grâce au service météo, le BLX 2000 sait qu'il fera beau aujourd'hui. Il sait aussi que Gontrand-Lucien n'a pas de rendez-vous professionnel aujourd'hui d'après son agenda. Il va donc proposer un petit ensemble short/T-shirt à notre protagoniste, sans oublier ses tongues préférées.
- Gontrand-Lucien se réveille en avance et ne veut pas se recoucher car il sait qu'il n'arrivera pas à se rendormir, il peut alors appuyer sur un bouton situé sur le BLX 2000 afin de forcer le traitement et ouvrir le compartiment adéquat avant l'heure de réveil normale.
- Quand l'utilisateur se présente devant le BLX 2000 et que ce dernier est en position ouverte, un capteur de présente le détecte, et un capteur de luminosité détecte s'il y a assez de lumière, si ce n'est pas le cas, des lampes s'allument dans les tiroirs ouverts pour que l'utilisateur puisse mieux en voir le contenu.
- Des capteurs d'humidité sont également présents dans les tiroirs et envoient une notification à l'utilisateur si l'humidité dépasse un certain seuil afin de l'informer qu'il est possible que de la moisissure se forme.
- Une fois que Gontrand-Lucien a finit, les tiroirs se ferment et les moteurs se bloquent afin de les verrouiller. Ainsi son frère Abidbole ne pourra pas venir lui voler de vêtements plus tard dans la journée.

### Objectif de premier sprint

- Le Rasp se connecte à un service de météo et affiche sur la WebApp le tiroir à ouvrir.

### GANTT

![Gantt](https://github.com/CamilleLeRoux/BLX2000/blob/master/GANTT.png)

### Architecture Matérielle

![Architecture Matérielle](https://github.com/CamilleLeRoux/BLX2000/blob/master/Dessin.png)

### Architecture Embarquée

![Architecture Matérielle Embarquée](https://github.com/CamilleLeRoux/BLX2000/blob/master/archi_materielle_embarque.jpg)

![Architecture Logicielle Embarquée](https://github.com/CamilleLeRoux/BLX2000/blob/master/archi_log_embarque.jpg)

### Membres du projet
- Alexandre HOWARD
- Camille LE ROUX
- Quentin MOREAU
- Balsam CHIHI
