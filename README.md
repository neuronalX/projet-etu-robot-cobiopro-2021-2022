# Projet M2 option Robot Enseirb/ESNC 2021-2022
Projet des étudiants option Robot de l'Enseirb/ENSC de Bordeaux pour le cours "Apprentissage"

Il est possible de choisir 5 sujets par groupe de 2/3 étudiants. Chaque groupe doit choisir un sujet différent des autres.
Afin de définir quels sont les sujets pour quels groupes, merci de faire une Pull-Request en donnant les noms et prénoms des membres du groupe, un nom de groupe et le sujet choisi.

## 1.a. Retrouver les angles manquants
Montrer qu’on a bien appris les positions (statiques) et qu’on est capable de reconstruire les angles manquants pour une personne amputée, à partir des angles de son épaule et de la position (désirée) de sa main:

En entrée: 
shPitch, shRoll, 
handRemapPosX, handRemapPosY, handRemapPosZ
handRemapPitch, handRemapRoll, handRemapYaw

En sortie: 
armYaw, elbPitch, forearmYaw, wriPitch, wriRoll

## 1.b. Retrouver la position du coude/poignet
Similairement au 1.a., montrer qu’on peut retrouver (en sortie) la position du coude (elbRemapPosX, elbRemapPosY, elbRemapPosZ) ou du poignet (wriRemapPosRefElbX, wriRemapPosRefElbY, wriRemapPosRefElbZ)

## 2. Prédiction position
Aller progressivement vers une cible: pour une cible donnée (tgtRemapPosX, tgtRemapPosY, tgtRemapPosZ), considérer la position actuelle de la main (handRemapPosX, handRemapPosY, handRemapPosZ), et tenter d'avancer en ligne droite par incréments (de l’ordre de 3-5cm). Pour cela, tenter de prédire les 7 angles (shPitch, shRoll, armYaw, elbPitch, forearmYaw, wriPitch, wriRoll) pour être dans cette position (handRemap + incrément de 3cm), connaissant les angles courants de l’épaule (shPitch, shRoll), la position actuelle (handRemapPosX, handRemapPosY, handRemapPosZ) et la position visée (handRemap + incrément); et donc entrainer un réseau à apprendre ce type d’association, en cherchant sur les trajectoires des couples de positions distantes de 3-5cm. 

## 3.a Prédiction de séquence avec Reservoir Computing
A partir des séquences de positions actuelles et/ou séquences d'angles, prédire sur les séquences :
- prédire à T+1, T+5, T+15, T+50
- en utilisant des combinaisons de variables différentes
- séparer les données pour chaque sujet en faisait une 5-fold cross-validation 


## 3.a Prédiction de séquence avec LSTMs
Similaire au 3.a mais avec des réseaux LSTM.

# Groupes
1.
2.
3.
4.
5.
