# New ports collection makefile for:	p5-WWW-Google-News
# Date created:		2006-07-17
# Whom:			Tsung-Han Yeh <snowfly@yuntech.edu.tw>
#
# $FreeBSD$
#

PORTNAME=	WWW-Google-News
PORTVERSION=	0.12
PORTREVISION=	1
CATEGORIES=	www perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	snowfly@yuntech.edu.tw
COMMENT=	Access to Google's News Service (Not Usenet)

BUILD_DEPENDS=	p5-URI>=0:${PORTSDIR}/net/p5-URI \
		p5-XML-Atom>=0:${PORTSDIR}/textproc/p5-XML-Atom \
		p5-libwww>=0:${PORTSDIR}/www/p5-libwww
RUN_DEPENDS:=	${BUILD_DEPENDS}

PERL_CONFIGURE=	yes

MAN3=		WWW::Google::News.3

.include <bsd.port.mk>
