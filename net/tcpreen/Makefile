# Created by: Janos.Mohacsi@bsd.hu
# $FreeBSD$

PORTNAME=	tcpreen
PORTVERSION=	1.4.4
PORTREVISION=	2
CATEGORIES=	net ipv6
MASTER_SITES=	http://www.remlab.net/files/tcpreen/

MAINTAINER=	jmohacsi@bsd.hu
COMMENT=	A simple TCP session re-engineering tool

USE_BZIP2=	yes
GNU_CONFIGURE=	yes
MAN1=		tcpreen.1

DOC_FILES=	AUTHORS NEWS README THANKS TODO

.include <bsd.port.options.mk>

.if ${PORT_OPTIONS:MNLS}
USES+=		gettext
PLIST_SUB+=	NLS=""
.else
CONFIGURE_ARGS+=--disable-nls
PLIST_SUB+=	NLS="@comment "
.endif

post-install:
.if ${PORT_OPTIONS:MDOCS}
	@${MKDIR} ${DOCSDIR}
.for file in ${DOC_FILES}
	@${INSTALL_DATA} ${WRKSRC}/${file} ${DOCSDIR}
.endfor
.endif

.include <bsd.port.mk>
