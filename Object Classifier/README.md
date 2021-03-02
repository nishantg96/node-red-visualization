# Object Classifier using Watson and Node-red

In this part, we will use the [Watson Visual recognition service](https://cloud.ibm.com/catalog/services/visual-recognition) to analyze the contents of an image and produce a series of text classifiers with a confidence score. A picture can either be uploaded from the filesyem or a picture can be clicked from an USB camera or it can be taken from a live stream of an IP camera.

## The Flow

The basic flow will allow the user to grab a picture from there local filesystem or from the cameras and send it to the Watson Visual recognition API.

![Image of the flow](https://raw.githubusercontent.com/nishantg96/node-red-visualization/main/Object%20Classifier/images/oc_flow.png)

## Watson Visual Recognition API configuration

1. Log into the [Watson cloud services](https://cloud.ibm.com/login).
2. Go to [Watson Visual recognition service](https://cloud.ibm.com/catalog/services/visual-recognition) in the catalogs tab.
3. Create visual recognition service with all the desired settings. For the time, the *lite* plan has been used.
4. Head over to [Resource list](https://cloud.ibm.com/resources) and go to the services menu. 
5. If the Watson Visual recognition service was configured correctly, an option to select it would be available under the service menu.
6. Clicking on it would land you on the credential page where you can see the **API key** and the **URL**.
7. Head back to the Node-red where you created the visual-recognition flow. On inserting the ![VR api](https://raw.githubusercontent.com/nishantg96/node-red-visualization/main/Object%20Classifier/images/vr.png) node.
8. To configure the node, open the node and enter the APIkey and the URL (in service endpoint).
9. If everything is configured correctly, you can deploy the flow.
    
   ![VR config](https://raw.githubusercontent.com/nishantg96/node-red-visualization/main/Object%20Classifier/images/VR_props.png)

## Dashboard

To install the stable version use the Menu - Manage palette option and search for node-red-dashboard, or run the following command in your Node-RED user directory, typically *~/.node-red*:

```sh
npm install node-red-dashboard
```
Restart your Node-RED instance and you should have UI nodes available in the palette and a new dashboard tab in the right side panel. The UI interface is available at http://localhost:1880/ui (if the default settings are used).

If you want to try the latest version from github, you can install it by:

```sh
npm i node-red/node-red-dashboard
```