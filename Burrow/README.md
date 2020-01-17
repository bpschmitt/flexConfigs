# Burrow New Relic Flex Config

This Flex config creates the following event types:

## Events

| Name | Description |
| ------ | ----------- |
| kafkaConsumerGroupLagSample   | test description |
| kafkaPartitionSample | test description |

## Burrow API Response

Performs a GET against the Burrow API:
[https://github.com/linkedin/Burrow/wiki/http-request-consumer-group-status](https://github.com/linkedin/Burrow/wiki/http-request-consumer-group-status)

Burrow Sample JSON Output:
```
{
  "error": false,
  "message": "consumer group status returned",
  "status": {
    "cluster": "clustername",
    "group": "groupname",
    "status": "WARN",
    "complete": 1.0,
    "maxlag": {
      "complete": 1,
      "current_lag": 0,
      "end": {
        "lag": 25,
        "offset": 2542,
        "timestamp": 1511780580382
      },
      "owner": "",
      "partition": 0,
      "start": {
        "lag": 20,
        "offset": 2526,
        "timestamp": 1511200836090
      },
      "status": "WARN",
      "topic": "topicA"
    },
    "partitions": [
      {
        "complete": 1,
        "current_lag": 0,
        "end": {
          "lag": 25,
          "offset": 2542,
          "timestamp": 1511780580382
        },
        "owner": "",
        "partition": 0,
        "start": {
          "lag": 20,
          "offset": 2526,
          "timestamp": 1511200836090
        },
        "status": "WARN",
        "topic": "topicA"
      }
      ...
    ]
  },
  "request": {
    "url": "/v3/kafka/clustername/consumer/groupname/status",
    "host": "responding.host.example.com",
  }
}   
```


