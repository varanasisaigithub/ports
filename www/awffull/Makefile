# Created by: Chadwick Sorrell chad@wickdev.com
# $FreeBSD$

PORTNAME=	awffull
PORTVERSION=	3.10.2
PORTREVISION=	8
CATEGORIES?=	www
MASTER_SITES=	http://www.stedee.id.au/files/

MAINTAINER?=	chad@wickdev.com
COMMENT=	AWFFull is a webserver log analysis tool forked from Webalizer

BUILD_DEPENDS=	${LOCALBASE}/lib/X11/fonts/bitstream-vera/Vera.ttf:${PORTSDIR}/x11-fonts/bitstream-vera
LIB_DEPENDS=	gd.4:${PORTSDIR}/graphics/gd \
		png15:${PORTSDIR}/graphics/png \
		pcre.3:${PORTSDIR}/devel/pcre
RUN_DEPENDS:=	${BUILD_DEPENDS}

CONFLICTS?=	ja-awffull-[0-9]*

FONTDEFAULT?=	${LOCALBASE}/lib/X11/fonts/bitstream-vera/VeraBd.ttf
FONTLABEL?=	${LOCALBASE}/lib/X11/fonts/bitstream-vera/Vera.ttf

OPTIONS_DEFINE=	GEOIP

USES=		gettext iconv

GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=--with-font-default=${FONTDEFAULT} \
		--with-font-label=${FONTLABEL} \
		--with-etcdir=${PREFIX}/etc

CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib

MAN1=		awffull.1
MAN5=		awffull.conf.5

.include <bsd.port.options.mk>

.if ${PORT_OPTIONS:MGEOIP}
LIB_DEPENDS+=	GeoIP.5:${PORTSDIR}/net/GeoIP
CONFIGURE_ARGS+=--enable-geoip
.else
CONFIGURE_ARGS+=--disable-geoip
.endif

.include <bsd.port.mk>
