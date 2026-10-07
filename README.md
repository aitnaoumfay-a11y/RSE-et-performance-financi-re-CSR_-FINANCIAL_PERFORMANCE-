# RSE et Performance Financière — BVC 2014–2023

Code R Markdown du mémoire de Master Finance Appliquée (Finance Durable), FSJES, Université Cadi Ayyad, Marrakech.

**Auteure :** Fadoua Ait Naoum
**Encadrants :** Pr. Salah Eddine Kartoubi · Pr. Zineb Elhachimi

## Objet

Analyse économétrique sur données de panel de la relation entre la Responsabilité Sociétale des Entreprises (RSE) et la performance financière de 30 sociétés cotées à la Bourse des Valeurs de Casablanca, sur la période 2014–2023 (300 observations firme-année).

## Variables

| Type | Variables |
|---|---|
| Dépendantes | ROA, ROE, Q de Tobin |
| Explicative | Score RSE (26 items, 0–100) |
| Contrôles | Taille (ln actifs), Endettement, Label RSE CGEM (0/1), Post-AMMC (circulaire 03/19), COVID (2020) |

## Hypothèses testées

* **H1** : la RSE améliore la performance financière
* **H2** : la performance passée favorise l'engagement RSE (slack resources)
* **H3** : la taille modère la relation RSE–performance

## Méthodologie

1. Statistiques descriptives et décomposition between / within
2. Corrélations et VIF
3. Tests de spécification (Fisher, Breusch-Pagan, Hausman)
4. Diagnostics (autocorrélation, hétéroscédasticité)
5. Test d'endogénéité de Wu-Hausman (diagnostic)
6. Stationnarité (IPS)
7. Modèles à effets fixes avec erreurs standards robustes clusterisées par firme
8. Robustesse : effets aléatoires, sous-périodes pré / post AMMC

## Utilisation

Ouvrir `RSE_performance_BVC.Rmd` dans RStudio puis cliquer sur **Knit** (sortie HTML). Les packages manquants s'installent automatiquement au premier lancement.

Packages : plm, lmtest, sandwich, car, stargazer, ggplot2, ggcorrplot, dplyr, tidyr, knitr, kableExtra, scales, tseries, gridExtra.
