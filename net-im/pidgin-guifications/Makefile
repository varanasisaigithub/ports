# Created by: ports@c0decafe.net
# $FreeBSD$

PORTNAME=	pidgin-guifications
PORTVERSION=	2.16
PORTREVISION=	5
CATEGORIES=	net-im
MASTER_SITES=	http://downloads.guifications.org/plugins/Guifications2/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Plugin to add msn style "toaster" popups to Pidgin

BUILD_DEPENDS=	${LOCALBASE}/include/pidgin/pidgin.h:${PORTSDIR}/net-im/pidgin
RUN_DEPENDS=	pidgin:${PORTSDIR}/net-im/pidgin

USE_BZIP2=	yes
USE_GMAKE=	yes
USES=        pathfix gettext
USE_GNOME=	gnomeprefix gtk20
GNU_CONFIGURE=	yes
CONFIGURE_ENV=	LIBS="-L${LOCALBASE}/lib"
CPPFLAGS+=	-I${LOCALBASE}/include

.include <bsd.port.pre.mk>

post-extract:
	@${FIND} ${WRKSRC} -name "Makefile.in" | ${XARGS} ${REINPLACE_CMD} \
		-e 's#\([@(]\)PIDGIN_LIBDIR\([@)]\)#\1libdir\2#' \
		-e 's#\([@(]\)PIDGIN_DATADIR\([@)]\)#\1datadir\2#'
	@${REINPLACE_CMD} -e 's|echo aout|echo elf|' ${WRKSRC}/configure

.include <bsd.port.post.mk>
