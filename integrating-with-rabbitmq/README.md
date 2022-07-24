     
       _   _ _ _____ _            _ _   _       ____       _     _     _ _   __  __  ___  
      | \ | (_)  ___(_) __      _(_) |_| |__   |  _ \ __ _| |__ | |__ (_) |_|  \/  |/ _ \ 
      |  \| | | |_  | | \ \ /\ / / | __| '_ \  | |_) / _` | '_ \| '_ \| | __| |\/| | | | |
      | |\  | |  _| | |  \ V  V /| | |_| | | | |  _ < (_| | |_) | |_) | | |_| |  | | |_| |
      |_| \_|_|_|   |_|   \_/\_/ |_|\__|_| |_| |_| \_\__,_|_.__/|_.__/|_|\__|_|  |_|\__\_\
                                                                                     

This example demonstrates how to connect from NiFi to RabbitMQ

## Deploy ecosystem stack

Clone the repository and checkout `integrating-with-rabbitmq` directory

```shell
git clone https://github.com/naddym/nifi-course.git
cd integration-with-rabbitmq
```

## Creating queue in RabbitMQ container

Step 1: Exec into the container

```shell
$ > docker exec -it rabbitmq bash
```

Step 2: Listing existing queue (it should be empty)

```shell
$ > rabbitmqctl list_queues
```

Step 3: Create queue with name `nifi`.

```shell
$ > rabbitmqadmin -u rabbitmq -p rabbitmq declare queue name=nifi
```

***Note that:*** `-u` is the flag for accepting username and `-p` for accepting password

## Deploying NiFi-RabbitMQ stack

Step 1: Clone the material if not already done

```shell
$ > git clone https://github.com/naddym/nifi-course.git
$ > cd integrating-with-rabbitmq
```

Step 2: Deploy NiFi-RabbitMQ stack with docker-compose

```shell
$ > sudo docker-compose up
```

## Configuring Processors

***GenerateFlowFile*** 

Configuring `GenerateFLowFile` processor is simple. Just copy below data to `Custom Text` property of GenerateFlowFile Processor

```json
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
  }
```

***PublishAMQP***

| Name | Value |
| ---- | ----- |
| Routing Key | nifi |
| Host Name | rabbitmq |
| port | 5672 |
| User Name | rabbitmq |
| Password | rabbitmq |


***ConsumeAMQP***

| Name | Value |
| ---- | ----- |
| Queue | nifi |
| Host Name | rabbitmq |
| port | 5672 |
| User Name | rabbitmq |
| Password | rabbitmq |