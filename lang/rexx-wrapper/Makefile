# ex:ts=8
# Ports collection makefile for:	rexx-wrapper
# Date created:			Nov 11, 2003
# Whom:	      			ijliao
#
# $FreeBSD$
#

PORTNAME=	wrapper
PORTVERSION=	2.4
CATEGORIES=	lang
MASTER_SITES=	SF/rexx${PORTNAME}/rexx${PORTNAME}/${PORTVERSION}
PKGNAMEPREFIX=	rexx-
DISTNAME=	RexxWrapper-${PORTVERSION}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	A tool that wraps Rexx source or tokenised code into an executable

BUILD_DEPENDS=	rexx:${PORTSDIR}/lang/rexx-regina
RUN_DEPENDS=	rexx:${PORTSDIR}/lang/rexx-regina

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--with-rexx=regina
DATADIR=	${PREFIX}/share/rexx${PORTNAME}

post-patch:	.SILENT
	@${REINPLACE_CMD} -Ee "/^compiler\.unix/s,'.*','${CC:T}'," \
		-e "s,cc\.cc = .*,cc.${CC:T} = '${CC}'," \
		-e "/ opt/s/-[Og][^' ]?//" \
		-e "s,cflags\. = '(.*)',cflags. = '\1 ${CFLAGS}'," \
		${WRKSRC}/rexxwrap.cmd
	@${REINPLACE_CMD} 's/-compiler=$$(CC/&:T/' ${WRKSRC}/Makefile.in

.include <bsd.port.mk>
