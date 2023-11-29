## Task:

The Nautilus DevOps team want to deploy a PHP website on Kubernetes cluster. They are going to use Apache as a web server and Mysql for database. The team had already gathered the requirements and now they want to make this website live. Below you can find more details:

1. Create a config map `php-config` for `php.ini` with `variables_order = "EGPCS"` data.

2. Create a deployment named `lamp-wp`.

3. Create two containers under it. 

    * First container must be `httpd-php-container` using image `webdevops/php-apache:alpine-3-php7` and

    * second container must be `mysql-container` from image `mysql:5.6`.

    * Mount `php-config` configmap in httpd container at `/opt/docker/etc/php/php.ini` location.


4. Create kubernetes generic secrets for mysql related values like myql root password, mysql user, mysql password, mysql host and mysql database. Set any values of your choice.

5. Add some environment variables for both containers:

    * MYSQL_ROOT_PASSWORD

    * MYSQL_DATABASE

    * MYSQL_USER

    * MYSQL_PASSWORD 

    * MYSQL_HOST 

__Take their values from the secrets you created. Please make sure to use env field (do not use envFrom) to define the name-value pair of environment variables.__

6. Create a node port type service `lamp-service` to expose the web application, nodePort must be `30008`.

7. Create a service for mysql named `mysql-service` and its port must be `3306`.

8. We already have `/tmp/index.php` file on jump_host server.

    * Copy this file into httpd container under Apache document root i.e `/app` and replace the dummy values for mysql related variables with the environment variables you have set for mysql related parameters. 
    
    __Please make sure you do not hard code the mysql related details in this file, you must use the environment variables to fetch those values.__

    * You must be able to access this `index.php` on node port `30008` at the end, please note that you should see Connected successfully message while accessing this page.