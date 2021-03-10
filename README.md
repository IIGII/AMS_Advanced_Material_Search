# Local Fiori Sandbox

### Quick Guide to run a UI5 app in the local launchpad

1. Put your Apps in the apps folder and used librariies in the libs folder
2. Create a gateway_controller.json file like this in the folder flp-local/config

```
{
    "gatewayConnections": {
        "default": {
            "host": "https://your-sap-system",
            "port": "44300",
            "defaultUser": {
                "_comment": "It's optional to define a default user for the forwarded requests.",
                "user": "USER",
                "password": "PASSWORD"
            },
            "proxySettings": {
                "_comment": "Available options: https://www.npmjs.com/package/http-proxy#options",
                "secure": false
            }
        }
    }
}
```
4. Install dependencies from package.json
5. Run "node update-apps-overview" in order to register the added apps to the dashboard
6. Run "node server"

Run http://localhost:3000 in your Browser.

