#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
# 

include $(TOPDIR)/rules.mk

PKG_NAME:=csagent
PKG_VERSION:=3
PKG_RELEASE:=6

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

define Package/csagent/postinst
#!/bin/sh
# check if we are on real system
if [ -z "$${IPKG_INSTROOT}" ]; then
        echo "Enabling rc.d symlink for $(PKG_NAME)"
        /etc/init.d/$(PKG_NAME) enable
fi
exit 0
endef

define Package/csagent/prerm
#!/bin/sh
# check if we are on real system
if [ -z "$${IPKG_INSTROOT}" ]; then
        echo "Removing rc.d symlink for $(PKG_NAME)"
        /etc/init.d/$(PKG_NAME) disable
fi
exit 0
endef

define Package/csagent/install
	$(INSTALL_DIR) $(1)/usr/share/csagent
	$(INSTALL_DIR) $(1)/usr/bin/
	$(INSTALL_DIR) $(1)/etc/config
	$(CP) $(PKG_BUILD_DIR)/*.lua $(1)/usr/share/csagent
	$(INSTALL_BIN) files/csagent $(1)/usr/bin/csagent
	$(INSTALL_BIN) files/config $(1)/etc/config/csagent
endef

$(eval $(call BuildPackage,csagent))
