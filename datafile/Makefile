#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=datafile
PKG_VERSION:=0.1
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/hishamhm/$(PKG_NAME)/archive/
PKG_MAINTAINER:=Amr Hassan <amr.hassan@gmail.com>
PKG_LICENSE=MIT

LUA_MODULE_PATH:=/usr/lib/lua

include $(INCLUDE_DIR)/package.mk

define Package/datafile
  SUBMENU:=Lua
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=datafile
  URL:=https://github.com/hishamhm/datafile
  DEPENDS:=+lua
endef

define Package/datafile/description
	A Lua library for handling paths when loading data files
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/datafile/install
	$(INSTALL_DIR) $(1)/$(LUA_MODULE_PATH)
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/datafile.lua $(1)/$(LUA_MODULE_PATH)/datafile.lua
	$(CP) $(PKG_BUILD_DIR)/datafile $(1)/$(LUA_MODULE_PATH)
endef

$(eval $(call BuildPackage,datafile))
