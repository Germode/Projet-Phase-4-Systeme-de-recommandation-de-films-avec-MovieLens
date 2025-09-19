# Projet Phase 4 Système de recommandation de films avec MovieLens
### Projet réalisé dans le cadre du bootcamp organisé par AKADEMI, Option data science + IA
**Préparé et présenté par :** Saint Germain Emode </br>
**Email** germodee12@gmail.com

![MovieLens](https://github.com/Germode/Projet-Phase-4-Systeme-de-recommandation-de-films-avec-MovieLens/blob/main/Images/Moovies.png)

# Aperçu
Le projet consiste à concevoir un système de recommandation de films capable de proposer à chaque utilisateur les films qu’il est le plus susceptible d’apprécier. Pour ce faire, nous avons utilisé l’ensemble de données MovieLens 100k, fourni par le laboratoire GroupLens de l’Université du Minnesota.
- L’ensemble de données contient 100 000 évaluations provenant de plusieurs milliers d’utilisateurs et de milliers de films.
- Chaque évaluation est notée sur une échelle de 0.5 à 5 étoiles.
- Le projet utilise une approche de filtrage collaboratif, complétée par un filtrage basé sur le contenu pour créer un modèle hybride capable de gérer le problème du démarrage à froid.

# Objectif
**Objectif principal :**
- Fournir à chaque utilisateur une liste personnalisée de 5 films recommandés basés sur ses préférences passées et les comportements d’autres utilisateurs.

**Objectifs secondaires :**
- Évaluer la performance du modèle à l’aide de métriques standards telles que RMSE et MAE.
- Explorer la combinaison de méthodes collaboratives et basées sur le contenu pour améliorer la précision et la ro
- Problématique métier : « Comment maximiser la satisfaction des utilisateurs en anticipant les films qu’ils aimeront, tout en gérant les nouveaux films et nouveaux utilisateurs sans données historiques ? »

 # Exploration et Prétraitement des Données
Les données sont complètes et cohérentes, permettant de construire un système de recommandation hybride, combinant les préférences explicites des utilisateurs (notes) 
et les caractéristiques des films (genres et tags).

### Fichiers chargés
- movies.csv : contient les films avec movieId, title et genres (plusieurs genres possibles, séparés par |).
- ratings.csv : contient les notes des utilisateurs (userId, movieId, rating, timestamp).
- links.csv : relie chaque film à ses identifiants IMDb et TMDb, utile pour enrichir les données.
- tags.csv : mots-clés attribués par les utilisateurs pour décrire les films, pouvant améliorer le filtrage basé sur le contenu.

### Structure et observations
- movies : 3 683 films, genres multiples → utile pour analyser les préférences par genre.
- ratings : beaucoup de lignes → capture les interactions utilisateur-film, indispensable pour le filtrage collaboratif.
- tags : informations qualitatives → possibilité d’ajouter des recommandations basées sur le contenu.

