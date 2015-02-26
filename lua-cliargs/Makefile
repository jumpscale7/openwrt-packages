#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#  

include $(TOPDIR)/rules.mk

PKG_NAME:=lua-cliargs
PKG_VERSION:=2.3-3
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/amireh/lua_cliargs/archive/
PKG_MAINTAINER:=Amr Hassan <amr.hassan@gmail.com>
PKG_LICENSE=MIT
PKG_BUILD_DIR=$(BUILD_DIR)/lua_cliargs-$(PKG_VERSION)/

LUA_MODULE_PATH:=/usr/lib/lua

include $(INCLUDE_DIR)/package.mk

define Package/lua-cliargs
  SUBMENU:=Lua
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=lua-cliargs
  URL:=https://github.com/amireh/lua_cliargs
  DEPENDS:=+lua
endef

define Package/lua-cliargs/description
	A command-line argument parsing module for Lua.
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/lua-cliargs/install
	$(INSTALL_DIR) $(1)/$(LUA_MODULE_PATH)
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/src/cliargs.lua $(1)/$(LUA_MODULE_PATH)/cliargs.lua
endef

$(eval $(call BuildPackage,lua-cliargs))
