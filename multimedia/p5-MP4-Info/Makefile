# New ports collection makefile for:	p5-MP4-Info
# Date created:		10-Dec-2005
# Whom:			Lars Eggert <lars.eggert@gmx.net>
#
# $FreeBSD$
#

PORTNAME=	MP4-Info
PORTVERSION=	1.13
CATEGORIES=	multimedia perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Fetch info from MPEG-4 files

BUILD_DEPENDS=	p5-IO-String>=0:${PORTSDIR}/devel/p5-IO-String \
		p5-Encode>=2.10:${PORTSDIR}/converters/p5-Encode
RUN_DEPENDS:=	${BUILD_DEPENDS}

PERL_CONFIGURE=	yes

MAN3=	MP4::Info.3

.include <bsd.port.mk>
