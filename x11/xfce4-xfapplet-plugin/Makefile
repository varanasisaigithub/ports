# New ports collection makefile for:	xfapplet plugin for xfce4
# Date created:				29 April 2006
# Whom:					Martin Wilke (miwi@FreeBSD.org)
#
# $FreeBSD$
#

PORTNAME=	xfce4-xfapplet-plugin
PORTVERSION=	0.1.0
PORTREVISION=	16
CATEGORIES=	x11 xfce
MASTER_SITES=	${MASTER_SITE_XFCE}
MASTER_SITE_SUBDIR=/src/panel-plugins/${PORTNAME}/${PORTVERSION:R}
DIST_SUBDIR=	xfce4

MAINTAINER=	xfce@FreeBSD.org
COMMENT=	Xfapplet plugin for Xfce

LIB_DEPENDS=	panelappletmm-2.6:${PORTSDIR}/x11-toolkits/libpanelappletmm

GNU_CONFIGURE=	yes
USE_BZIP2=	yes
USES=		gettext
USE_GMAKE=	yes
USE_GNOME=	gtk20 intltool intlhack orbit2 pkgconfig
USE_XFCE=	configenv libgui libutil panel

.include <bsd.port.mk>
