#
# Copyright (C) 2006-2009 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=lpc32XX
BOARDNAME:=Embedded Artists Lpc 3250
FEATURES:=jffs2
LINUX_VERSION:=2.6.32

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES += 

define Target/Description
	Build firmware images for Embedded Artists
endef

$(eval $(call BuildTarget))
