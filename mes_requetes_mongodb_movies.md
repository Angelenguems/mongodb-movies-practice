# Exercices MongoDB – Collection Movies

Dans le cadre de ma formation en Sciences des données appliquées, j’ai pratiqué quelques requêtes MongoDB.  
Aujourd’hui, j’explore la base de données `angelguems` et sa collection `movies`.

---

## 🔗 Connexion à la base de données

### 🔍 Lister toutes les bases disponibles
```javascript
Voir mes difeerentes bases de données 
show dbs
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
Utiliser la bases de données "angelguems"
use angelguems
voir les collections de cette base de données 
show collections
movies
Affiche les 5 premiers films dans la collection.
db.movies.find().limit(5)
Récupèrer uniquement les titres des films sans afficher l'ID
db.movies.find({}, { title: 1, _id: 0 })
Obtenir le nombre total d'enregistrements dans la collection movies
db.movies.countDocuments()
Trouver les filmer sortis après 2015
db.movies.find({ year: { $gt: 2015 } })
lister tous les fims du genre "comedie"
db.movies.find({ genres: "Comedy" })
Lister les films par ordre decroissant d'année de publication
db.movies.find().sort({ year: -1 })
Afficher les films avec une note superieure à 8
db.movies.find({ rating: { $gt: 8 } })
Afficher uniquement les films et les annees des films sans le "_id"
db.movies.find({}, { title: 1, year: 1, _id: 0 })








