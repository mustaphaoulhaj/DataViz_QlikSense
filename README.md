# La visualisation des ventes sous Qlik Sense

## Les données disponibles 

1. **Table Facture :**
   Contient les informations sur les factures, telles que les numéros de facture, les dates et les montants.

2. **Table Poste_Facture:**
   Comprend les détails des articles associés à chaque facture, comme les quantités et les prix unitaires.
   
3. **Table Magasin:**
   Contient les données sur les magasins, y compris leurs identifiants, leurs adresses et d'autres informations pertinentes.

4. **Table Client**
   Comprend les informations sur les clients, telles que leurs identifiants, leurs noms, leurs genres, leurs adresses, etc.

5. **Table Article :**
   Contient les détails sur les articles vendus, tels que leurs catégories et familles.

6. **Table Objectif :**
   Comprend les objectifs de vente fixés pour chaque magasin, pour chaque année et mois, et pour chaque famille d'article.
   
7. **Table Commercial :**
   Contient les données sur les commerciaux, y compris leurs identifiants, leurs noms, leurs équipes, etc.

## Méthodologie

Pour répondre aux besoins commerciaux, un modèle en étoile est utilisé, reliant les différentes tables de données. Vous pouvez consulter le résultat dans le fichier "Modèle.png" pour voir comment les tables sont connectées.

Astuces pour construire le modèle en étoile :

- Utilisez des tables de mapping pour standardiser les données et faciliter les jointures.
- Utilisez des jointures pour lier les tables principales entre elles.
- Utilisez des concaténations pour combiner des tables de données similaires.
- Utilisez des boucles IF et LOAD pour effectuer des transformations et des calculs sur les données chargées.
- Créez une table "Calendrier" qui facilite l'analyse des données et contient les informations suivantes : Date, Année, Mois, Semaine et Jour de la semaine.
- Utilisez la dimension hiérarchique pour définir la variable qui lie l'article, la catégorie et la famille d'article. Cette dimension hiérarchique permettra une analyse plus détaillée des ventes par article, catégorie et famille d'article.
  
## Définition des KPIs

Après le déploiement du modèle, nous créons les indicateurs qui peuvent être intéressants pour l'étude. Par exemple :

**Chiffre d'Affaires (CA) :** Quantité vendue * Montant unitaire.
**Objectifs de vente :** Objectifs fixés pour chaque magasin, chaque année, mois et famille d'article.
**Performance :** Ratio du chiffre d'affaires réalisé par rapport à l'objectif (CA / Objectif).

Ces KPIs fournissent une vision globale de la performance des ventes et permettent une analyse approfondie des résultats par rapport aux objectifs fixés.

## Types de visualisations

   
1. **Volet de filtre:**
   Utilisez des filtres pour permettre à l'utilisateur de sélectionner l'année, la zone, le type de remise et l'article.

2. **Carte KPI:**
   Créez trois cartes KPI pour visualiser les informations sur le chiffre d'affaires (CA), l'objectif et la performance.

3. **Graphique en courbe:**
   Affichez une courbe pour représenter l'évolution de la performance commerciale en fonction de la date.
   
3. **TCD:**
   Utilisez un tableau croisé dynamique pour visualiser les informations entre les magasins (lignes), les KPIs (valeurs) et les années (colonnes).

5. **Map:**
   Créez une carte géographique des départements français. Utilisez une condition de couleur pour mettre en évidence la performance (vert si la performance dépasse 100%, sinon rouge).
   
7. **Table:**
   Ajoutez une table à la fin de chaque rapport pour afficher les détails des informations, permettant à l'utilisateur d'approfondir son analyse.

## Outil utilisé

Nous utilisons Qlik Cloud (SAAS) pour la visualisation et l'analyse des données.

## Conclusion 

En conclusion, Qlik Sense est un outil puissant de Business Intelligence (BI) qui permet d'analyser et de visualiser les données de manière efficace. Grâce à sa facilité d'utilisation et à ses fonctionnalités avancées, il offre aux utilisateurs la possibilité d'explorer et de comprendre leurs données plus rapidement. Avec Qlik Sense, les entreprises peuvent prendre des décisions plus éclairées et identifier des opportunités de croissance grâce à une analyse approfondie des performances et des tendances.
