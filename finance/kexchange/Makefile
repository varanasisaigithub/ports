# New ports collection makefile for:	kexchange
# Date created:				17 October 2003
# Whom:					Adam Weinberger <adamw@FreeBSD.org>
#
# $FreeBSD$
#

PORTNAME=	kexchange
PORTVERSION=	1.0
PORTREVISION=	10
CATEGORIES=	finance kde
MASTER_SITES=	SF

MAINTAINER=	ports@FreeBSD.org
COMMENT=	KDE currency converter

DEPRECATED=	Depends on QT3; unmaintained
EXPIRATION_DATE=	2013-07-01

USE_KDELIBS_VER=3
USE_AUTOTOOLS=	libtool

post-patch:
	@${REINPLACE_CMD} -e 's|-O2||g' ${WRKSRC}/${CONFIGURE_SCRIPT}

.include <bsd.port.mk>
