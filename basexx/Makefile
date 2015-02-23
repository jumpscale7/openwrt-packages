#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=basexx
PKG_VERSION:=0.1.0
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/aiq/$(PKG_NAME)/archive/
PKG_MAINTAINER:=Amr Hassan <amr.hassan@gmail.com>
PKG_LICENSE=MIT

LUA_MODULE_PATH:=/usr/lib/lua

include $(INCLUDE_DIR)/package.mk

define Package/basexx
  SUBMENU:=Lua
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=basexx
  URL:=https://github.com/aiq/basexx
  DEPENDS:=+lua
endef

define Package/basexx/description
	A Lua library which provides base2(bitfield), base16(hex), base32(crockford/rfc), 
	base64 decoding and encoding.
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/basexx/install
	$(INSTALL_DIR) $(1)/$(LUA_MODULE_PATH)
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/lib/basexx.lua $(1)/$(LUA_MODULE_PATH)/basexx.lua
endef

$(eval $(call BuildPackage,basexx))
