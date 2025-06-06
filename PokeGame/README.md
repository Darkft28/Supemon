# Supémon - Jeu RPG

## 1. Aperçu
Supémon est un jeu RPG au tour par tour où les joueurs peuvent combattre, capturer et entraîner des créatures appelées Supémons. Le jeu inclut l'exploration, un système de boutique, un centre de soin et une fonctionnalité de sauvegarde.

---
## 2. Fonctionnalités

### 2.1 - Lancement du jeu
- Le joueur doit entrer un nom.
- Le jeu propose un Supémon de départ.
- Option de charger une partie sauvegardée.

### 2.2 - Actions hors combat
- **Explorer la nature** : Lance un combat contre un Supémon aléatoire.
- **Boutique** : Acheter ou vendre des objets.
    - Mode achat : Affiche la liste des objets avec description et prix.
    - Mode vente : Affiche les objets du joueur et leur prix de vente.
- **Centre Supémon** : Soigne tous les Supémons du joueur gratuitement.
- **Quitter le jeu** : Option de sauvegarde avant de quitter.

### 2.3 - Joueur
- Possède un nom.
- Possède une liste de Supémons.
- Choisit un Supémon pour combattre.
- Utilise des Supcoins pour acheter des objets.
- Possède une liste d'objets.

### 2.4 - Supémons
Chaque Supémon a :
- Un nom
- Un niveau (commence à 1)
- Une expérience (commence à 0)
- Des PV et PV max
- Attaque et Attaque de base
- Défense et Défense de base
- Esquive et Esquive de base
- Précision et Précision de base
- Vitesse (détermine l'ordre des tours)
- Une liste d'attaques

#### Supémons de départ
- **Supmander** :
    - PV : 10, Attaque : 1, Défense : 1, Esquive : 1, Précision : 2, Vitesse : 1
    - Attaques : Griffure (3 dmg), Rugissement (+1 Attaque)
- **Supasaur** :
    - PV : 9, Attaque : 1, Défense : 1, Esquive : 3, Précision : 2, Vitesse : 2
    - Attaques : Charge (2 dmg), Feuillage (+1 Esquive)
- **Supirtle** :
    - PV : 11, Attaque : 1, Défense : 2, Esquive : 2, Précision : 1, Vitesse : 2
    - Attaques : Charge (2 dmg), Carapace (+1 Défense)

#### Mécanique de combat
- Les attaques infligent des dégâts ou modifient des statistiques.
- Formule des dégâts : `(Attaque_Lanceur x Dégâts) / Défense_Cible` (arrondi à 50%)
- Taux de réussite d'une attaque : `Précision_Lanceur / (Précision_Lanceur + Esquive_Cible) + 0.1`

### 2.5 - Système de Combat
- Les combats sauvages correspondent au niveau du Supémon du joueur.
- Le Supémon avec la vitesse la plus élevée attaque en premier (aléatoire en cas d'égalité).
- Options du joueur :
    1. **Utiliser une attaque** : Choisir une attaque.
    2. **Changer de Supémon** : Passe le tour.
    3. **Utiliser un objet** : Un objet par tour, maximum 4 par combat.
    4. **Fuir** : Chance de réussite = `Vitesse_Joueur / (Vitesse_Joueur + Vitesse_Ennemi)`.
    5. **Capturer** : Chance de réussite = `(PV_Max_Ennemi - PV_Ennemi) / PV_Max_Ennemi - 0.5`.
- L'ennemi choisit une attaque aléatoirement.
- Fin du combat : Un Supémon atteint 0 PV.
- Victoire : 100-500 Supcoins + 100-500 XP par niveau ennemi.

### 2.6 - Objets
- **Potion** : +5 PV (100 Supcoins)
- **Super Potion** : +10 PV (300 Supcoins)
- **Bonbon Rare** : +1 Niveau (700 Supcoins)
- Prix de vente = Prix d'achat / 2.

### 2.7 - Expérience & Niveaux
- L'augmentation de niveau augmente toutes les stats de **30%** (arrondi à 50%).
- Conditions de niveau :
    - Niveau 2 : 500 XP
    - Chaque niveau suivant : +1 000 XP supplémentaires.

### 2.8 - Système de sauvegarde
- Sauvegarde des données du joueur : nom, Supémons (stats & niveau), objets et Supcoins.

---
## 3. Comment Jouer
1. Démarrer une nouvelle partie ou charger une sauvegarde.
2. Choisir un Supémon de départ.
3. Explorer, combattre, acheter et soigner ses Supémons.
4. Monter en niveau, capturer des Supémons et gérer son inventaire.
5. Sauvegarder et quitter au besoin.

---
## 4. Installation
1. Téléchargez les fichiers du jeu.
2. Exécutez `main.exe`.
3. Suivez les instructions à l'écran.

Profitez de votre aventure avec les Supémons !

