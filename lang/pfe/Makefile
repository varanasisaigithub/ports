# New ports collection makefile for:    pfe-devel
# Date created:         29 October 2000
# Whom:                 patrick
#
# $FreeBSD$
#

PORTNAME=	pfe
PORTVERSION=	0.33.71
CATEGORIES=	lang
MASTER_SITES=	SF

MAINTAINER=	johans@FreeBSD.org
COMMENT=	Implementation of ANSI Forth

USE_BZIP2=	yes
USE_PERL5_BUILD=yes
USE_GCC=	4.2+
USE_GMAKE=	yes
USE_AUTOTOOLS=	libtool
LIBTOOLFILES=	pfe/configure
MAKE_ARGS=	pkgconfigdir="${PREFIX}/libdata/pkgconfig"

MAN1=		pfe.1

.include <bsd.port.pre.mk>

.if ${ARCH} == "powerpc"
BROKEN=		does not compile
.endif

post-patch:
	@${REINPLACE_CMD} -e 's|^CFLAGS=|#CFLAGS=|g ; \
		 s|-O$$opt_level||g' ${WRKSRC}/pfe/configure

.include <bsd.port.post.mk>
