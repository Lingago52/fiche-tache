# Projet : Pendule d'échecs avec Arduino

## Présentation
Réalisation d'une pendule d'échecs électronique pour deux joueurs à l'aide d'une carte Arduino.

Le programme fourni utilise deux boutons poussoirs :
- Joueur 1 : broche D2
- Joueur 2 : broche D3

Chaque joueur dispose de 5 minutes. Le temps du joueur actif diminue et l'appui sur son bouton passe la main à l'autre joueur. Les temps et les messages sont affichés dans le Moniteur Série à 9600 bauds.

## Liste des tâches

| N° | Tâche | Résultat attendu |
|---:|---|---|
| 1 | Analyser le fonctionnement du code Arduino fourni | Comprendre les variables, les boutons et la gestion des chronomètres |
| 2 | Identifier les composants nécessaires | Carte Arduino, deux boutons poussoirs, fils et plaque d'essai |
| 3 | Réaliser le schéma électrique | Bouton J1 entre D2 et GND ; bouton J2 entre D3 et GND |
| 4 | Câbler les deux boutons sur la carte Arduino | Obtenir un montage conforme au schéma avec `INPUT_PULLUP` |
| 5 | Installer et configurer l'IDE Arduino | Pouvoir téléverser le programme sur la carte |
| 6 | Téléverser le programme dans l'Arduino | Démarrer le programme sans erreur de compilation |
| 7 | Ouvrir le Moniteur Série à 9600 bauds | Voir le message de démarrage et les temps |
| 8 | Tester le démarrage avec le bouton du joueur 1 | Vérifier que le joueur 2 devient actif |
| 9 | Tester le démarrage avec le bouton du joueur 2 | Vérifier que le joueur 1 devient actif |
| 10 | Tester le décompte des deux chronomètres | Vérifier que seul le temps du joueur actif diminue |
| 11 | Tester le changement de joueur | Vérifier que chaque bouton passe la main à l'adversaire |
| 12 | Tester la fin du temps | Vérifier que la partie s'arrête lorsqu'un chronomètre atteint zéro |
| 13 | Corriger les défauts constatés pendant les essais | Obtenir un fonctionnement fiable et régulier |
| 14 | Améliorer la présentation de l'affichage si nécessaire | Rendre les deux temps faciles à lire |
| 15 | Réaliser le montage final et documenter le projet | Présenter le montage, le code et les résultats des tests |

## Branchement prévu

- Bouton du joueur 1 : D2 et GND.
- Bouton du joueur 2 : D3 et GND.
- Les entrées sont configurées en `INPUT_PULLUP` : bouton relâché = HIGH ; bouton appuyé = LOW.

## Tests à effectuer

- [ ] La carte démarre et affiche le message d'accueil.
- [ ] Un appui sur le bouton J1 lance la partie et donne la main à J2.
- [ ] Un appui sur le bouton J2 lance la partie et donne la main à J1.
- [ ] Le chronomètre du joueur actif diminue.
- [ ] Le chronomètre de l'autre joueur reste stable.
- [ ] Chaque joueur peut passer la main avec son bouton.
- [ ] La partie s'arrête lorsqu'un temps atteint zéro.

## Limites du programme actuel

- L'affichage est réalisé dans le Moniteur Série ; aucun écran LCD ou OLED n'est prévu dans le code fourni.
- Les temps sont initialisés à 5 minutes dans le programme.
- Le programme utilise `delay(300)` pour limiter les détections répétées ; ce comportement devra être vérifié lors des essais.
- Le code fourni ne prévoit pas de bouton de remise à zéro ni de réglage de la durée.

## Arborescence conseillée pour GitHub

```text
pendule-echecs-arduino/
├── README.md
└── pendule-echecs-arduino.ino
```
