# Created by: Sergey Skvortsov <skv@protey.ru>
# $FreeBSD$

PORTNAME=	POE-Component-RSS
PORTVERSION=	0.09
CATEGORIES=	devel perl5 textproc
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Module for event based RSS parsing

BUILD_DEPENDS=	p5-POE>=0:${PORTSDIR}/devel/p5-POE \
		p5-XML-RSS>=0:${PORTSDIR}/textproc/p5-XML-RSS
RUN_DEPENDS:=	${BUILD_DEPENDS}

PERL_CONFIGURE=	yes

MAN3=		POE::Component::RSS.3

.include <bsd.port.mk>
