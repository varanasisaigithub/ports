# Created by: Christian Laursen <xi@borderworlds.dk>
# $FreeBSD$

PORTNAME=	musiccontrol
PORTVERSION=	0.3
PORTREVISION=	2
CATEGORIES=	audio java
MASTER_SITES=	http://borderworlds.dk/projects/mc/
DISTNAME=	MusicControl-0.3
EXTRACT_SUFX=	.jar
EXTRACT_ONLY=

MAINTAINER=	xi@borderworlds.dk
COMMENT=	An advanced music player

RUN_DEPENDS=	${LOCALBASE}/bin/mpg123:${PORTSDIR}/audio/mpg123 \
		${LOCALBASE}/bin/ogg123:${PORTSDIR}/audio/vorbis-tools \
		${LOCALBASE}/bin/simplemod:${PORTSDIR}/audio/simplemod

USE_JAVA=	yes
JAVA_VERSION=	1.6+
NO_BUILD=	yes
PLIST_FILES=	share/java/classes/MusicControl-${PORTVERSION}.jar bin/musiccontrol

do-install:
	@${MKDIR} ${JAVAJARDIR}
	${INSTALL_DATA} ${DISTDIR}/MusicControl-${PORTVERSION}.jar ${JAVAJARDIR}/
	${SED} 's,%%LOCALBASE%%,${LOCALBASE},g ; s,%%JAVAJARDIR%%,${JAVAJARDIR},g' \
		${FILESDIR}/musiccontrol > ${WRKDIR}/musiccontrol
	${INSTALL_SCRIPT} ${WRKDIR}/musiccontrol ${PREFIX}/bin

.include <bsd.port.mk>
