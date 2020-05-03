# HELK and APT29 Day 1 & Day2

## Pre-requirements

* Install Kafkacat 1.5+
  * Reference: https://github.com/edenhill/kafkacat#install
* git clone https://github.com/Cyb3rWard0g/HELK
* git clone https://github.com/OTRF/detection-hackathon-apt29 (same VM or local host as HELK)

## Send Data to HELK

* cd detection-hackathon-apt29/datasets/day1
* decompress files

```
unzip apt29_evals_day1_manual.zip
```

* Use Kafkacat to send the data over to the kafka broker deployed by HELK

```
kafkacat -b 127.0.0.1:9092 -t winlogbeat -P -l apt29_evals_day1_manual_2020-05-01225525.json
```


