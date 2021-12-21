include $(TOPDIR)/rules.mk

PKG_NAME:=libpahomqttstatic
PKG_VERSION:=1.3.9
PKG_RELEASE:=1
PKG_SOURCE_PROTO:=git

PKG_SOURCE_URL:=git://github.com/eclipse/paho.mqtt.c.git
PKG_SOURCE_VERSION:=3b7ae6348bc917d42c04efa962e4868c09bbde9f
PKG_MIRROR_HASH:=

PKG_MAINTAINER:=Nian Bohung <n0404.n0404@gmail.com>
PKG_LICENSE:=Eclipse Public License 2.0

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/libpahomqttstatic
	SECTION:=libs
	CATEGORY:=PiRoutesOS
	TITLE:=Eclipse paho mqtt c library
	URL:=https://github.com/eclipse/paho.mqtt.c.git
endef

CMAKE_OPTIONS:=-DPAHO_BUILD_STATIC=TRUE -DPAHO_WITH_SSL=FALSE -DPAHO_HIGH_PERFORMANCE=TRUE

define Package/libpahomqtt_static/description
	This library provides functions for mqtt client.
endef

define Package/libpahomqttstatic/install
	$(INSTALL_DIR) $(1)/usr/include
	$(INSTALL_DIR) $(1)/usr/lib
	$(INSTALL_DIR) $(1)/usr/share
  	$(CP) $(PKG_INSTALL_DIR)/usr/include/* $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/*.a $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/share/* $(1)/usr/share
endef

$(eval $(call BuildPackage,libpahomqttstatic))
