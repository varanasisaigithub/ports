# New ports collection makefile for:	HTTP::Headers::Fast
# Date created:		12 Feb 2009
# Whom:			Jun Kuriyama <kuriyama@FreeBSD.org>
#
# $FreeBSD$
#

PORTNAME=	HTTP-Headers-Fast
PORTVERSION=	0.16
CATEGORIES=	www perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	kuriyama@FreeBSD.org
COMMENT=	Perl extension for faster implementation of HTTP::Headers

RUN_DEPENDS=	\
	p5-libwww>=0:${PORTSDIR}/www/p5-libwww
BUILD_DEPENDS:=	${RUN_DEPENDS}
TEST_DEPENDS=	p5-Test-Requires>0:${PORTSDIR}/devel/p5-Test-Requires

PERL_MODBUILD=	yes

MAN3=		HTTP::Headers::Fast.3

.include <bsd.port.mk>
