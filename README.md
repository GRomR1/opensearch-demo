# OpenSearch Demo

Тестовый проект для запуска стенда состоящего из
- opensearch
- opensearch-dashboards
- logstash

Необходим для демонстрации работы сбора и обработки логов через logstash, их сохранения в OpenSearch и последующей работы с логами в OpenSearch Dashboards.

Проект содержит датасет из 100k запросов пользователей поиска из открытой базы AOL [(AOL User Session Collection 500K)](https://www.cim.mcgill.ca/~dudek/206/Logs/AOL-user-ct-collection/U500k_README.txt). Этот же датасет используется в [бенчмарке](https://github.com/opensearch-project/opensearch-benchmark-workloads/tree/main/percolator) opensearch.

Для подготовки датасета использовалась следующая команда

```
sed -n '2,100001p' sample-data/user-ct-test-collection-02.txt > sample-data/user-ct-test-collection.txt
```

# URLs

Ниже ссылки для прямого доступа к логам AOL в OpenSearch Dashboards запущенный локально:

- [Discover AOL logs](http://localhost:5601/app/discover/#/?_g=(time:(from:'2006-02-28T20:00:00.000Z',to:'2006-06-01T20:00:00.000Z')))
  > логин: admin, пароль: admin