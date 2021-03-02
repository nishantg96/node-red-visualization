# Translate and Text-to-Speech using Watson and Node-red

In this part, we use the [Watson Language Translator service](https://cloud.ibm.com/catalog/services/language-translator) and [Watson Text-to-Speech](https://cloud.ibm.com/catalog/services/text-to-speech).

## The Flow

The basic flow will allow the user to send a message to a telegram bot, enter a text or ask the node to read an email and translate the text from it. The translated text is then converted to speech which is read out loud from the speaker.

![Image of the flow](https://raw.githubusercontent.com/nishantg96/node-red-visualization/main/Translate-TTS/images/flow.PNG)

## Watson Visual Recognition API configuration

1. Log into the [Watson cloud services](https://cloud.ibm.com/login).
2. Go to the said services in the catalogs tab.
3. Create language translate and Text to Speech services with all the desired settings. For the time, the *lite* plan has been used.
4. Head over to [Resource list](https://cloud.ibm.com/resources) and go to the services menu. 
5. If the services were configured correctly, an option to select it would be available under the service menu.
6. Clicking on the services would land you on the credential page where you can see the **API key** and the **URL**.
7. Head back to the Node-red where you created the Translate-TTS flow. 
8. To configure the node, open the node and enter the APIkey and the URL (in service endpoint).
9. If everything is configured correctly, you can deploy the flow.
    

## Dashboard

![Image of the flow](https://raw.githubusercontent.com/nishantg96/node-red-visualization/main/Translate-TTS/images/dashboard.PNG)

To install the stable version use the Menu - Manage palette option and search for node-red-dashboard, or run the following command in your Node-RED user directory, typically *~/.node-red*:

```sh
npm install node-red-dashboard
```
Restart your Node-RED instance and you should have UI nodes available in the palette and a new dashboard tab in the right side panel. The UI interface is available at http://localhost:1880/ui (if the default settings are used).

If you want to try the latest version from github, you can install it by:

```sh
npm i node-red/node-red-dashboard
```