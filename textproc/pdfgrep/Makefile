# Created by: Michael Ranner <michael@ranner.eu>
# $FreeBSD$

PORTNAME=	pdfgrep
PORTVERSION=	1.3.0
CATEGORIES=	textproc
MASTER_SITES=	SF/${PORTNAME}/${PORTVERSION}/
MASTER_SITE_SUBDIR=	${PORTNAME}

MAINTAINER=	michael@ranner.eu
COMMENT=	A tool to search text in PDF files

LICENSE=	GPLv2

LIB_DEPENDS=	poppler:${PORTSDIR}/graphics/poppler

GNU_CONFIGURE=	yes
USE_GMAKE=	yes
CONFIGURE_ARGS=	poppler_CFLAGS="-I${LOCALBASE}/include -I${LOCALBASE}/include/poppler"

PLIST_FILES=	bin/pdfgrep
MAN1=		pdfgrep.1

.include <bsd.port.mk>
