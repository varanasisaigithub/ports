# $FreeBSD$

PORTNAME=	rocs
PORTVERSION=	${KDE4_VERSION}
CATEGORIES=	math kde
MASTER_SITES=	${MASTER_SITE_KDE}
MASTER_SITE_SUBDIR=	${KDE4_BRANCH}/${PORTVERSION}/src
DIST_SUBDIR=	KDE/${PORTVERSION}

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE Graph theory IDE

LIB_DEPENDS=	boost_thread:${PORTSDIR}/devel/boost-libs

CONFLICTS=	kdeedu-4.[0-6].*

USE_KDE4=	kdehier kdelibs kdeprefix automoc4
USES=		cmake:outsource
USE_QT4=	gui qtestlib script scripttools webkit xml \
		moc_build qmake_build rcc_build uic_build
USE_XZ=		yes
USE_LDCONFIG=	yes
MAKE_JOBS_SAFE=	yes

.include <bsd.port.mk>
