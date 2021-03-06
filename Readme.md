- App Share To stage view.

## Prerequisites

- [NodeJS](https://nodejs.org/en/)
- [ngrok](https://ngrok.com/) or equivalent tunnelling solution
- Publicly addressable https url or tunnel such as [ngrok](https://ngrok.com/) or [Tunnel Relay](https://github.com/OfficeDev/microsoft-teams-tunnelrelay) 
    
## To try this sample
-  Clone the repository

    ```bash
    git clone https://github.com/jignesh-stp/ShareToStageDemo.git
    ```

- In a terminal, navigate to cloned repo

- Install modules

    ```
    npm install
    ```
- Run ngrok - point to port 3978

    ```
    ngrok http 3978 -host-header=localhost:3978
    ```    
- Modify the `manifest.json` in the `/Manifest` folder and replace the following details
   - `<<App-ID>>` with some unique GUID   
   - `<<BASE-URL>>` with your application's base url, e.g. https://1234.ngrok.io
   - `<<VALID DOMAIN>>` with your app domain e.g. *.ngrok.io

 - Run solution

    ```
    npm start
    ```

- Zip the contents of `Manifest` folder into a `manifest.zip`

- Upload the manifest.zip to Teams (in the Apps view click "Upload a custom app")
   - Go to Microsoft Teams. From the lower left corner, select Apps
   - From the lower left corner, choose Upload a custom App
   - Go to your project directory, the ./Manifest folder, select the zip folder, and choose Open.
   - Select Add in the pop-up dialog box. Your tab is uploaded to Teams.

## Interacting with the app in Teams
    You can use this app by following the below steps:
    - Edit a meeting and select `+` icon at the top right corner.

![Add icon in meeting](Images/add_icon.png)

    - Search for your app `App in meeting` and add it.

![Select App](Images/select_app.png)

    - Join the meeting and click on the app icon at the top
    - This will open a sidepanel with `Share` icon at top to share the app for collaboration in stage view.

![App icon](Images/app_icon.png)
