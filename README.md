# Introduction à l'hydrologie computationnelle

Ce dépôt regroupe plusieurs notebooks et scripts Python destinés à illustrer les principales étapes de l'exploitation de données hydrologiques. 
Il constitue **pour moi** une introduction pratique à l'hydrologie computationnelle, depuis la manipulation de données géographiques jusqu'à l'analyse de séries temporelles hydrométéorologiques et la prise en compte des incertitudes.
**Il ne s'agit pas d'un document de réference, mais plutôt d'un projet qui me sert a en apprendre plus sur l'hydrologie**

L'ensemble des exemples est développé en Python et s'appuie sur des bibliothèques couramment utilisées en sciences de l'environnement (NumPy, Pandas, GeoPandas, Matplotlib, SciPy, etc.).

## Contenu

### 1. Visualisation de données géographiques

**`SIG visualisation/visualisation_SIG_data.ipynb`**

Ce notebook introduit la manipulation de données issues de Systèmes d'Information Géographique (SIG) appliquées à l'hydrologie. Il présente notamment :

* la lecture de données HydroRIVERS ;
* la représentation des réseaux hydrographiques avec GeoPandas ;
* la manipulation des géométries de tronçons de rivière ;
* l'identification des connexions entre tronçons ;
* la sélection d'un bassin versant et la visualisation de ses caractéristiques.

Ce notebook constitue une première approche de la géomatique appliquée aux réseaux hydrographiques.

---

### 2. Exploration de données hydrométéorologiques

**`hydrometrie/notebooks/01_data_exploration.ipynb`**

Ce notebook présente différentes méthodes d'exploration de données hydrologiques et météorologiques :

* chargement de séries temporelles hydrométriques ;
* visualisation des hauteurs d'eau ;
* téléchargement et exploitation de données ERA5 ;
* analyse des précipitations et des températures ;
* étude des variations saisonnières ;
* régressions linéaires simples ;
* préparation des données pour des analyses statistiques ultérieures.

---

### 3. Téléchargement des données ERA5

**`hydrometrie/scripts/download_era5.py`**

Ce script automatise le téléchargement de données météorologiques issues de la réanalyse ERA5 via l'API du Copernicus Climate Data Store.

Il permet notamment de récupérer :

* les précipitations ;
* les températures ;
* d'autres variables météorologiques exploitables dans des études hydrologiques.

---

### 4. Modélisation des incertitudes

**`incertitude/uncertainty.ipynb`**

Ce notebook introduit la notion d'incertitude dans les données hydrologiques.

À travers un modèle simplifié de réseau hydrographique, il présente :

* la représentation probabiliste des débits ;
* la propagation des incertitudes dans un réseau ;
* l'influence des confluences et des exutoires ;
* la prise en compte de corrélations spatiales entre tronçons ;
* l'ajustement de distributions statistiques adaptées aux débits.

L'objectif est de montrer comment intégrer explicitement l'incertitude dans les analyses hydrologiques.

## Dépendances principales

Les notebooks utilisent notamment :

* Python ≥ 3.10
* NumPy
* Pandas
* SciPy
* Matplotlib
* GeoPandas
* Shapely
* Xarray
* NetCDF4
* cdsapi (pour ERA5)

## Licence

Ce dépôt est destiné à un usage pédagogique et scientifique.
