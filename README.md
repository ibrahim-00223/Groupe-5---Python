📘 INSTRUCTION — Extraction de statistiques de football (FBref)
1️⃣ Comment exécuter le code
Exécute le script avec :
python3 rk.py
Le script va automatiquement lancer le scraping et créer plusieurs fichiers CSV dans le même dossier.

2️⃣ Durée d’exécution
Le script prend 6 minutes pour exécuter le scrapping pour une catégorie.

Et il prend 30 minutes pour toutes les catégories.

3️⃣ Modifications possibles
L’utilisateur peut facilement modifier les paramètres suivants :

Les saisons à analyser (ligne 17 du code)
years = range(2017, 2025)
(par exemple range(2020, 2023) pour réduire le temps d’exécution)

Les catégories de statistiques à extraire (ligne 158 du code)
categories = ["possession", "passing", "gca", "shooting", "playingtime"]
(tu peux retirer ou ajouter des catégories selon ce que tu veux récupérer)

Les ligues concernées (ligne 17 du code)
leagues = {
    "Premier-League": "9",
    "La-Liga": "12",
    "Bundesliga": "20",
    "Serie-A": "11",
    "Ligue-1": "13"
}
(tu peux enlever une ligue ou en ajouter si tu connais son identifiant FBref)

4️⃣ Fonctionnement global du code
Le script effectue les actions suivantes :

Parcourt automatiquement les saisons de 2017 à 2024.
Scrape les données depuis le site FBref.com pour les 5 grands championnats européens.
Récupère les statistiques des joueurs pour plusieurs catégories (possession, passes, tirs, etc.).
Regroupe et enregistre les données dans des fichiers CSV, un par catégorie.
Chaque ligne du CSV correspond à un joueur, avec des informations comme son nom, son équipe, la saison, la ligue et les statistiques détaillées.
