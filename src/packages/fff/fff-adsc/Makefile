include $(TOPDIR)/rules.mk

PKG_NAME:=fff-adsc
PKG_RELEASE:=0.2

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=base
	CATEGORY:=Freifunk
	TITLE:=Freifunk-Franken adsc Customizations
	URL:=http://www.freifunk-franken.de
	DEPENDS:=+@BUSYBOX_CONFIG_WGET
endef

define Package/$(PKG_NAME)/description
	This is the adsc customization package.
endef

define Build/Prepare
	echo "all: " > $(PKG_BUILD_DIR)/Makefile
endef

define Build/Configure
	# nothing
endef

define Build/Compile
	# nothing
endef

define Package/$(PKG_NAME)/install
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
