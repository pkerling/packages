#
# Copyright (C) 2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-compress-bzip2
PKG_VERSION:=2.17
PKG_RELEASE:=1

PKG_SOURCE_URL:=http://www.cpan.org/authors/id/R/RU/RURBAN/
PKG_SOURCE:=Compress-Bzip2-$(PKG_VERSION).tar.gz
PKG_MD5SUM:=d8b809f6efe3edb33f81d608c932b2ef

PKG_LICENSE:=GPLv1+ ARTISTIC
PKG_MAINTAINER:=Marcel Denia <naoir@gmx.net>

PKG_BUILD_DIR:=$(BUILD_DIR)/perl/Compress-Bzip2-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-compress-bzip2
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Perl interface to bzip2 compression library
  URL:=http://search.cpan.org/dist/Compress-Bzip2/
  DEPENDS:=perl +libbz2
endef

define Build/Configure
	$(call perlmod/Configure,,BUILD_BZLIB=0)
endef

define Build/Compile
	$(call perlmod/Compile,,)
endef

define Package/perl-compress-bzip2/install
	$(call perlmod/Install,$(1),Compress auto/Compress)
endef


$(eval $(call BuildPackage,perl-compress-bzip2))
