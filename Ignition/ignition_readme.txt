Ignition Project — Setup Notes
Files
- BottlingLine_UNS_20261002132820.zip — exported project resources (views, tags, scripts, templates) from Ignition Designer/Gateway

What's Included
This export contains the project logic built throughout the book: Perspective/Vision views, tag definitions, UDTs, and scripts.

What's NOT Included
Gateway-level configuration is not part of a project export and must be set up manually in your own Ignition Gateway before importing:
-Database connection — pointing to your SQL Server instance (see Chapter 4 for schema and connection details)
-OPC UA device connection — pointing to your PLC (see Chapter 3 for configuration steps)
-Tag providers — as configured in the book's walkthrough

Import Instructions
1.In your Ignition Gateway: Config → Projects → Import
2.Select ignition-project-export.zip
3.Before running the project, recreate the database and OPC UA connections listed above, matching the names/paths referenced in the project's tags and scripts
4.Open the project in Designer to verify all connections resolve correctly