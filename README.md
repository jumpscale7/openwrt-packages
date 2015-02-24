# OpenWRT Packages
To use this as a package feed in your OpenWRT buildroot:
```bash
if [ ! -f feeds.conf ]; then mv feeds.conf.default feeds.conf ; fi
echo "src-git jumpscale https://github.com/Jumpscale/openwrt-packages.git" >> feeds.conf
./scripts/feeds update jumpscale
```

#### The following packages require the use of eglibc instead of uClibc: ####

* lunix
