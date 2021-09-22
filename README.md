# Gitter MD export App

A simple way to export the chat history of a room as markdown. Very crude as simple a quick hack based on the official [gitter-demo-app](https://github.com/gitterHQ/gitter-demo-app).

## HOWTO

1. Create a new app at [https://developer.gitter.im](https://developer.gitter.im). The ```Redirect URL``` should be ```http://localhost:7000/login/callback```
2. Run `npm install` and `nopm install express`
3. Get the `MESSAGE_START_ID` from the Gitter UI. Take the one before the messages you want to print
4. Launch the demo app with:

```
GITTER_KEY=<your-oauth-app-key> GITTER_SECRET=<your-oauth-app-secret> MESSAGE_START_ID=<message-id-from-gitter-webui> node app.js
```

5. Go to [localhost:7000](http://localhost:7000/) and select the right gitter room (the one containing the `MESSAGE_START_ID`)
6. You should see the messages on a webpage or in a .md file
