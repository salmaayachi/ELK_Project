# ELK Stack avec Docker Compose
Ce projet met en place une stack ELK (Elasticsearch, Logstash, Kibana) en environnement Docker, accompagnée d'un générateur de logs personnalisé pour simuler des flux de données.

##📦 Services inclus
- Elasticsearch : moteur de recherche et d'analyse.
- Kibana : interface web pour visualiser les données d'Elasticsearch.
- Logstash : pipeline de traitement des logs.
- Log Generator : service personnalisé générant des logs pour alimenter Logstash.​


## 🚀 Démarrage rapide
Assurez-vous d'avoir Docker et Docker Compose installés.​

Clonez ce dépôt :​
```
git clone https://github.com/salmaayachi/ELK_Project.git
```
```
cd ELK_Project
```
```
docker compose up -d
```
Accédez à Kibana via http://localhost:5601.​

## ⚙️ Configuration
- Elasticsearch :
Port : 9200
Mode : single-node
Sécurité : désactivée (xpack.security.enabled=false)​
- Kibana :
Port : 5601
Connecté à Elasticsearch via http://elasticsearch:9200​
- Logstash :
Ports : 5044 (input), 9600 (API monitoring)
Pipelines configurés dans ./logstash/pipeline​
- Log Generator :
Construit à partir du Dockerfile situé dans ./logGenerator
Monte le volume ./logGenerator dans le conteneur​



