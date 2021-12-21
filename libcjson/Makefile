include $(TOPDIR)/rules.mk

PKG_NAME:=libcjson
PKG_VERSION:=1.7.15
PKG_RELEASE:=1
PKG_SOURCE_PROTO:=git

PKG_SOURCE_URL:=git@github.com:DaveGamble/cJSON.git
PKG_SOURCE_VERSION:=203a0dec6ff06e3842fa23a1bc9825aecf56b381
PKG_MIRROR_HASH:=

PKG_MAINTAINER:=Nian Bohung <n0404.n0404@gmail.com>
PKG_LICENSE:=Eclipse Public License 2.0

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/libcjson
	SECTION:=libs
	CATEGORY:=Pi_routes_os
	TITLE:=Json library for c language
 	URL:=https://github.com/DaveGamble/cJSON
endef

define Package/libcjson/description
 	This library provides functions for cjson.
endef

define Package/libcjson/install
 	$(INSTALL_DIR) $(1)/usr
 	$(CP) $(PKG_INSTALL_DIR)/usr/* $(1)/usr
endef

$(eval $(call BuildPackage,libcjson))
