# MCP Server for Copilot Studio Demos

## Prerequisites
Node v22  
Azure Developer CLI  
Azure Subscription  

## Run the MCP Server local
Start the server local in Visual Studio Code
Run ```npm install```  
Run ```npm run build && npm run start```  

Forward port 3000 exposed by the server using microsoft dev tunnel
![](https://raw.githubusercontent.com/holgerimbery/mcpserver/main/assets/port1.jpg)  
![](https://raw.githubusercontent.com/holgerimbery/mcpserver/main/assets/port2.jpg)  
![](https://raw.githubusercontent.com/holgerimbery/mcpserver/main/assets/port3.jpg)  


open the URL in your browser and add ```/mcp``` to the URL to access the MCP Server.

The result should look like this:
![](https://raw.githubusercontent.com/holgerimbery/mcpserver/main/assets/port4.jpg)

## Run the MCP Server in Azure
Make sure to login to Azure Developer CLI if you haven't done that yet.

```
azd auth login
```

> [!WARNING]  
> After running azd up, you will have an MCP Server running on Azure that is publicly available.
> Ideally, you don't want that.
> Make sure to run ```azd down``` after finishing the lab to delete all the resources from your Azure subscription.

Run the following command in the terminal:
```
azd up
```

## Tools 
- bitcoin in USD


## MCP Server in Microsoft Copilot Studio
Import the Connector

### Setting up the Custom Connector

* Navigate to the Power Apps custom connectors page at https://make.preview.powerapps.com/customconnectors and select "+ New custom connector"

* Choose "Import from GitHub" option

*  Configure the import with these settings:
    - Connector Type: Custom
    - Branch: dev
    - Connector: MCP-Streamable-HTTP

*  Click "Continue" to proceed

*  In the configuration screen:
    - Assign a descriptive name (e.g., "Demo MCP Server for Copilot Studio")
    - Add an appropriate description
    - Enter your server URL in the Host field (either your dev tunnel URL like `something-3000.something.devtunnels.ms` or Azure URL like `something.azurecontainerapps.io`)

* Complete the process by selecting "Create connector"

### Add the MCP Server to your Copilot Studio
Add the MCP Server to your Copilot Studio by selecting it within the "tools" tab in the Copilot Studio.
