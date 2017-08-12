# Zipkin Service

Service which provides traceability and tracking of requests through a distributed system.



## Requires

Consul
```
  $ docker run \
    -p 8400:8400 \
    -p 8500:8500 \
    -p 8600:53/udp \
    -h node1 \
    progrium/consul -server -bootstrap -ui-dir /ui
```

Rabbit MQ
```
  $ docker run -d \
    --net=host \
    --hostname my-rabbit \
    --name some-rabbit \
    rabbitmq:3
```

## Build

```
  $ mvn clean package
```

## Run

```
  $ java -jar target/zipkin-1.0-SNAPSHOT.jar
```


