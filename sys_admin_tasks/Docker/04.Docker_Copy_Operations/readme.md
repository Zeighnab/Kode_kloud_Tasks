## Task:

The Nautilus DevOps team has some confidential data present on `App Server 2` in `Stratos Datacenter`. There is a container `ubuntu_latest` running on the same server. We received a request to copy some of the data from the docker host to the container. Below are more details about the task:

* On `App Server 2` in Stratos Datacenter, copy an encrypted file `/tmp/nautilus.txt.gpg` from docker host to `ubuntu_latest` container (running on same server) in `/usr/src/` location. **Please do not try to modify this file in any way**.