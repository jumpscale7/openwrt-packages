#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
# 

include $(TOPDIR)/rules.mk

PKG_NAME:=lunix
PKG_VERSION:=20140819
PKG_RELEASE:=1

PKG_SOURCE:=rel-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/wahern/$(PKG_NAME)/archive/
PKG_MAINTAINER:=Amr Hassan <amr.hassan@gmail.com>
PKG_INSTALL=1
PKG_BUILD_DEPENDS:=lua/host luac/host
PKG_LICENSE_FILE=license.txt
PKG_BUILD_DIR=$(BUILD_DIR)/$(PKG_NAME)-rel-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/lunix
  SUBMENU:=Lua
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=lunix
  URL:=https://github.com/wahern/lunix
  DEPENDS:=+lua +luac +librt
endef

define Package/lunix/description
	Lua Unix Module.
endef

define Build/Configure
endef

define Build/Compile
	$(call Build/Compile/Default,all5.1 libdir=$(STAGING_DIR_HOST)/lib bindir=$(STAGING_DIR_HOST)/bin)
endef

define Package/lunix/install
	$(INSTALL_DIR) $(1)/usr/lib/lua/
	$(INSTALL_DATA) $(PKG_INSTALL_DIR)/usr/local/lib/lua/5.1/unix.so $(1)/usr/lib/lua/unix.so
endef

$(eval $(call BuildPackage,lunix))
