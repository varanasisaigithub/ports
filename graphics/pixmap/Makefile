# Created by: jmz
# $FreeBSD$

PORTNAME=	pixmap
PORTVERSION=	2.6
PORTREVISION=	3
CATEGORIES=	graphics
MASTER_SITES=	XCONTRIB/applications/pixmap
DISTNAME=	${PORTNAME}${PORTVERSION}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Pixmap editor based on XPM library

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYRIGHT

# requires rgb.txt
BUILD_DEPENDS=	showrgb:${PORTSDIR}/x11/rgb \
		xrdb:${PORTSDIR}/x11/xrdb

WRKSRC=		${WRKDIR}/${PORTNAME}

USES=		imake
USE_XORG=	xpm xbitmaps x11 xaw xmu xt sm ice xext

CFLAGS+=	-D_X_SENTINEL\(x\)= -D_X_ATTRIBUTE_PRINTF\(x,y\)= \
		-D_X_DEPRECATED= -DUSG

MAN1=		pixmap.1

.include <bsd.port.mk>
