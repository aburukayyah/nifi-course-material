# Airports Dataflow Usecase

A complex nifi dataflow which can pull data from `ourairports.com`, performs data (transformation/enrichment/filtering) and routes to appropriate destinations such as Hadoop, Kafka, Postgres, Elasticsearch ( for data insights & visualization in Kibana ).

## Deploy ecosystem stack

Clone the repository and checkout usecase

```shell
git clone https://github.com/naddym/nifi-course.git
cd usecase
```

Deploy stack with docker-compose

```shell
sudo docker-compose up
```

## Sample JSON source data

```json
[
    {
        "id": 40814,
        "ident": "SK-377",
        "type": "small_airport",
        "name": "Barbosa Airport",
        "latitude_deg": 5.943333,
        "longitude_deg": -73.611389,
        "elevation_ft": 5176,
        "continent": "SA",
        "iso_country": "CO",
        "iso_region": "CO-SAN",
        "municipality": "Barbosa",
        "scheduled_service": "no",
        "gps_code": null,
        "iata_code": null,
        "local_code": "BSA",
        "home_link": null,
        "wikipedia_link": null,
        "keywords": null
    },
    {
        "id": 342103,
        "ident": "ZYXW",
        "type": "closed",
        "name": "Mt Logan Airstrip",
        "latitude_deg": 60.79299,
        "longitude_deg": -138.694027,
        "elevation_ft": 1997,
        "continent": "NA",
        "iso_country": "CA",
        "iso_region": "CA-YT",
        "municipality": "Unorganized Yukon",
        "scheduled_service": "no",
        "gps_code": "ZYXW",
        "iata_code": "ZYA",
        "local_code": "YK90",
        "home_link": null,
        "wikipedia_link": null,
        "keywords": null
    },
    {
        "id": 317861,
        "ident": "ZYYK",
        "type": "medium_airport",
        "name": "Yingkou Lanqi Airport",
        "latitude_deg": 40.542524,
        "longitude_deg": 122.3586,
        "elevation_ft": null,
        "continent": "AS",
        "iso_country": "CN",
        "iso_region": "CN-21",
        "municipality": "Laobian, Yingkou",
        "scheduled_service": "yes",
        "gps_code": "ZYYK",
        "iata_code": "YKH",
        "local_code": null,
        "home_link": null,
        "wikipedia_link": "https://en.wikipedia.org/wiki/Yingkou_Lanqi_Airport",
        "keywords": null
    },
    {
        "id": 6099,
        "ident": "SKAR",
        "type": "medium_airport",
        "name": "El Eden Airport",
        "latitude_deg": 4.45278,
        "longitude_deg": -75.7664,
        "elevation_ft": 3990,
        "continent": "SA",
        "iso_country": "CO",
        "iso_region": "CO-QUI",
        "municipality": "Armenia",
        "scheduled_service": "yes",
        "gps_code": "SKAR",
        "iata_code": "AXM",
        "local_code": "AXM",
        "home_link": null,
        "wikipedia_link": "https://en.wikipedia.org/wiki/El_Ed%C3%A9n_Airport",
        "keywords": null
    }
]
```

## Changes to Containers

Following changes are needed by dataflow to store airports data.

### Hadoop

Get into Hadoop's namenode container

```shell
sudo docker exec -it namenode bash

# listing existing files in hadoop
hdfs dfs -ls /

# creating /user/nifi directory for storing airports data
hdfs dfs -mkdir -p /user/nifi
```

### Kafka

Get into Kafka container

```shell
sudo docker exec -it kafka bash

# cd into user directory of kafka
cd /opt/kafka

# create topics
# closed topic
./bin/kafka-topics.sh --bootstrap-server kafka:9092 --create --topic closed --replication-factor 1 --partitions 1
# heliport topic
./bin/kafka-topics.sh --bootstrap-server kafka:9092 --create --topic heliport --replication-factor 1 --partitions 1
# large_airport topic
./bin/kafka-topics.sh --bootstrap-server kafka:9092 --create --topic large_airport --replication-factor 1 --partitions 1
# medium_airport topic
./bin/kafka-topics.sh --bootstrap-server kafka:9092 --create --topic medium_airport --replication-factor 1 --partitions 1
# seaplane_base topic
./bin/kafka-topics.sh --bootstrap-server kafka:9092 --create --topic seaplane_base --replication-factor 1 --partitions 1
# small_airport topic
./bin/kafka-topics.sh --bootstrap-server kafka:9092 --create --topic small_airport --replication-factor 1 --partitions 1
# ballonport topic
./bin/kafka-topics.sh --bootstrap-server kafka:9092 --create --topic ballonport --replication-factor 1 --partitions 1
```
### Postgres DB

Get into Postgres container

```shell
sudo docker exec -it postgres bash

# connecting to postgres
psql -U postgres


# creating table airports for storing finalized data from nifi
CREATE TABLE AIRPORTS (
    ID INT PRIMARY KEY NOT NULL,
    IDENT TEXT NOT NULL,
    TYPE TEXT NOT NULL,
    NAME TEXT NOT NULL,
    LATITUDE_DEG DECIMAL,
    LONGITUDE_DEG DECIMAL,
    ELEVATION_FT INT,
    CONTINENT TEXT,
    ISO_COUNTRY TEXT,
    ISO_REGISON TEXT,
    MUNICIPALITY TEXT,
    SCHEDULED_SERVICE TEXT,
    GPS_CODE TEXT,
    IATA_CODE TEXT,
    LOCAL_CODE TEXT,
    HOME_LINK TEXT,
    KEYWORDS TEXT,
    FREQUENCY_MHZ TEXT
);
```