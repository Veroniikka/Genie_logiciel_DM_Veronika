
### Prototype d'une base de données des néologismes russes et l'API

Cette application est une application web développée avec Flask et Bokeh pour visualiser les données de la base de données des néologismes russes. L'application se connecte à une base de données MySQL pour extraire des données et créer un tableau et des diagrammes basés sur ces données.



#### Lancement de l'application
1. Le code de l'application se trouve dans un fichier `app.py`.
2. Lancez l'application avec la commande :

python app.py


3. Ouvrez votre navigateur web et accédez à l'adresse `http://localhost:5001/`.

#### Utilisation de l'API pour obtenir des données

- **Voir l'interface Web qui réprésente le tableau de néologismes et les diagrammes:**
  Accédez à l'adresse `http://localhost:5001/api/v1/neologismes` pour obtenir le tableau de néologismes et les diagrammes. 
  Si vous cliquez sur un mot dans le tableau, vous pouvez voir des informations sur le néologisme : traduction en français, partie du discours et thème.
  L'application propose deux graphiques :
1. Diagramme de distribution thématique des néologismes
2. Diagramme de distribution des néologismes par partie du discours

Ces graphiques sont de type camembert. Si vous placez votre souris sur un secteur du graphique, vous pouvez voir les pourcentages.

Le tableau et les graphiques sont automatiquement mis à jour si des modifications sont apportées à la base de données. 

- **Obtenir toutes les données :**

  Accédez à l'adresse `http://localhost:5001/api/v1/all_data` pour obtenir des données de toutes les tables de la base de données.
  Il s'agit d'un format json, actuellement les mots cyrilliques ne sont pas affichés correctement.



- **Obtenir des données sur un néologisme par ID :**
  Accédez à l'adresse `http://localhost:5001/api/v1/neologismes/<id>` et remplacez `<id>` par un identifiant spécifique de néologisme pour obtenir des informations détaillées sur le néologisme.

- **Obtenir des données par partie du discours (POS) :**
  Accédez à l'adresse `http://localhost:5001/api/v1/pos` pour obtenir la liste de toutes les parties du discours.

- **Obtenir des données par thème :**
  Accédez à l'adresse `http://localhost:5001/api/v1/theme` pour obtenir la liste de tous les thèmes.


- **Autres fonctionnalités de l'API**
- Ajouter un nouveau néologisme

- Mettre à jour les informations sur un néologisme
 
- Supprimer un néologisme par ID
 
