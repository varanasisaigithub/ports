# Created by: J Han <hjh@best.com>
# $FreeBSD$

PORTNAME=	t3d
PORTVERSION=	1.1
PORTREVISION=	2
CATEGORIES=	x11-clocks
MASTER_SITES=	http://bernd-paysan.de/
DISTNAME=	t3d
EXTRACT_SUFX=	.shar.gz

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Clock using flying balls to display the time

LICENSE=	GPLv2

EXTRACT_CMD=		${GZIP_CMD}
EXTRACT_BEFORE_ARGS=	-dc
EXTRACT_AFTER_ARGS=	| ${SH}

NO_WRKSUBDIR=	yes
USES=		imake
USE_XORG=	x11 xext

MAN1=		t3d.1
PLIST_FILES=	bin/t3d

.include <bsd.port.mk>
