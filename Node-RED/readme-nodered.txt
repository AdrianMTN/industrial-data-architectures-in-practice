NODERED Flow - Setup Notes


This flow requires the following additional Node-RED nodes, not included in the default installation:
- node-red-contrib-opcua — for OPC UA communication with the PLC
- (add any other custom nodes you used, e.g. MQTT, SQL/database nodes, if not already built-in)

Install them from the Node-RED editor: Menu (☰) → Manage palette → Install, then search for the package name above, or run from the Node-RED user directory:
- npm install node-red-contrib-opcua


Credentials
For security reasons, the exported flow (flows.json) does not include any credentials (OPC UA connection passwords, MQTT broker authentication, database login details, etc.). Node-RED stores these separately and encrypted, and they are intentionally excluded from the export.
After importing the flow, you will need to reconfigure these manually in the respective nodes:
- OPC UA endpoint connection settings (and credentials, if your server requires authentication)
- MQTT broker connection (host, port, username/password if applicable)
- Any database connection strings used in the flow

Import Instructions
1.Install the required nodes listed above
2.In Node-RED: Menu (☰) → Import → select the .json file
3.Reconfigure credentials and endpoint addresses to match your own environment (PLC IP address, broker address, etc.)
4.Deploy the flow