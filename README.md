# OpenWRT Packages
To use this as a package feed in your OpenWRT buildroot:
```bash
if [ ! -f feeds.conf ]; then cp feeds.conf.default feeds.conf ; fi
echo "src-git jumpscale https://github.com/Jumpscale/openwrt-packages.git;for-14.07" >> feeds.conf
./scripts/feeds update jumpscale
```
