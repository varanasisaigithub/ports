# New ports collection makefile for:   p5-XML-ApacheFOP
# Date created:                        27 Feb 2006
# Whom:                                Simun Mikecin <numisemis@yahoo.com>
#
# $FreeBSD$
#

PORTNAME=	XML-ApacheFOP
PORTVERSION=	0.03
PORTREVISION=	2
CATEGORIES=	print perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	numisemis@yahoo.com
COMMENT=	Access Apache FOP from Perl to create PDF files using XSL-FO

BUILD_DEPENDS=	p5-Java>=0:${PORTSDIR}/devel/p5-Java \
		${LOCALBASE}/share/java/fop/build/fop.jar:${PORTSDIR}/textproc/fop
RUN_DEPENDS:=	${BUILD_DEPENDS}

PERL_CONFIGURE=	yes

MAN3=		XML::ApacheFOP.3

.include <bsd.port.mk>
