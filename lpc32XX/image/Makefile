#
# Copyright (C) 2007-2008 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/image.mk


define Image/BuildKernel
	mkimage -A arm -O linux -T kernel -C none -a 30007FC0 -e 30008000 -n "WODE!" -d $(LINUX_DIR)/arch/arm/boot/Image $(BIN_DIR)/openwrt-$(BOARD)-$(KERNEL)-uImage
endef

define Image/Build/squashfs
    $(call prepare_generic_squashfs,$(BIN_DIR)/openwrt-$(BOARD)-$(KERNEL)-root.$(1))
endef

define Image/Build
	$(CP) $(KDIR)/root.$(1) $(BIN_DIR)/openwrt-$(BOARD)-$(KERNEL)-root.$(1)
	$(call Image/Build/$(1),$(1))
endef

$(eval $(call BuildImage))
