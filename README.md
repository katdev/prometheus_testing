# A repository for testing Prometheus, various exporters, and other things
This is a quick & easy way to spin up a local dockerized Prometheus environment for testing, along with exporters and other containers as specified in [docker-compose.yml](./docker-compose.yml).

Data is stored on the Prometheus container, and will be deleted when the container is stopped.

Note that use of the cloudwatch_exporter assumes that you have valid AWS account credentials associated with a \[default\] profile in ~/.aws/credentials for the AWS account of interest.
## Start it up
- `docker-compose up -d`

Localhost endpoints of interest
- [Prometheus](http://localhost:9090)
- [Grafana](http://localhost:3000)
- [blackbox_exporter](http://localhost:9115)
- [cloudwatch_exporter](http://localhost:9106)

## Stop it
- `docker-compose down`