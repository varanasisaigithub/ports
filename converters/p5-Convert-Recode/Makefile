# New ports collection makefile for:	p5-Convert-Recode
# Date created:				17 January 2000
# Whom:					Dmitry Sivachenko <dima@Chg.RU>
#
# $FreeBSD$
#

PORTNAME=	Convert-Recode
PORTVERSION=	1.04
PORTREVISION=	1
CATEGORIES=	converters perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	demon@FreeBSD.org
COMMENT=	Front end to the GNU recode program

BUILD_DEPENDS=	recode:${PORTSDIR}/converters/recode
RUN_DEPENDS=	recode:${PORTSDIR}/converters/recode

PERL_CONFIGURE=	YES

MAN3=		Convert::Recode.3

post-patch:
		${PERL} -pi -e 's#recode -\$$#${LOCALBASE}/bin/recode -\$$#' \
		${WRKSRC}/Recode.pm

.include <bsd.port.mk>
