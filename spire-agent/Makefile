#
#
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=spire-agent
PKG_VERSION:=0.0.1
PKG_RELEASE:=1

# PKG_SOURCE:=../../../spire
# UNPACK_CMD=cp -R $(PKG_SOURCE)/* $(1)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/spiffe/spire.git
PKG_REV:=aa327b2be26c0c2a5dca5a315f089dd28cb29568

PKG_SOURCE_VERSION:=$(PKG_REV)
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_SOURCE_SUBDIR).tar.gz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_SOURCE_SUBDIR)

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE
PKG_MAINTAINER:=From Nowhere To <mail@nowhere.org>

PKG_BUILD_DEPENDS:=golang/host
PKG_BUILD_PARALLEL:=1
PKG_USE_MIPS16:=0

GO_PKG:=github.com/spiffe/spire

include $(INCLUDE_DIR)/package.mk
include ../../packages/lang/golang/golang-package.mk

define Package/spire-agent
	SECTION:=cpe
	CATEGORY:=CPE
	TITLE:=spire-agent
	URL:=https://github.com/spiffe/spire
	DEPENDS:=$(GO_ARCH_DEPENDS)
endef

define Package/spire-agent/description
	This package contains the main program.
endef

$(eval $(call GoBinPackage,spire-agent))
$(eval $(call BuildPackage,spire-agent))