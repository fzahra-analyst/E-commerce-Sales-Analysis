# 📄 Projet d’Analyse des Données E-commerce

📘 Langues disponibles :  
🇬🇧 [English](README.md) | 🇫🇷 Français

## 📌 Aperçu du Projet
Ce projet analyse un large jeu de données provenant d’un site e-commerce brésilien (Olist).  
L’objectif est de comprendre :

- le comportement des clients  
- la performance des ventes  
- les caractéristiques des produits  
- l’efficacité de la livraison  

Le projet couvre :
- Nettoyage des données  
- Feature Engineering  
- Analyse exploratoire (EDA)  
- Analyse clients  
- Analyse de la livraison  
- Analyse produits  
- Analyse géographique  

Ce travail fait partie de mon **portfolio en Data Analysis**.

---

## 🚀 1. Nettoyage des Données

### Étapes principales :
- Suppression des doublons  
- Traitement des valeurs manquantes (produits, avis, géolocalisation…)  
- Correction des types de données  
- Fusion de plusieurs tables en un seul dataset au niveau de la commande  
- Suppression des valeurs invalides concernant la livraison :  
  - temps de livraison négatifs  
  - valeurs extrêmes (> 90 jours)

---

## 🧱 2. Feature Engineering

### Variables temporelles
- `order_year`
- `order_month`
- `order_weekday`

### Variables clients
- `customer_order_count`
- `customer_total_spent`
- `is_repeat_customer`

### Variables liées à la livraison
- `delivery_time_days`
- `delays_days` (livraison réelle – livraison estimée)
- `shipping_ratio` (freight_value / price)

### Variables produits
- `product_volume_cm3`
- `product_density`

Ces nouvelles variables ont permis d’obtenir des analyses plus précises et pertinentes.

---

## 📊 3. Analyse Exploratoire des Données (EDA)

### Insights sur les ventes
- Les ventes sont fortement concentrées dans les grandes villes :  
  **São Paulo**, **Rio de Janeiro**, **Belo Horizonte**
- Catégories les plus vendues :  
  - `bed_bath_table`
  - `health_beauty`
  - `sports_leisure`
- Catégories les plus chères :  
  - `computers_accessories`
  - `watches_gifts`
  - `auto`
- Présence de tendances saisonnières dans les ventes mensuelles  
- La majorité des commandes contiennent **un seul produit**

---

## 👥 4. Analyse Clients
- La plupart des clients achètent **une seule fois**  
- Les clients récurrents représentent une faible part mais génèrent une grande valeur  
- Les “top clients” contribuent fortement au chiffre d’affaires  
- Distribution géographique concentrée dans le Sud et le Sud-Est du Brésil  
- La variable `customer_order_count` confirme une forte proportion d’acheteurs occasionnels

---

## 🚚 5. Analyse de la Livraison
- **Délai moyen de livraison ≈ 13 jours**  
- Certains colis arrivent après la date estimée  
- Plus la distance est grande → plus la livraison est longue  
- Les produits volumineux/poids lourds →  
  - coût de livraison élevé  
  - délais plus longs  
- `shipping_ratio` est le plus élevé pour les catégories volumineuses (meubles, décoration)

---

## 📦 6. Analyse Produits
- Le volume et la densité du produit influencent fortement la livraison  
- Produits volumineux (meubles, bagages, déco) → livraison plus lente  
- Produits de petite taille (beauté, accessoires, jouets) → livraison rapide et peu coûteuse  

---

## 🔍 7. Analyse RFM (si appliquée)
- La majorité des clients sont **Low Frequency – Low Monetary**  
- Les clients à forte valeur sont rares mais essentiels  
- L’analyse de la récence montre des patterns saisonniers  

---

## 🌍 8. Analyse Géographique
- États les plus performants : **SP**, **RJ**, **MG**, **PR**  
- Les régions du Nord et de l’intérieur montrent des délais plus longs (distance + logistique)

---

## 🧩 9. Synthèse Finale des Insights
- ✔ Les ventes se concentrent dans les grandes villes  
- ✔ Les catégories les plus vendues ≠ les catégories les plus chères  
- ✔ Faible fidélité client  
- ✔ Livraison moyenne : 13 jours, dépend fortement de la géographie  
- ✔ Produits volumineux → coûts + délais  
- ✔ Le Feature Engineering a grandement amélioré l’analyse  

---

## 🛠️ 10. Outils & Librairies
- Python  
- Pandas  
- Numpy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  
- (Optionnel) GeoPandas  

---

## 📊 Data Source

Ce projet est basé sur le **jeu de données public brésilien de e-commerce (Olist)**, qui contient des données commerciales réelles provenant de plusieurs vendeurs et clients.

Le jeu de données original comprend :
- Commandes
- Clients
- Produits
- Paiements
- Avis
- Vendeurs
- Données de géolocalisation

Afin d’optimiser l’analyse et les performances, les données brutes ont été nettoyées, transformées et enrichies pour créer de nouveaux jeux de données utilisés tout au long de ce projet.

🔗 Source du jeu de données :  
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce


## 📁 Strecture de Projet

E-commerce-Sales-Analysis/
│
├── data/
│   ├── cleaned_dataset.csv
│   ├── engineered_dataset.csv
│   ├── orders_full.csv
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_customer_analysis.ipynb
│   ├── 04_rfm_analysis.ipynb
│   ├── 05_geographical_analysis.ipynb
│
├── results/
│   ├── customer_summary.csv
│   ├── rfm_segments.csv
│   └── graphs/
│       ├── 1.png
│       ├── 2.png
│       ├── 3.png
│       └── ...
│
├── src/
│   ├── data_cleaning.py
│   ├── eda.py
│   └── utils.py
│
├── README.md
└── requirements.txt


---

## 🎯 12. Conclusion
Ce projet présente un workflow complet et professionnel d’analyse de données e-commerce.  
Il met en avant le comportement client, les tendances de vente, l’impact logistique et les caractéristiques produits grâce à un Feature Engineering avancé.

---

## 💼 Auteur
**Fatima Zahra**
Analyste
