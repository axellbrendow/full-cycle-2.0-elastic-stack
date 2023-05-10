# full-cycle-2.0-elastic-stack

Files I produced during the "Observability / Elastic Stack" classes of my [Microservices Full Cycle 3.0 course](https://drive.google.com/file/d/1bJnFxQPKgSsI30sCvW-KzYK4V5JWzgSs/view?usp=share_link).

## Initial steps

```sh
docker network create observability
docker-compose up
# Then, access localhost:5601 to open kibana
# Go to Observability->Metrics to see docker the metrics of your computer
# Go to Observability->Uptime to see the containers uptime
```

## Using Elastic APM

Run the django application:

```sh
cd app
docker-compose up
```

Now, go to localhost:8000 and you will receive a 404 not found, then, go to localhost:8000/exemplo and you will get a page.

Now go to kibana on Observability->APM->Services->codeprogress-run->Transactions->/exemplo and see the trace.
