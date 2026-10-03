# dingdong-opkg

Public OpenWrt opkg feed for dingdong-listener (packages only).

```
src/gz dingdong_feed https://raw.githubusercontent.com/lioWeb1024/dingdong-opkg/main
```

Routers with `option check_signature 1` need the feed public key:

```
mkdir -p /etc/opkg/keys
uclient-fetch -O /etc/opkg/keys/16db492bdceecaf3 https://raw.githubusercontent.com/lioWeb1024/dingdong-opkg/main/dingdong-opkg.pub
opkg update
```
