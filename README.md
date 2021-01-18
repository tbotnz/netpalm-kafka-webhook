# netpalm-kafka-webhook
simple kafka webhook example for netpalm

### installing the webhook

- add ```kafka-python``` to your ```netpalm/worker_requirements.txt```
- load ```kafka.py``` to ```netpalm/backend/plugins/extensibles/custom_webhooks/```
- add compose file ```docker-compose-with-kafka.yml```
- rebuild container


### using the webhook

```
    "webhook": {
        "name": "kafka",
        "args": {
            "topic": "test",
            "bootstrap_server": "kafka",        # hostname or IP of kafka broker
            "port": 29092                       # this is default if omitted,
            "message_format": json              # json - json is default if omitted. allow future options?
        }
    }
```

### credits
 @wmclendon ( creator of this webhook )
