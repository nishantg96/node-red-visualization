# Translate and Text-to-Speech using Watson and Node-red


## The Flow

The basic flow demonstrates the usage of visualization using an LED strip which is controlled using node-red.

![Image of the flow](https://raw.githubusercontent.com/nishantg96/node-red-visualization/main/LED/images/flow.png)


## Dashboard

![Image of the flow](https://raw.githubusercontent.com/nishantg96/node-red-visualization/main/LED/images/Dashboard.png)

To install the stable version use the Menu - Manage palette option and search for node-red-dashboard, or run the following command in your Node-RED user directory, typically *~/.node-red*:

```sh
npm install node-red-dashboard
```
Restart your Node-RED instance and you should have UI nodes available in the palette and a new dashboard tab in the right side panel. The UI interface is available at http://localhost:1880/ui (if the default settings are used).

If you want to try the latest version from github, you can install it by:

```sh
npm i node-red/node-red-dashboard
```