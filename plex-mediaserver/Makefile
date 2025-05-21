include $(TOPDIR)/rules.mk

PKG_NAME:=plex-mediaserver
PKG_VERSION:=1.41.5
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=multimedia
	CATEGORY:=Multimedia
    TITLE:=Plex Media Server
    URL:=https://github.com/jkool702/openwrt-plexmediaserver
    PKGARCH:=aarch64_cortex-a53
	DEPENDS:=+squashfs-tools-mksquashfs
	#unzip busybox
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/etc/init.d/plexmediaserver $(1)/etc/init.d/
	$(INSTALL_DIR) $(1)/etc/config
	$(INSTALL_CONF) ./files/etc/config/plexmediaserver $(1)/etc/config/
endef

$(eval $(call BuildPackage,plex-mediaserver))
