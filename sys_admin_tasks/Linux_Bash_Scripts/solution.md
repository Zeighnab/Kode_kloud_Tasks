1. SSH into App Server 1

2. cd into the `/scripts` folder and create the requested backup script
```
vi /scripts/beta_backup.sh
```

3. Write a script to create a zip file and save into `/backup` directory of the App Server and Backup Server
```
#!/bin/bash
zip -r /backup/xfusioncorp_beta.zip /var/www/html/beta
scp /backup/xfusioncorp_beta.zip clint@stbkp01:/backup
```

