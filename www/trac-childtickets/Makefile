# New ports collection makefile for:	trac-childtickets
# Date created:				2012-08-16
# Whom:					Radim Kolar <hsn@sendmail.cz>
#
# $FreeBSD$
#

PORTNAME=	childtickets
PORTVERSION=	2.5.2
CATEGORIES=	www devel python
MASTER_SITES=	http://schema.filez.com/distfiles/
PKGNAMEPREFIX=	trac-

MAINTAINER=	hsn@sendmail.cz
COMMENT=	Support for having child-tickets in Trac

LICENSE=	BSD

RUN_DEPENDS+=	trac>=0.12:${PORTSDIR}/www/trac

USE_ZIP=	yes

WRKSRC=		${WRKDIR}/childticketsplugin/0.12

USE_PYTHON=	-2.7
USE_PYDISTUTILS=	easy_install
PYDISTUTILS_PKGNAME=	Tracchildtickets

SUB_FILES=	pkg-message
PLIST_FILES=	%%PYTHON_SITELIBDIR%%/%%PYEASYINSTALL_EGG%%

post-install:
	@${CAT} ${PKGMESSAGE}

.include <bsd.port.mk>
