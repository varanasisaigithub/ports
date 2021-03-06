# Created by: Adam Weinberger <adamw@FreeBSD.org>
# $FreeBSD$
#   $MCom: ports/devel/devhelp/Makefile,v 1.45 2012/09/01 23:02:09 mezz Exp $

PORTNAME=	devhelp
PORTVERSION=	2.32.0
PORTREVISION=	3
PORTEPOCH=	1
CATEGORIES=	devel gnome
MASTER_SITES=	GNOME
DIST_SUBDIR=	gnome2

MAINTAINER=	gnome@FreeBSD.org
COMMENT=	Developer help browser for GNOME 2

LIB_DEPENDS=	webkitgtk-1.0:${PORTSDIR}/www/webkit-gtk2 \
		unique-1.0:${PORTSDIR}/x11-toolkits/unique

CONFLICTS=	devhelp-3.[0-9]*

USE_BZIP2=	yes
USE_XORG=	x11
USE_GMAKE=	yes
USES=		pathfix gettext
USE_GNOME=	intlhack gnomeprefix libgnomeui libwnck
USE_AUTOTOOLS=	libtool
GNU_CONFIGURE=	yes
INSTALLS_ICONS=	yes
USE_LDCONFIG=	yes
GCONF_SCHEMAS=	devhelp.schemas
CPPFLAGS+=	${PTHREAD_CFLAGS} -I${LOCALBASE}/include
LDFLAGS+=	${PTHREAD_LIBS} -L${LOCALBASE}/lib

OPTIONS_DEFINE=	GEDIT
GEDIT_DESC=	Enable GEdit plug-in support

.include <bsd.port.options.mk>

.if ${PORT_OPTIONS:MGEDIT}
BUILD_DEPENDS+=	gedit<3.0.0:${PORTSDIR}/editors/gedit
RUN_DEPENDS+=	gedit<3.0.0:${PORTSDIR}/editors/gedit
PLIST_SUB+=	GEDIT=""
.else
PLIST_SUB+=	GEDIT="@comment "
.endif

post-patch:
.if ! ${PORT_OPTIONS:MGEDIT}
	@${REINPLACE_CMD} -e 's|gedit-plugin||' \
		${WRKSRC}/misc/Makefile.in
	@${REINPLACE_CMD} -e 's|-DGTK_DISABLE_SINGLE_INCLUDES||g' \
		${WRKSRC}/src/Makefile.in
.endif

.include <bsd.port.mk>
