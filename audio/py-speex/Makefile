# New ports collection makefile for: py-speex
# Date created:		3 March 2007
# Whom:			Carl Johan Gustavsson <cjg@bsdmail.org>
#
# $FreeBSD$
#

PORTNAME=	speex
PORTVERSION=	0.2
CATEGORIES=	audio python
MASTER_SITES=	http://www.freenet.org.nz/python/pySpeex/
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}
DISTNAME=	pySpeex-${DISTVERSIONPREFIX}${DISTVERSION}${DISTVERSIONSUFFIX}
DIST_SUBDIR=	python

MAINTAINER=	cjg@bsdmail.org
COMMENT=	Python bindings for the Speex compressor/decompressor audio codec

BUILD_DEPENDS=	pyrex>=0.9.6.2:${PORTSDIR}/devel/pyrex
LIB_DEPENDS=	speex.1:${PORTSDIR}/audio/speex

PLIST_FILES=	%%PYTHON_SITELIBDIR%%/speex.so
USE_PYTHON=	yes
USE_PYDISTUTILS=yes
PYDISTUTILS_PKGVERSION=	1.0

post-patch:
	@${REINPLACE_CMD} -e 's|%%LOCALBASE%%|${LOCALBASE}|g' \
		${WRKSRC}/setup.py

.include <bsd.port.mk>
