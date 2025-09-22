# elk_stack
## 1. Elasticsearch
### Сначала поднимаю все контейнеры, чтобы проверить, работает ли docker-compose.yml 
### Далее изменяем конфигурационный файл в configs/elasticsearch, в config.yml меняем cluster.name
### После всех этих шагов перезапускаем elasticsearch, не останавливая остальные контейнеры
### docker compose up -d --force-recreate elasticsearch
### Далее проверяем следующей командой, изменилось ли имя curl -X GET 'localhost:9200/_cluster/health?pretty' -u elastic:test
### [cluster_name](image/elasticsearch_config_1.png)
## 2. Kibana

## 3. Logstash

## 4. Filebeat
