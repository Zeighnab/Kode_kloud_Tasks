1. Login to App Server 3 as root user.
```
ssh banner@stapp03

sudo su -
```

2. Check fot existing images.
```
docker images
```

3. Pull the busybox image {without verbose}.
```
docker pull -q busybox:musl
```

4. Re-tag the image.
```
docker tag busybox:musl busybox:blog
```