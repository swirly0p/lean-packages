include $(TOPDIR)/rules.mk

PKG_NAME:=switch-lan-play
PKG_VERSION:=0.2.1
PKG_RELEASE:=3
PKG_MAINTAINER:=spacemeowx2

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/spacemeowx2/switch-lan-play.git
PKG_SOURCE_VERSION:=9f291fe20d673ece3ed99239ce67c12969d1ef82
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_BUILD_DIR:=$(BUILD_DIR)/switch-lan-play-$(PKG_VERSION)

PKG_LICENSE:=GNU
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/switch-lan-play 
  SECTION:=net
  CATEGORY:=Network
  TITLE:=switch-lan-play
  URL:=https://github.com/spacemeowx2
  DEPENDS:=+libpcap

endef

define Package/switch-lan-play/description
    Make you and your friends play games like in a LAN.
endef

define Package/switch-lan-play/install
    $(INSTALL_DIR) $(1)/usr/bin
    $(INSTALL_BIN) $(PKG_BUILD_DIR)/src/lan-play $(1)/usr/bin
endef

$(eval $(call BuildPackage,switch-lan-play))