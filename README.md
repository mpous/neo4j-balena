# neo4j graph database running on balena

This is a proof of concept to run the graph database neo4j on balena x86 devices.

## Deploy the code

Running this project is as simple as deploying it to a balenaCloud application. You can do it in just one click by using the button below:

[![](https://www.balena.io/deploy.png)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/mpous/neo4j-balena)

Follow instructions, click Add a Device and flash an SD card with that OS image dowloaded from balenaCloud. Enjoy the magic 🌟Over-The-Air🌟!

## Log in

The neo4j UI service is exposed on the `7474` port. You can access to the UI using the local IP address with the port 7474.

|Service|Port|Username|Password|
|:--|---|---|---|
|neo4j|7474 (http)|neo4j|balenabalenabalena|


![Captura de pantalla 2023-07-20 a les 14 16 09](https://github.com/mpous/neo4j-balena/assets/173156/c9fdff4c-48fd-4052-828f-12afa6dfec26)


## neo4j Block configuration

To add the neo4j Block, add this service in your `docker-compose.yml`, as shown below.

```
  neo4j:
    image: bh.cr/marc6/neo4j-amd64
    ports:
      - "7474:7474"
      - "7687:7687"
    volumes:
      - neo4j-data:/data
      - neo4j-logs:/logs
    environment:
      - NEO4J_AUTH=< your username >/< your password >
    restart: always

volumes:
  neo4j-data:
  neo4j-logs:
```

At this moment you will have the neo4j graph database UI available on the port `7474`.


## Troubleshooting

If you detect any issue using this block, feel free to contact us at the [forums.balena.io](https://forums.balena.io).

