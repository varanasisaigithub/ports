# New ports collection makefile for:   p5-Apache-ParseFormData
# Date created:                13-Jul-2004
# Whom:                        Jon Nistor <nistor@snickers.org>
#
# $FreeBSD$
#

PORTNAME=	Apache-ParseFormData
PORTVERSION=	0.09
PORTREVISION=	1
CATEGORIES=	www perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	nistor@snickers.org
COMMENT=	Module allows you to easily decode/parse form and query data

BUILD_DEPENDS=	${APACHE_PKGNAMEPREFIX}mod_perl2>=0:${PORTSDIR}/www/mod_perl2
RUN_DEPENDS:=	${BUILD_DEPENDS}

PERL_CONFIGURE=	yes
USE_APACHE=	22+

MAN3=		Apache::ParseFormData.3

post-patch:
	@${FIND} ${WRKSRC} -name "*.orig" -delete

.include <bsd.port.mk>
