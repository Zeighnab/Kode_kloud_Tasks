## Task:

The xFusionCorp development team added updates to the project that is maintained under `/opt/games.git` repo and cloned under /`usr/src/kodekloudrepos/games`. 
Recently some changes were made on Git server that is hosted on Storage server in Stratos DC. T
he DevOps team added some new Git remotes, so we need to update remote on `/usr/src/kodekloudrepos/games` repository as per details mentioned below:

* In `/usr/src/kodekloudrepos/games` repo add a new remote `dev_games` and point it to `/opt/xfusioncorp_games.git` repository.

* There is a file `/tmp/index.html` on same server; copy this file to the repo and `add/commit` to `master` branch.


c. Finally push `master` branch to this new remote origin.