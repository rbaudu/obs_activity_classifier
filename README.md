# OBS Activity Classifier

Cette application reçoit et analyse les flux vidéo et audio d'OBS Studio, puis classifie l'activité de la personne dans différentes catégories (endormi, à table, lisant, au téléphone, en conversation, occupé, inactif).

## Structure du projet

- `server/` : Contient le code du serveur principal
  - `capture/` : Module pour la capture des flux OBS
  - `analysis/` : Module pour l'analyse et la classification
  - `database/` : Module pour la gestion des données
  - `api/` : Module pour l'interaction avec les services externes
- `web/` : Contient les ressources pour l'interface web
  - `static/` : Ressources statiques (CSS, JS)
  - `templates/` : Gabarits HTML

## Installation

```bash
pip install -r requirements.txt
```

## Configuration

Modifiez le fichier `server/config.py` pour configurer les paramètres de connexion à OBS, la base de données et les services externes.

## Utilisation

```bash
cd server
python main.py
```

L'application se connectera à OBS, analysera les flux et classifiera l'activité toutes les 5 minutes.
