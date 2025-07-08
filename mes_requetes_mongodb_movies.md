# Exercices MongoDB - Movies

Dans le cadre de ma formation en science des données appliquées, j’ai pratiqué quelques requêtes MongoDB , aujourdhui, nous allons faire de même sur ma base de données `angelguems` avec la collection `movies`.

---

##  Connexion à la base de données

##  Liste des bases disponibles
```javascript
show dbs// voir toutes les bases disponibles
###   Résultat:
```javascript
College       8.00 KiB
admin        40.00 KiB
angelguems   12.34 MiB
config      108.00 KiB
gesres       72.00 KiB
info         40.00 KiB
local        72.00 KiB
premierP      8.00 KiB
produits     24.00 KiB
ua2          48.00 KiB

###  Sélection de la base angelguems
```javascript
use angelguems

###  Vérification des collections disponibles
```javascript
show collections
###  Résultat :
```javascript
movies

##  Requêtes MongoDB sur la collection movies
###  Afficher les 5 premiers documents
angelguems> db.movies.find().limit(5)

### Lister tous les titres de films
db.movies.find({}, { title: 1, _id: 0 }) // Récupérer uniquement les titres des films sans afficher l’ID.


