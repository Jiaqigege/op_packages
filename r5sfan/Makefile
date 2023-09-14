include $(TOPDIR)/rules.mk

PKG_NAME:=r5sfan
PKG_VERSION:=1.0
PKG_RELEASE:=1

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/r5sfan
    SECTION:=My Apps
    CATEGORY:=My Apps
    DEPENDS:=
    TITLE:=r5s fan
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	cp -rf ./src/* $(PKG_BUILD_DIR)
endef

define Build/Compile
endef	


define Build/Compile/Default

endef

define Package/$(PKG_NAME)/description
  r5s air fan
endef


define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_DIR) $(1)/etc/rc.d
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/auto_fan $(1)/etc/init.d/auto_fan
	$(CP) $(PKG_BUILD_DIR)/S99auto_fan  $(1)/etc/rc.d/S99auto_fan
	#$(INSTALL_BIN) $(PKG_BUILD_DIR)/S99auto_fan $(1)/root/S99auto_fan_ins_bin
	#$(LN) /etc/init.d/auto_fan $(1)/root/S100auto_fan_ln
endef
	
$(eval $(call BuildPackage,$(PKG_NAME)))

