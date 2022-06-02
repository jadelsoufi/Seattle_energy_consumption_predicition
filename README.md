# Seattle_energy_consumption_prediction
Créer un algorithme destiné à estimer la consommation énergétique et l'émission de CO2 de la ville de Seattle.
Les prédictions seront annuelles, l'objectif étant qu'elles soient assez précises pour ne pas avoir recours aux relevés de consommation de chaque immeuble (méthode trop couteuse).

## Présentation

Vous travaillez pour la ville de Seattle. Pour atteindre son objectif de ville neutre en émissions de carbone en 2050, votre équipe s’intéresse de près à la consommation et aux émissions des bâtiments non destinés à l’habitation.

Des relevés minutieux ont été effectués par les agents de la ville en 2016. Voici les données et leur source. Cependant, ces relevés sont coûteux à obtenir, et à partir de ceux déjà réalisés, vous voulez tenter de prédire les émissions de CO2 et la consommation totale d’énergie de bâtiments pour lesquels elles n’ont pas encore été mesurées.

## Base de données

Le dataset de la consommation energétique de 2016 est disponible via ce lien:
https://data.seattle.gov/dataset/2016-Building-Energy-Benchmarking/2bpz-gwpy

## Traitement et nettoyage de la base de données :


- Suppression des colonnes non pertinentes
- Gestion des nans
- Gestions des valeurs aberrantes
- Transformation des data leaks (ex: consommation par type de carburant) en variables proportionnelles (pourcentage de consommation)
- Suppression des outliers

## DataViz :
### Matrice de corrélation :
![image](https://user-images.githubusercontent.com/76253068/170478625-24522ca8-3009-4b59-a2eb-14621bd1f161.png)

### Analyse Anova:
### Corrélation par rapport à la variable cible de consommation d'énergie:
![image](https://user-images.githubusercontent.com/76253068/170478945-ffe229df-182c-4d10-8f72-ad6a49acaca8.png)

### Corrélation par rapport à la variable cible d'émission de CO2:

![image](https://user-images.githubusercontent.com/76253068/170479023-3b11ccac-1f4b-43a4-b8d3-db80b64c1068.png)

## Modélisation (consommation énergétique)
### Transformation logarithmiques
![image](https://user-images.githubusercontent.com/76253068/170479136-513018e0-c59f-4efa-a231-9c5df6c0bac5.png)

### Exemple de gridsearchCV:

![image](https://user-images.githubusercontent.com/76253068/170479483-86362a09-2597-471b-9f95-abe5251b7f58.png)

### Résultats :

![image](https://user-images.githubusercontent.com/76253068/170479557-5b251a9a-5469-4a36-8e4b-89164436acb1.png)

![image](https://user-images.githubusercontent.com/76253068/170479605-6029d048-f7e6-4cbc-9918-cf4f0c2c1b87.png)

## Modélisation (CO2)

### Résultats(CO2 sans la variable ESS)

![image](https://user-images.githubusercontent.com/76253068/170479839-3b62a838-19da-4b8a-821e-03ebb22688a6.png)

![image](https://user-images.githubusercontent.com/76253068/170479887-e621c880-7de5-4bc7-a83b-58b2f9b01fa0.png)

### Résultats(CO2 avec la variable ESS)

![image](https://user-images.githubusercontent.com/76253068/170480109-e818d6b7-cded-4dde-a42c-ee488badd5ca.png)

![image](https://user-images.githubusercontent.com/76253068/170480141-68fb904d-afc2-4962-8b37-c117bea0dc6c.png)

## Synthèse

![image](https://user-images.githubusercontent.com/76253068/170480191-335cb050-1972-47e0-9393-5229b7ba9e5b.png)




