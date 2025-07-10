# Exercices MongoDB – Collection Movies

Dans le cadre de ma formation en Sciences des données appliquées, j’ai pratiqué quelques requêtes MongoDB.  
Aujourd’hui, j’explore la base de données `angelguems` et sa collection `movies`.

---

##  Connexion à la base de données

###  Lister toutes les bases disponibles
```javascript
show dbs
```
### Résultat attendu :

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
#### Sélectionner la base angelguems
```JavaScript
use angelguems
```
 #### Vérifier les collections disponibles
```JavaScript

show collections
```
### Résultat :

movies
 ## Requêtes MongoDB sur la collection movies
#### 1. Afficher les 5 premiers documents
```JavaScript
db.movies.find().limit(5)
```
#### 2. Lister tous les titres des films
```JavaScript

db.movies.find({}, { title: 1, _id: 0 })
```
#### 3. Compter le nombre total de films
```JavaScript

db.movies.countDocuments()
```
#### 4. Trouver les films sortis après 2015
```JavaScript

db.movies.find({ year: { $gt: 2015 } })
```
#### 5. Lister tous les films du genre "Comédie"
```JavaScript

db.movies.find({ genres: "Comedy" })
```
#### 6. Trier les films par année décroissante
```JavaScript

db.movies.find().sort({ year: -1 })
```
#### 7. Afficher les films avec une note supérieure à 8
```JavaScript

db.movies.find({ rating: { $gt: 8 } })
```
#### 8. Afficher uniquement les titres et les années (sans l'ID)
```JavaScript

db.movies.find({}, { title: 1, year: 1, _id: 0 })
```
## Conclusion

Ces requêtes simples m'ont permis de manipuler une base de données NoSQL, de filtrer, trier et analyser les informations issues d'une collection MongoDB.  
Elles illustrent les bases essentielles de l’interrogation de données dans un environnement orienté document.
Cette exploration est une première étape vers une maîtrise plus approfondie des bases de données NoSQL.


