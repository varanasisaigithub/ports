# New ports collection makefile for:	p5-Net-LDAP-Makepath
# Date created:		2008-06-24
# Whom:			Zane C, Bowers <vvelox@vvelox.net>
#
# $FreeBSD$
#

PORTNAME=	Image-Size-FillFullSelect
PORTVERSION=	0.1.0
CATEGORIES=	graphics perl5
MASTER_SITES=	CPAN
MASTER_SITE_SUBDIR=	CPAN:VVELOX
PKGNAMEPREFIX=	p5-

MAINTAINER=	vvelox@vvelox.net
COMMENT=	Pick whether an image fill setting for a image should be fill or full

BUILD_DEPENDS=	p5-Image-Size>=3.230:${PORTSDIR}/graphics/p5-Image-Size
RUN_DEPENDS:=	${BUILD_DEPENDS}

PERL_CONFIGURE=	yes

MAN3=		Image::Size::FillFullSelect.3

.include <bsd.port.mk>
