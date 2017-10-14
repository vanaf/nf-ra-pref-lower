# nf-ra-pref-lower
NFQUEUE based AdvDefaultPreference lower for IPv6 Router Advertisement packets

Useful on bridges
```
ip6tables -t mangle -I FORWARD -p icmpv6 --icmpv6-type router-advertisement -m physdev --physdev-in tap0 -j NFQUEUE --queue-num 1
```
