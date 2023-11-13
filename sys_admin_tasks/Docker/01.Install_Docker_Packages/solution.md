1. SSh into App server 1
```
ssh tony@stapp01

sudo su -
```

2. Install docker packages
```
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

---

sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

---

sudo systemctl start docker
```

* Visit [docker official website](https://docs.docker.com/engine/install/centos/) for more info.