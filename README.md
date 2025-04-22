
# 📊 Prédiction des Coûts Unitaires pour Produits à Moins de 10 €

Ce sous-projet fait partie de l’étude globale de prédiction des prix de revient chez **CMR Group Tunis**.  
Il se concentre exclusivement sur les produits dont le coût unitaire est **inférieur à 10 €**, représentant plus de 50% des articles du dataset.

## 🎯 Objectif

- Construire des modèles de régression robustes pour estimer le `UnitCostToEuro` de produits abordables.
- Comparer plusieurs algorithmes pour sélectionner le plus performant sur cette gamme de prix.

## 🧠 Données utilisées

- Données internes d’achats avec :
  - Produit, Quantité, Société, Relation fournisseur/vente
  - Date physique, Mois d’achat
- Données filtrées sur `UnitCostToEuro < 10`

## 🤖 Modèles testés

- CatBoost Regressor
- LightGBM Regressor
- Random Forest Regressor

## 📊 Comparaison des modèles

| Modèle               | MAE (€/unité) | RMSE (€/unité) | R²       |
|----------------------|---------------|----------------|----------|
| **CatBoost**         | 1.0086 €      | 1.6057 €       | 0.6213   |
| **LightGBM**         | **0.6984 €**  | **1.3241 €**   | **0.7425** |
| **Random Forest**    | 0.8149 €      | 1.4381 €       | 0.6962   |

## ✅ Conclusion

Le modèle **LightGBM** s'est avéré être le plus performant pour les produits à bas coût, offrant la meilleure précision moyenne et expliquant plus de 74% de la variance observée.


