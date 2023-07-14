# neo4j graph database running on balena

This is a proof of concept to run the graph database neo4j on balena x86 device.

## Deploy the code

Running this project is as simple as deploying it to a balenaCloud application. You can do it in just one click by using the button below:

[![](https://www.balena.io/deploy.png)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/mpous/neo4j-balena)

Follow instructions, click Add a Device and flash an SD card with that OS image dowloaded from balenaCloud. Enjoy the magic 🌟Over-The-Air🌟!

## Log in

The neo4j UI service is exposed on the `7474` port. You can access to the UI using the local IP address with the port 7474.

|Service|Port|Username|Password|
|:--|---|---|---|
|neo4j|7474 (http)|neo4j|balenabalenabalena|


## Troubleshooting

If you detect any issue using this block, feel free to contact us at the [forums.balena.io](https://forums.balena.io).

