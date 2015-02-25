#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
# 

include $(TOPDIR)/rules.mk

PKG_NAME:=csagent
PKG_VERSION:=2.0
PKG_RELEASE:=1

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/jumpscale/$(PKG_NAME)/archive/
PKG_MAINTAINER:=Amr Hassan <amr.hassan@gmail.com>
PKG_INSTALL=1

include $(INCLUDE_DIR)/package.mk

define Package/csagent
  SUBMENU:=
  SECTION:=jumpscale
  CATEGORY:=JumpScale
  TITLE:=csagent
  URL:=https://github.com/jumpscale/csagent
  DEPENDS:=+lua +luasocket +uuid +basexx +json4lua +luafilesystem +lua-penlight +luarocks +lua-cliargs
endef

define Package/csagent/description
	A JumpScale agent in Lua.
endef

define Build/Configure
endef

define Build/Compile
endef

define Build/Install
endef

define Package/csagent/install
	$(INSTALL_DIR) $(1)/usr/share/csagent
	$(INSTALL_DIR) $(1)/usr/bin/
	$(CP) $(PKG_BUILD_DIR)/*.lua $(1)/usr/share/csagent
	$(INSTALL_BIN) files/csagent $(1)/usr/bin/csagent
endef

$(eval $(call BuildPackage,csagent))
