#
# Copyright (C) 2022 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ath10k-quic-firmware
PKG_SOURCE_DATE:=2024-10-22
PKG_RELEASE:=2


include $(INCLUDE_DIR)/package.mk

RSTRIP:=:
STRIP:=:

define Package/ath10k-quic-firmware-default
  SECTION:=firmware
  CATEGORY:=Firmware
  URL:=$(PKG_SOURCE_URL)
  DEPENDS:=
endef

define Package/ath10k-quic-firmware-ipq4019
$(Package/ath10k-quic-firmware-default)
  TITLE:=IPQ4019 10.4-3.2.1.1-00035
endef

define Build/Compile

endef


define Package/ath10k-quic-firmware-ipq4019/install
	$(INSTALL_DIR) $(1)/lib/firmware/ath10k/QCA4019/hw1.0
	$(INSTALL_DATA) \
		$(PKG_BUILD_DIR)/firmware-5.bin_10.4-3.2.1.1-00035 \
		$(1)/lib/firmware/ath10k/QCA4019/hw1.0/firmware-5.bin
endef

$(eval $(call BuildPackage,ath10k-quic-firmware-ipq4019))

