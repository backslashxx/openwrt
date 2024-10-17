include $(TOPDIR)/rules.mk

PKG_NAME:=tinymembench
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ssvb/tinymembench.git
PKG_SOURCE_VERSION:=a2cf6d7e382e3aea1eb39173174d9fa28cad15f3
PKG_SOURCE_DATE:=2017-02-14

PKG_MAINTAINER:=none
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk

define Package/tinymembench
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=tinymembench
  URL:=https://github.com/ssvb/tinymembench
endef

define Package/tinymembench/description
  Simple benchmark for memory throughput and latency
endef

define Package/tinymembench/install
	$(INSTALL_DIR) $(1)/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/tinymembench $(1)/bin/
endef

$(eval $(call BuildPackage,tinymembench))
