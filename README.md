# OpenWRT Packages
To use this as a package feed in your OpenWRT buildroot:
```bash
if [ ! -f feeds.conf ]; then cp feeds.conf.default feeds.conf ; fi
echo "src-git jumpscale URL;for-14.07 >> feeds.conf
./scripts/feed update jumpscale
```
