# New ports collection makefile for:	p5-WWW-Mechanize-GZip
# Date created:				21 Apr 2009
# Whom:					Cheng-Lung Sung <clsung@FreeBSD.org>
#
# $FreeBSD$
#

PORTNAME=	WWW-Mechanize-GZip
PORTVERSION=	0.12
PORTREVISION=	1
CATEGORIES=	www perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Use WWW::Mechanize by requesting gzip-compression from the webserver

RUN_DEPENDS=	p5-WWW-Mechanize>=0:${PORTSDIR}/www/p5-WWW-Mechanize
BUILD_DEPENDS=	p5-WWW-Mechanize>=0:${PORTSDIR}/www/p5-WWW-Mechanize

PERL_CONFIGURE=	yes

MAN3=	WWW::Mechanize::GZip.3

.include <bsd.port.mk>
