# docker-free-rootfs

Created via:
```sh
docker run --name rootfs alpine true
docker export rootfs | tar x
git add -A
git commit -m'Alpine'
```
