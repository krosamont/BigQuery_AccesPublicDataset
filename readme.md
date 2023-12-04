# Big Query : Initiation

**Comment utiliser les tables publiques de BigQuery gratuitement**

BigQuery est un entrepôt de données (data warehouse)  dans le cloud de Google. Il permet de stocker et d'analyser des données à grande échelle. Il offre un niveau d'utilisation gratuit qui permet de traiter jusqu'à 1 To de données et d'exécuter jusqu'à 100 000 requêtes par mois.

Pour commencer à utiliser BigQuery gratuitement, vous devez créer un compte Google (avoir une adresse gmail). Une fois que vous avez créé votre compte, vous pouvez activer le niveau d'utilisation gratuit de BigQuery.

Pour activer le niveau d'utilisation gratuit, procédez comme suit :

1. Allez sur le site suivant: https://cloud.google.com/bigquery/
2. Dans la console Google Cloud Platform, ouvrez le menu **Menu**, puis sélectionnez **BigQuery**.

![](image/BigQuery_init1.gif)
Vous pouvez utiliser les données d'autres entrepôts de données.

Pour charger des données dans BigQuery, procédez comme suit :

1. Allez dans l’explorateur.
2. Tapez Austin par exemple.
3. Cliquez sur “Recherchez dans tous les projet”
4. Cliquez sur l’étoile de “bigquery-public-dataset” afin que le projet soit épinglé.
![](image/BigQuery_init2.gif)

A présent, vous pouvez voir les données qui sont dans le projet bigquery-public-dataset. Vous pouvez choisir un ensemble de données puis choisir les tables et les interroger.

Pour effectuer une requête dans BigQuery, procédez comme suit :

1. Choisissez une table dans un ensemble de données.
2. Cliquez sur les 3 points verticaux.
3. Cliquez **Interroger**.
4. Entrez votre requête SQL.
5. Cliquez sur le bouton **Exécuter**.
![](image/BigQuery_init3.gif)

Voici un exemple de requête SQL simple :

**SQL**

```
SELECT * 
FROM `bigquery-public-data.austin_bikeshare.bikeshare_stations` 
LIMIT 100

```

Cette requête renvoie les 100 premières ligne de la table bikeshare_stations. Cette table est situé dans l’ensemble de données austin_bikeshare qui est lui même situé dans le projet bigquery-public-data.

Si vous n'avez pas encore exploré la façon dont les tables sont référencées dans BigQuery, voici un rappel de trois concepts clés qui faciliteront votre compréhension de la notation associée à l'appel des tables :

**Projet**

Un projet est un conteneur pour les ensembles de données, les tables, les requêtes, les vues, les flux et d'autres objets BigQuery. Il s'agit de la plus grande unité organisationnelle dans BigQuery.

**Ensemble de données**

Un ensemble de données est une collection de tables qui partagent un ensemble de métadonnées communes. Il s'agit de la plus petite unité organisationnelle dans BigQuery.

**Table**

Une table est une collection de données structurées. Elle est composée de lignes et de colonnes. Chaque ligne représente une instance d'un objet, et chaque colonne représente une propriété de cet objet.

**Référencement d'un ensemble de données, d'un projet ou d'une table**

Pour référencer un ensemble de données, un projet ou une table dans BigQuery, vous pouvez utiliser une notation composée de 3 parties : projet, dataset (ensemble de données), table.

Vous l’écrivez de la manière suivante:`project.dataset.table` .
Par exemple, pour référencer la table `customers` dans l'ensemble de données `my_dataset` du projet `my_project`, vous utiliseriez la notation suivante :

`my_project.my_dataset.customers`

**Exemples**

Voici quelques exemples de référencement d'un ensemble de données, d'un projet ou d'une table dans BigQuery :

- `bigquery-public-data.samples.shakespeare` : référence l'ensemble de données `shakespeare` dans le projet `bigquery-public-data`
- `my_project.my_dataset.customers` : référence la table `customers` dans l'ensemble de données `my_dataset` du projet `my_project`
- `my_dataset.orders` : référence la table `orders` dans l'ensemble de données `my_dataset`

**Remarques**

- Les noms des ensembles de données et des tables ne peuvent contenir que des lettres, des chiffres et le caractère `_`.
- Les noms des projets ne peuvent contenir que des lettres, des chiffres, le caractère `_` et le caractère ``.
- Les noms des ensembles de données, des tables et des projets ne peuvent pas dépasser 128 caractères.

Pour plus d'informations sur l'utilisation de BigQuery, consultez la documentation officielle de BigQuery.