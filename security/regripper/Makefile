# Created by: antoine@FreeBSD.org
# $FreeBSD$

PORTNAME=	regripper
DISTVERSION=	2.8
CATEGORIES=	security
MASTER_SITES=	GOOGLE_CODE
DISTNAME=	rrv${DISTVERSION}
EXTRACT_SUFX=	.zip

MAINTAINER=	antoine@FreeBSD.org
COMMENT=	Tool for registry analysis in forensics examinations

LICENSE=	GPLv3

RUN_DEPENDS=	p5-Parse-Win32Registry>=0:${PORTSDIR}/devel/p5-Parse-Win32Registry

NO_WRKSUBDIR=	yes
USE_DOS2UNIX=	yes
NO_BUILD=	yes
USE_PERL5_RUN=	yes
PLIST_FILES=	bin/rip.pl

post-patch:
	${REINPLACE_CMD} -e 's|#! c:\\perl\\bin\\perl.exe|#!${PERL}| ; \
		s|plugindir = $$str|plugindir = "${DATADIR}"| ; \
		s|require "plugins/|require "${DATADIR}plugins/|' ${WRKSRC}/rip.pl

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/rip.pl ${PREFIX}/bin

.include <bsd.port.mk>
