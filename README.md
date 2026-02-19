# Analyse-Risque-Marche-VaR-ES
Analyse économétrique du risque de marché (VaR et Expected Shortfall) pour une banque, une assurance et un broker-dealer, réalisée en R et Python à l’aide des méthodes Simulation Historique et GARCH (2007–2023).

# Analyse du Risque de Marché – VaR & Expected Shortfall (2007–2023)

Ce projet d’économétrie financière analyse le risque de marché de trois types d’institutions financières :

- Une banque (établissement de dépôt)
- Une compagnie d’assurance
- Un broker-dealer

L’objectif est d’estimer et comparer leur exposition au risque de marché sur la période 2007–2023 à l’aide de méthodes quantitatives appliquées aux séries temporelles financières.

Le projet a été réalisé en **R et Python**.

---

## Objectifs

- Estimer la **Value-at-Risk (VaR)** aux niveaux 95% et 99%
- Estimer l’**Expected Shortfall (ES)**
- Comparer différentes méthodes d’estimation
- Réaliser des tests de **backtesting**
- Étudier l’évolution du risque durant les grandes crises financières
- Mettre en place un exercice de **forecasting hors échantillon**

---

## Données

- Prix journaliers des actions
- Période : 2007–2023
- Source : Yahoo Finance
- Rendements calculés en log-returns

Analyse statistique préalable :
- Moyenne
- Volatilité
- Asymétrie
- Kurtosis
- Tests de normalité

---

## Méthodologie

### Simulation Historique (Historical Simulation – HS)

- Méthode non paramétrique
- Estimation empirique de la distribution des rendements
- Calcul de la VaR
- Calcul de l’Expected Shortfall conditionnelle

---

### Modélisation GARCH (GARCH(1,1))

- Estimation de la volatilité conditionnelle
- Prise en compte du clustering de volatilité
- Calcul dynamique de la VaR conditionnelle
- Estimation de l’Expected Shortfall sous hypothèse paramétrique

---

### Backtesting

- Test de Kupiec (couverture inconditionnelle)
- Test de Christoffersen (indépendance)
- Analyse du nombre de violations
- Comparaison de performance des modèles

---

### Forecasting

- Méthode rolling window
- Prévisions hors échantillon de la VaR
- Analyse de sensibilité à la taille de la fenêtre d’estimation

---

## Analyse économique

Le projet met en évidence :

- La présence de **queues épaisses (fat tails)**
- Le phénomène de **volatility clustering**
- L’amplification du risque en période de crise
- Les différences structurelles de risque entre banque, assurance et broker-dealer
- La supériorité des modèles conditionnels en période de forte instabilité

---

## Outils utilisés

### Python
- pandas
- numpy
- arch
- scipy
- matplotlib

### R
- rugarch
- quantmod
- PerformanceAnalytics
- tseries

---

## Structure du dépôt

Analyse-Risque-Marche-VaR-ES
│
├── data/ # Données financières
├── python/ # Scripts Python
├── r/ # Scripts R
├── report/ # Rapport académique
├── presentation/ # Slides de présentation
├── README.md

---

## Limites

- Sensibilité au choix de la fenêtre d’estimation
- Hypothèses distributionnelles des modèles paramétriques
- Hypothèse de stationnarité partielle
- Difficulté à modéliser les chocs extrêmes

---

## Concepts mobilisés

- Value-at-Risk (VaR)
- Expected Shortfall (ES)
- Modèles ARCH/GARCH
- Backtesting réglementaire
- Séries temporelles financières
- Clustering de volatilité
- Gestion du risque de marché
