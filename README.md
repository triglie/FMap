<h1 align="center">fmap (Frequence Mapper)</h1>
<p align="center">(🇮🇹) Monitora la qualità della ricezione dei segnali radio nelle province siciliane. </p>
<p align="center">(🇺🇸) Monitors the quality of radio signal reception in the Sicilian provinces. </p>



## ⚡ Quickstart

```shell
$ git clone (this repo)
$ cd fmap
$ docker-compose up -d
```



## 📊 Data flow 

<p align="center">
  <img src="./docs/assets/data-flow-card.png" alt="data-flow" width=500/>
</p>



### PI/frequence - Station Conversion maps

 Frequency - StationName (province) maps are stored in `fmdata` directory: 

| Province | File path                                     |
| -------- | --------------------------------------------- |
| Catania  | kafkastream/fmdata/fm-station-map-catania.csv |
| Messina  | kafkastream/fmdata/fm-station-map-messina.csv |
| Palermo  | kafkastream/fmdata/fm-station-map-palermo.csv |

> Any other province outside of this three uses the csv of the nearest province. 

Frequency - PI - StationName map is stored in `fmdata` directory: 

| State  | File path                                      |
| ------ | ---------------------------------------------- |
| Italia | kafkastream/fmdata/complete-pi-station-map.csv |



## Useful links 

| Container     | URL                                             | Description                           |
| ------------- | ----------------------------------------------- | ------------------------------------- |
| kafkaserver   | http://localhost:8080                           | Open kafka UI to monitor kafka server |
| connect       | http://localhost:8083                           | Kafka Connect base URL                |
| connect       | http://localhost:8083/connectors                | Kafka Connect connectors list         |
| elasticsearch | http://localhost:9200/                          | ElasticSearch base URL                |
| elasticsearch | http://localhost:9200/rds-signal-output/_search | ElasticSearch index content           |



## Building kafkastream apps 

[...]



## Authors 

* [Luigi Seminara](https://github.com/Gigi-G)
* [Lemuel Puglisi](https://github.com/LemuelPuglisi) 

