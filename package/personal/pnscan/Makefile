include $(TOPDIR)/rules.mk

PKG_NAME:=pnscan
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ptrrkssn/pnscan.git
PKG_SOURCE_VERSION:=5a8cd55b0a11e625bc48039ebed62331835710f8
PKG_SOURCE_DATE:=2020-06-19

PKG_MAINTAINER:=none
PKG_LICENSE:=BSD-3
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk

define Package/pnscan
  SECTION:=net
  CATEGORY:=Network
  TITLE:=pnscan
  URL:=https://github.com/ptrrkssn/pnscan
  DEPENDS:=+libpthread
endef

define Package/pnscan/description
  Peter's Parallel Network Scanner
endef

define Package/pnscan/install
	$(INSTALL_DIR) $(1)/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/pnscan $(1)/bin/
endef

$(eval $(call BuildPackage,pnscan))
