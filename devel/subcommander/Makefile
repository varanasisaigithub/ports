# Created by: sutra
# $FreeBSD$

PORTNAME=	subcommander
PORTVERSION=	1.2.3
PORTREVISION=	12
CATEGORIES=	devel
MASTER_SITES=	http://subcommander.tigris.org/files/documents/1759/42385/
DISTNAME=	Subcommander-${PORTVERSION}

MAINTAINER=	cyberbotx@cyberbotx.com
COMMENT=	Qt based multiplatform subversion client, diff & merge tool

LIB_DEPENDS=	neon.27:${PORTSDIR}/www/neon29 \
		boost_thread:${PORTSDIR}/devel/boost-libs \
		svn_client-1.0:${PORTSDIR}/devel/subversion16

CONFLICTS_BUILD=subversion-1.7.[0-9]*

WRKSRC=	${WRKDIR}/${PORTNAME}-${PORTVERSION}

GNU_CONFIGURE=	yes
USE_GMAKE=	yes
USE_QT_VER=	3
CONFIGURE_ARGS+=--with-boost=${LOCALBASE} --with-neon=${LOCALBASE} \
		--with-subversion=${LOCALBASE}
CONFIGURE_ENV=	QTDIR=${LOCALBASE}
CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib -pthread

NO_LATEST_LINK=	yes

.include <bsd.port.mk>
