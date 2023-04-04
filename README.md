# Docker_grafana
L'objectif de ce projet est de faire un docker compose avec Grafana, Prometheus, cAdvisor (prometheus), Node Exporter (prometheus),Prom Gateway + Autre container serverless dans notre cas nous avons choisir openfaas.

Etapes pour la mise en place de ce projet :

Extraire les fichiers dans un dossier qui doit contenir les fichiers suivants : 

Le fichier docker-compose.yml lance les services suivants : Grafana, Prometheus, cAdvisor, Node Exporter,Prom Gateway, Autre container serverless(openfaas).
-docker-compose.yml

#définit la configuration de démarrage de grafana dans docker compose
-grafana_config.ini

#définit l'endroit où le service grafana peut trouver les données du service prometheus 
-grafana_datasources.yml

#définit la configuration de Prometheus
-prometheus.yml



#lancement du docker compose

Acceder au dossier créer via l'invite de commande lancez la commande suivante : docker-compose up -d

#Accès aux interfaces

une fois les services lancés :
  
- Pour accéder à Grafana ouvrez un navigateur et saisissez l'URL : http://localhost:3000.

- Saisissez le nom d'utilisateur et le mot de passe par défaut (admin / admin).

- Pour accéder à Grafana ouvrez un navigateur et saisissez l'URL : http://prometheus:9090

#monitoring de node-exporter via Grafana

- Dans le menu de gauche de Grafana, déplacez votre curseur sur "Dashboard" puis cliquez sur "Import".
- Dans la barre "Import via grafana.com", entrez l'ID : 1860 ( Cela permet d'importer un dashboard Node-exporter-full pré configuré)
- Puis cliquez sur le bouton Load
  

Remarques : 

- Vous trouverez dans le dossier images les captures de la configuration de grafana
- Fichier Json Node Exporter : c'est le fichier JSON pour le tableau de bord Prometheus pour Grafana que nous avons exporté 
  

