# Ports collection makefile for:	py-libdnet
# Date created:			Nov 2, 2005
# Whom:	      			thierry@pompo.net
#
# $FreeBSD$
#

CATEGORIES=	net python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

COMMENT=	Python module for libdnet

LIB_DEPENDS=	dnet.1:${PORTSDIR}/net/libdnet

NOT_FOR_ARCHS=	ia64
NOT_FOR_ARCHS_REASON_ia64=	fails to build with internal compiler error

MASTERDIR=	${.CURDIR}/../libdnet
INSTALL_WRKSRC=	${WRKSRC}/python
DESCR=		${.CURDIR}/pkg-descr
PLIST=		${.CURDIR}/pkg-plist

LIBDNET_SLAVE=	yes

USE_PYTHON=	yes
CONFIGURE_ARGS=	--with-python
INSTALLS_EGGINFO=	yes
PYDISTUTILS_PKGNAME=	dnet

.if defined(MAINTAINER_MODE)
regression-test: install
	${PYTHON_CMD} ${INSTALL_WRKSRC}/test.py
.endif

.include "${MASTERDIR}/Makefile"
