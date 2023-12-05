# k6-test
Playing around with K6, statsD and Otel collector

This repository is to collect my knowledge about running K6 from k6.io, connected to our backend system.

**Start Otel Collector with:**
`docker run --rm \ 
-e SPLUNK_O11Y_TOKEN=<our splunk o11y token here> \
-e SPLUNK_CLOUD_METRIC_TOKEN=<our splunk cloud token for metric index here> \
-e SPLUNK_CLOUD_EVENT_TOKEN=<our splunk cloud token for event index here here> \
-e NEW_RELIC_INGEST_TOKEN=<our New Relic ingest token here> \
-e SPLUNK_CONFIG=/etc/collector.yaml -v "${PWD}/collector.yaml":/etc/collector.yaml:ro \  
-p 8125:8125/udp \
--name otelcol otel/opentelemetry-collector-contrib:latest`

