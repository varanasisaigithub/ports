# New ports collection makefile for:	p5-WWW-WebArchive
# Date created:		2006-08-20
# Whom:			Gea-Suan Lin <gslin@gslin.org>
#
# $FreeBSD$
#

PORTNAME=	WWW-WebArchive
PORTVERSION=	0.50
CATEGORIES=	www perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	gslin@gslin.org
COMMENT=	Retrieve old versions of public web pages from various web archives

RUN_DEPENDS=	p5-App-Options>=0:${PORTSDIR}/devel/p5-App-Options \
		p5-App-Trace>=0:${PORTSDIR}/devel/p5-App-Trace \
		p5-WWW-Mechanize>=0:${PORTSDIR}/www/p5-WWW-Mechanize

PERL_CONFIGURE=	yes

MAN3=		WWW::WebArchive.3 WWW::WebArchive::Agent.3 \
		WWW::WebArchive::WaybackMachine.3

.include <bsd.port.mk>
