# docker-free-rootfs

Created via:
```sh
mkdir rootfs
docker run --name rootfs alpine true
docker export rootfs | tar -x -C rootfs/ --exclude dev/ --exclude sys/ --exclude proc/
find rootfs/ -type d -empty -not -name '*empty' -exec touch {}/.keep \;
git add -A
git commit -m'Alpine'
```

