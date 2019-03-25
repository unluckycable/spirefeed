# spirefeed

in feeds.conf

src-git packages https://git.openwrt.org/feed/packages.git
src-git luci https://git.openwrt.org/project/luci.git
src-git routing https://git.openwrt.org/feed/routing.git
src-git telephony https://git.openwrt.org/feed/telephony.git
src-link spirefeed /home/username/spirefeed

cd openwrt

./scripts/feeds update -a
./scripts/feeds install -a


