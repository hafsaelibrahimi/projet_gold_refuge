# Projet Python pour la Data Science 2024-2025
# L'or et les cryptomonnaies : des valeurs refuges ? 

Auteurs : *El Ibrahimi Hafsa, Legrée-Hagbarth Camille*

# Sujet :
Dans de nombreux articles parus dans la presse ces derniers mois, les cryptomonnaies sont décrites comme de nouvelles valeurs refuges. Toutefois, les cryptommonnaies sont considérés dans la littérature économique comme une mauvaise réserve de valeur du fait de leur forte volatilité et de l'absence de garantie de leur valeur nominale par une instance publique ou privée. Par exemple, en août 2016, Bitfinex a été victime d’un piratage informatique impliquant la perte de 120 000 bitcoins. Ainsi, les cryptomonnaies apparaissent être des actifs financiers particulièrement risqués et peu fiables. Au contraire, l'or est un actif financier traditionnellement considéré comme une valeur refuge, dans la mesure où il joue un rôle de réserve de valeur de long terme en période de crise. Ce projet a pour but d'étudier si l'or et les cryptomonnaies se comportent comme des valeurs refuges à l'aide d'une approche scientifique à la fois descriptive et explicative. 

# Définition :
On définit une valeur refuge comme un actif particulièrement demandé lors des périodes de crises parce qu'il est réputé pour conserver sa valeur dans le temps malgré l'instabilité du contexte économique et financier. Ce type d'actif remplit les critères suivants :
- Il dégage des rendements non corrélés à ceux des actions en période de crise
- Il joue un rôle de couverture en dégageant des rendements non corrélés à ceux des actions sur le long terme.  

# Problématique :
L'or et les cryptomonnaies se comportent-elles comme des valeurs refuges ? 

# Modèle utilisé :
Nous nous sommes appuyées principalement sur le modèle ARMA-GARCH traditionnellement utilisé pour des séries temporelles stationnaires. Ce choix de modèle s'appuie sur les travaux de Virginie Coudert et Hélène Raymond. Leur article étant daté de 2012 et n'étudiant que l'or, nous souhaitions :
- Utiliser ce modèle avec des données allant de 2000 à 2024, couvrant ainsi également la période la plus récente.
- Étendre ce modèle à l'étude des cryptomonnaies.

# Données utilisées :
- API générée à partir d'Alpha Vantage pour télécharger des données boursières historiques mensuelles de grandes entreprises technologiques entre 2000 et 2024
- Bases de données mensuelles Yahoo Finance sur l'Or, le Bitcoin, l'Ethereum et l'indice S&P 500 entre 2000 et 2024

# Navigation au sein du projet :
Il suffit d'exécuter successivement les cellules du notebook "main.ipynb". 

# Bibliothèques à installer
     !pip install yfinance
     !pip install arch

# Bibliothèques utilisées
     import requests
     import pandas as pd
     import os
     import yfinance as yf
     import numpy as np
     import matplotlib.pyplot as plt
     import seaborn as sns
     from arch import arch_model
     from scipy.optimize import minimize
     from statsmodels.api import OLS, add_constant
     
# Conseils d'utilisation 
L'utilisation de l'API est limitée à 25 requêtes par jour. Il est donc conseillé d'exécuter la cellule important les données issues de l'API le moins possible.

# Sources 
- Coudert V., Raymond H. (2012), « L'or est-il une valeur refuge pendant les récessions et les crises boursières ? », Revue économique
- Baur D.G., McDermott T.K (2010), « Is gold a safe haven? International evidence », Journal of Banking and Finance

