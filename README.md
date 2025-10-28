🧩 Étape 1 – Scraping des données (rk.py)
🎯 Objectif :

Extraire les statistiques des joueurs pour chaque ligue et chaque saison entre 2017 et 2025.

🔧 Fonctionnement :

Le script :

Parcourt 5 ligues : Premier League, La Liga, Bundesliga, Serie A, Ligue 1.

Scrape 5 catégories statistiques : possession, passing, gca, shooting, playingtime.

Enregistre les données dans des fichiers CSV du type :

top_5_leagues_{category}_2017-2025.csv


Exemple : top_5_leagues_shooting_2017-2025.csv

🚀 Exécution :
python rk.py

Le script prend 6 minutes pour exécuter le scrapping pour une catégorie.

Et il prend 30 minutes pour toutes les catégories.


⏳ Temps estimé : plusieurs minutes (le script scrape plusieurs saisons et ligues).

🧮 Étape 2 – Calcul du ranking (ranking.py)
🎯 Objectif :

Créer un système de notation complet et produire un classement final des joueurs.

🔧 Fonctionnement :

Le script :

Importe les fichiers CSV générés par rk.py.

Nettoie les données (formatage, normalisation, suppression de colonnes inutiles).

Crée un ID unique pour chaque joueur (player_id).

Calcule des scores par catégorie :

🎨 Creativity → à partir du passing

⚡ Performance → à partir du gca

💪 Impact → à partir du playingtime

🎯 Finition → à partir du shooting

🧩 Dribble → à partir du possession

Combine ces scores dans un tableau final final.csv.

Calcule la Note Globale (somme pondérée des 5 catégories).

Génère un fichier de classement complet : ranking_vf.csv.

🚀 Exécution :
python ranking.py

Le script prend moins de 20 secondes à s'éxécuter.

Parcourt automatiquement les saisons de 2017 à 2024.
Scrape les données depuis le site FBref.com pour les 5 grands championnats européens.
Récupère les statistiques des joueurs pour plusieurs catégories (possession, passes, tirs, etc.).
Regroupe et enregistre les données dans des fichiers CSV, un par catégorie.
Chaque ligne du CSV correspond à un joueur, avec des informations comme son nom, son équipe, la saison, la ligue et les statistiques détaillées.
