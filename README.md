# elasticsearch2

docker-compose.yml

```
version: '3.2'
services:
  elasticsearch:
    image: layatai/elasticsearch2
    environment:
      - "ES_JAVA_OPTS=-Xms512m -Xmx512m"
    ports:
      - "9300:9300"
    ulimits:
      memlock:
        soft: -1
        hard: -1
    volumes:
      - data_es:/usr/share/elasticsearch/data
