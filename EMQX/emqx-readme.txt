EMQX Broker — Setup Notes
Files
- docker-compose.yml — configuration used to run the EMQX broker container
- emqx-backup-export.<ext> — exported configuration (users, ACL rules, rule engine settings) from the EMQX Dashboard

Setup Instructions
1.Run docker-compose up -d using the provided docker-compose.yml to start a fresh EMQX instance
2.Access the EMQX Dashboard (default: http://localhost:18083)
3.Go to System → Backup & Restore (or the equivalent menu in your EMQX version) and import the provided backup file
4.Verify that users, topics, and ACL rules match what is described in the book


Note on Credentials
If any passwords were present in the original configuration, they have been removed or replaced with placeholders in the files provided. You will need to set your own credentials after restoring the backup.