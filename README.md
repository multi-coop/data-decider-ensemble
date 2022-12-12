# Visualiseur des données

Widget de prévisualisation des données issues de fichiers csv

---

## Résumé

Afin de pouvoir partager et de mettre en valeur toutes les ressources de ce repo il a été proposé de créer un outil numérique de type "widget" : `datami`. En effet un outil de ce type permet de pouvoir intégrer sur des sites tiers (sites de partenaires ou autres) une sélection plus ou moins large de ressources. Cette solution permet à la fois d'éviter aux sites partenaires de "copier-coller" les ressources, d'afficher sur ces sites tiers les ressources toujours à jour, et de permettre aux sites tiers ainsi qu'au site source de gagner en visibilité, en légitimité et en qualité d'information.

L'autre avantage de cette solution est qu'elle n'est déployée qu'une fois, mais que le widget peut être intégré et paramétré/personnalisé sur autant de sites tiers que l'on souhaite... gratuitement.

La solution proposée et réalisée ici s'appuie sur un projet open source porté par la coopérative numérique [**multi**](https://multi.coop) : le projet [Datami](https://datami.multi.coop).

---

## Démo

- Page html de démo : 
- url de démo :
  - DEMO / données Décider ensemble : https://demo-decider-ensemble.netlify.app/

---

### Documentation

Un site dédié à la doucmentation technique de Datami est consultable ici : https://datami-docs.multi.coop

---

## Mini server for local development

A mini server is writen in the `server.py` to serve this folder's files, so we could test and develop locally while running [multi-site-app](https://gitlab.com/multi-coop/multi-site-app)

To install the mini-server :

```sh
pip install --upgrade pip
python3 -m pip install --user virtualenv
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

or

```sh
sh setup.sh
source venv/bin/activate
```

---

### Geocoder

To geocode the dataset :

```sh
python geocoder.py csv/decider-ensemble-ressources.csv -sep , -adress adresse_postale
```

or

```sh
sh run_geocoding.sh
```

The output geocoded file will be generated at `csv/geocoding/geocoded.csv`

---

### Run local server

To run the server on `http://localhost:8805`:

```sh
python server.py
```

or

```sh
sh run_server.sh
```

Files will be locally served on :

- `http://localhost:8805/content/<path:folder_path>/<string:filename>`
- `http://localhost:8805/statics/<path:folder_path>/<string:filename>`

---

## Crédits

| | url |
| :-: | :-: |
| **Décider Ensemble** | https://www.deciderensemble.com |
| **coopérative numérique multi** | https://multi.coop |

---

## Pour aller plus loin

### Datami

Le widget fait partie intégrante du projet [Datami](https://gitlab.com/multi-coop/datami)
