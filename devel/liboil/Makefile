# New ports collection makefile for:	liboil
# Date created:				Nov 24, 2004
# Whom:					ijliao
#
# $FreeBSD$
#    $MCom: ports/devel/liboil/Makefile,v 1.7 2008/03/23 06:57:57 marcus Exp $
#      $Id: Makefile 23 2006-10-25 14:24:32Z buhnux $

PORTNAME=	liboil
PORTVERSION=	0.3.17
CATEGORIES=	devel
MASTER_SITES=	http://liboil.freedesktop.org/download/

MAINTAINER=	mm@FreeBSD.org
COMMENT=	Library of optimized inner loops

LICENSE=	BSD
LICENSE_FILE=	${WRKSRC}/COPYING

USE_GCC=	any
USE_GNOME=	pkgconfig gnomehack ltverhack
USE_AUTOTOOLS=	libtool
USE_LDCONFIG=	yes
CONFIGURE_ARGS=	--disable-gtk-doc \
		--disable-glib
CFLAGS:=	${CFLAGS:N-O*} -O2

.if ${CC:T:M*clang*}
CFLAGS+=	-fheinous-gnu-extensions
.endif

.include <bsd.port.pre.mk>

post-patch:
	@${REINPLACE_CMD} -e 's|\\$$(libdir)/pkgconfig|${PREFIX}/libdata/pkgconfig|' \
		${WRKSRC}/configure
	@${REINPLACE_CMD} -e 's|<stdint\.h|<inttypes.h|g' \
		${WRKSRC}/liboil/liboiltypes.h \
		${WRKSRC}/liboil/liboilprofile.h \
		${WRKSRC}/liboil/liboil.h

.include <bsd.port.post.mk>
