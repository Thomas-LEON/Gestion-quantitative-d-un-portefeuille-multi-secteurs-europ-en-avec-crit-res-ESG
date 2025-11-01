# Gestion Quantitative de Portefeuille (Backtesting & Optimisation)

## Description

Ce projet fournit un framework d'analyse quantitative en Python pour backtester des stratégies de trading et optimiser des portefeuilles. L'analyse se base sur des données de marché (collectées via `yfinance`) et une stratégie technique multi-indicateurs.

Le notebook principal (`Gestion_Quantitative_Finale.ipynb`) permet de :
1.  Charger et traiter les données d'actifs de plusieurs portefeuilles (ex: EU et US).
2.  Analyser les corrélations entre les actifs via une heatmap.
3.  Backtester une stratégie basée sur 6 indicateurs techniques (Moyennes Mobiles, RSI, MACD, ATR, etc.).
4.  **Analyser les Seuils :** Identifier la combinaison de signaux la plus performante (de 1/6 à 6/6) en analysant le PNL total, le rendement moyen par trade et le "win rate".
5.  **Visualiser le Backtest :** Générer des graphiques détaillés pour chaque actif, incluant les signaux d'achat/vente, la courbe de PNL (€/$) et le Max Drawdown de la stratégie.
6.  **Optimiser (Markowitz) :** Calculer et afficher la frontière efficiente pour trouver les portefeuilles à variance minimale et à ratio de Sharpe maximal.

## Structure du Projet

* `Gestion_Quantitative_Finale.ipynb`: Le notebook Jupyter principal contenant tout le code, les analyses et les visualisations.
* `data_*.csv`: (Généré) Fichiers de données brutes téléchargés depuis Yahoo Finance.
* `*.pkl`: (Généré) Fichiers de données traitées (indicateurs calculés) pour un chargement rapide.

## Prérequis

* Python 3.8+
* Jupyter Notebook ou Jupyter Lab
* Bibliothèques :
    * `pandas`
    * `numpy`
    * `yfinance`
    * `matplotlib`
    * `seaborn`
    * `scipy`
    * `tqdm`

## Utilisation

1.  **Cloner le dépôt** (en utilisant votre URL de dépôt) :
    ```bash
    git clone [https://github.com/Thomas-LEON/Gestion-quantitative-d-un-portefeuille-multi-secteurs-europ-en-avec-crit-res-ESG](https://github.com/Thomas-LEON/Gestion-quantitative-d-un-portefeuille-multi-secteurs-europ-en-avec-crit-res-ESG)
    cd Gestion-quantitative-d-un-portefeuille-multi-secteurs-europ-en-avec-crit-res-ESG
    ```

2.  **Installer les dépendances** (il est recommandé d'utiliser un environnement virtuel) :
    ```bash
    pip install pandas numpy yfinance matplotlib seaborn scipy tqdm jupyter
    ```

3.  **Modifier le chemin de sortie (OBLIGATOIRE)** :
    * Ouvrez le notebook `Gestion_Quantitative_Finale.ipynb`.
    * Dans la **Cellule 3 (Paramètres Globaux)**, modifiez la variable `OUTPUT_DIR` pour qu'elle pointe vers le dossier où vous souhaitez sauvegarder les données sur *votre* ordinateur.

    ```python
    # !! Modifier ce chemin pour correspondre à votre configuration
    OUTPUT_DIR = "C:/Chemin/Vers/Votre/Dossier/Projet/"
    ```

4.  **Lancer Jupyter et exécuter le notebook** :
    ```bash
    jupyter notebook Gestion_Quantitative_Finale.ipynb
    ```
    * Exécutez les cellules séquentiellement pour voir les analyses s'afficher.
