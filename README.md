# elk_stack
## 1. Elasticsearch
### Сначала поднимаю все контейнеры, чтобы проверить, работает ли docker-compose.yml 
### Далее изменяем конфигурационный файл в configs/elasticsearch, в config.yml меняем cluster.name
### После всех этих шагов перезапускаем elasticsearch, не останавливая остальные контейнеры
### docker compose up -d --force-recreate elasticsearch
### Далее проверяем следующей командой, изменилось ли имя curl -X GET 'localhost:9200/_cluster/health?pretty' -u elastic:test
### [cluster_name](image/elasticsearch_config_1.png)
## 2. Kibana
### Сначала авторизовался в http://127.0.0.1:5601/app/home#/ используя логин и пароль из config/kibana/config.yml 
### Далее войдя на http://127.0.0.1:5601/app/dev_tools#/console  выполнил GET /_cluster/health?pretty
### [kibana](image/kibana_2.png)
## 3. Logstash
### [nginx-access](image/logstash_-1.png)
### [index-pattern](image/logstash_0.png)
### [created-index-pattern](image/logstash_1.png)
### [discover](image/logstash_2.png)
### [last_logs_kibana](image/last_logs_kibana.png)
## 4. Filebeat
