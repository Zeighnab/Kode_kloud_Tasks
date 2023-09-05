## Task:

The Nautilus team is planning to use Jenkins for some of their CI/CD pipelines. DevOps team has just installed a fresh Jenkins server and they are configuring it further to be available for use.

Click on the Jenkins button on the top bar to access the Jenkins UI. Login using username `admin` and password `Adm!n321`.

It has only a sample job for now. A new developer has joined the Nautilus application development team and they want this user to be added to the Jenkins server as per the details mentioned below:

1. Create a jenkins user named `jim` with `8FmzjvFU6S` password, their full name should be `John` (it is case sensitive).

2. Using `Project-based Matrix Authorization Strategy` assign `overall read permission` to `john` user.

3. Remember to remove all permissions for Anonymous users (if given) and make sure `admin` user has `overall Administer permissions`.

4. There is one existing job, make sure `john` only has `read permissions` to that job (we are not worried about other permissions like Agent, SCM, etc.).