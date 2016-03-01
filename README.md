gluon rebooter
============

Create a file "modules" with the following content in your site directory:</a>

# Modules

GLUON_SITE_FEEDS="reeboter"<br>
PACKAGES_SSIDCHANGER_REPO=https://github.com/AKA-47/gluon-rebooter.git<br>
PACKAGES_SSIDCHANGER_COMMIT=da8607446385c5980a45ef708ac223c0dfa5f15f<br>

With this done you can add the package gluon-ssid-changer to your site.mk

# site.mk

GLUON_SITE_PACKAGES := \
......
	      gluon-rebooter \
......

DEFAULT_GLUON_RELEASE := 15.12-v2015.2-exp-AKA47-$(shell date '+%Y%m%d')

GLUON_RELEASE ?= $(DEFAULT_GLUON_RELEASE)

GLUON_PRIORITY ?= 0
GLUON_BRANCH ?= experimental
export GLUON_BRANCH

GLUON_TARGET ?= ar71xx-generic
export GLUON_TARGET

GLUON_LANGS ?= de

# gluon-rebooter
