# Created by: Arjan van Leeuwen <avleeuwen@piwebs.com>
# $FreeBSD$

PORTNAME=	cube
DISTVERSION=	2005_08_29
PORTREVISION=	11
CATEGORIES=	games
MASTER_SITES=	SF/${PORTNAME}/${PORTNAME}/${DISTVERSION}
DISTFILES=	${CUBE_DATA} ${CUBE_SRC}
EXTRACT_ONLY=	${CUBE_SRC}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	OpenGL 3D FPS (first person shooter) game

BUILD_DEPENDS=	${LOCALBASE}/lib/libenet.a:${PORTSDIR}/net/enet

USE_ZIP=	yes
USE_DOS2UNIX=	yes
USE_GMAKE=	yes
ALL_TARGET=	#
MAKE_JOBS_SAFE=	yes

CFLAGS+=	-fsigned-char
WRKSRC=		${WRKDIR}/${PORTNAME}_source/src

SUB_FILES=	cube_client cube_server

CUBE_DATA=	${PORTNAME}_${DISTVERSION}_unix.tar.gz
CUBE_SRC=	${PORTNAME}_${DISTVERSION}_src.zip

OPTIONS_DEFINE=	OPTIMIZED_CFLAGS DOCS
OPTIONS_MULTI=	FLAVOR
OPTIONS_MULTI_FLAVOR=	CLIENT SERVER
OPTIONS_DEFAULT=	CLIENT SERVER

FLAVOR_DESC=	Clients and servers
CLIENT_DESC=	Build client
SERVER_DESC=	Build dedicated server

.include <bsd.port.options.mk>

.if ${PORT_OPTIONS:MCLIENT}
USE_GL=		glu
USE_SDL=	image mixer sdl
ALL_TARGET+=	client
CUBE_BIN+=	client
PLIST_SUB+=	CLIENT=""
.else
PLIST_SUB+=	CLIENT="@comment "
.endif

.if ${PORT_OPTIONS:MSERVER}
ALL_TARGET+=	server
CUBE_BIN+=	server
PLIST_SUB+=	SERVER=""
.else
PLIST_SUB+=	SERVER="@comment "
.endif

.if ${PORT_OPTIONS:MOPTIMIZED_CFLAGS}
CFLAGS+=	-O3 -fomit-frame-pointer
.endif

post-extract:
	@${TAR} zxf ${DISTDIR}/${CUBE_DATA} -C ${WRKDIR}

do-install:
.for f in ${CUBE_BIN}
	${INSTALL_SCRIPT} ${WRKDIR}/cube_${f} ${PREFIX}/bin
	${INSTALL_PROGRAM} ${WRKSRC}/cube_${f} ${PREFIX}/libexec
.endfor
	@${MKDIR} ${DATADIR}
	@(cd ${WRKDIR}/cube && ${COPYTREE_SHARE} "data packages" ${DATADIR})
	${INSTALL_DATA} ${WRKDIR}/cube/autoexec.cfg ${DATADIR}
.if ${PORT_OPTIONS:MDOCS}
	@${MKDIR} ${DOCSDIR}
	${INSTALL_DATA} ${WRKDIR}/cube/readme.html ${DOCSDIR}
	@(cd ${WRKDIR}/cube/docs && ${COPYTREE_SHARE} . ${DOCSDIR})
.endif

.include <bsd.port.mk>
