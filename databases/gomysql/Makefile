# Created by: Wen Heping <wen@FreeBSD.org
# $FreeBSD$

PORTNAME=	gomysql
PORTVERSION=	0.3.2
PORTREVISION=	3
CATEGORIES=	databases
MASTER_SITES=	LOCAL/wen
DISTNAME=	Philio-GoMySQL-${PORTVERSION}-0-g3c1f411

MAINTAINER=	wen@FreeBSD.org
COMMENT=	A MySQL client library written in Go

BROKEN=		Does not compile with go1

WRKSRC=		${WRKDIR}/Philio-GoMySQL-f1112aa
PLIST_FILES=	${GO_LIBDIR}/mysql.a

.include <bsd.port.pre.mk>
.include "${PORTSDIR}/lang/go/files/bsd.go.mk"
.include <bsd.port.post.mk>
