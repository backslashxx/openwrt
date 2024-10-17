#
# Copyright (C) 2022 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ath11k-extfw
PKG_SOURCE_DATE:=2024-07-28
PKG_RELEASE:=2


include $(INCLUDE_DIR)/package.mk

RSTRIP:=:
STRIP:=:

define Package/ath11k-extfw-default
  SECTION:=firmware
  CATEGORY:=Firmware
  URL:=$(PKG_SOURCE_URL)
  DEPENDS:=
endef

define Package/ath11k-extfw-ipq6018-212-01368
$(Package/ath11k-extfw-default)
  TITLE:=IPQ6018 ath11k firmware 2.12-01368
endef

define Package/ath11k-extfw-ipq6018-212-01460
$(Package/ath11k-extfw-default)
  TITLE:=IPQ6018 ath11k firmware 2.12-01460
endef

define Build/Compile

endef


define Package/ath11k-extfw-ipq6018-212-01368/install
	$(INSTALL_DIR) $(1)/lib/firmware/IPQ6018
	$(INSTALL_DATA) \
		$(PKG_BUILD_DIR)/WLAN.HK.2.12-01368-QCAHKSWPL_SILICONZ-1/* \
		$(1)/lib/firmware/IPQ6018/
endef

define Package/ath11k-extfw-ipq6018-212-01460/install
	$(INSTALL_DIR) $(1)/lib/firmware/IPQ6018
	$(INSTALL_DATA) \
		$(PKG_BUILD_DIR)/WLAN.HK.2.12-01460-QCAHKSWPL_SILICONZ-1/* \
		$(1)/lib/firmware/IPQ6018/
endef

$(eval $(call BuildPackage,ath11k-extfw-ipq6018-212-01368))
$(eval $(call BuildPackage,ath11k-extfw-ipq6018-212-01460))

