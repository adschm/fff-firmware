include $(TOPDIR)/rules.mk

PKG_NAME:=fff-nodewatcher
PKG_RELEASE:=59.1

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=base
	CATEGORY:=Freifunk
	TITLE:= Freifunk-Franken Nodewatcher
	URL:=http://www.freifunk-franken.de
	DEPENDS:=+ip +ip-bridge +micrond +fff-alfred +fff-config +fff-random
endef

define Package/$(PKG_NAME)/description
	This is the Nodewatcher for the Freifunk Franken Firmware
	It is used to send node status information to
	monitoring.freifunk-franken.de and
	netmon.freifunk-franken.de
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
	printf "$(if $(PKG_VERSION),$(PKG_VERSION).)$(PKG_RELEASE)" >> $(1)/etc/nodewatcher_version
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
