# Created by: miwi
# $FreeBSD$

PORTNAME=	kdepim
PORTVERSION=	4.4.11.1
PORTREVISION=	5
CATEGORIES=	deskutils kde ipv6
MASTER_SITES=	${MASTER_SITE_KDE}
MASTER_SITE_SUBDIR=	stable/kdepim-${PORTVERSION}/src
DIST_SUBDIR=	KDE

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Libraries for KDE-PIM applications

LIB_DEPENDS=	gpgme:${PORTSDIR}/security/gpgme \
		sasl2:${PORTSDIR}/security/cyrus-sasl2 \
		boost_thread:${PORTSDIR}/devel/boost-libs \
		qca:${PORTSDIR}/devel/qca
RUN_DEPENDS=	${KDE4_PREFIX}/bin/akonadi_mbox_resource:${PORTSDIR}/deskutils/kdepim44-runtime

LATEST_LINK=	${PORTNAME}44
CONFLICTS_INSTALL=	kdepim-4.[89].*

USE_KDE4=	kdelibs pimlibs \
		akonadi kdeprefix kdehier automoc4 oxygen
USES=		cmake:outsource
USE_BZIP2=	yes
USE_QT4=	qmake_build moc_build rcc_build uic_build \
		corelib dbus designer gui network qt3support sql webkit
USE_OPENLDAP=	yes
USE_LDCONFIG=	yes
MAKE_JOBS_SAFE=	yes

MAN1=		kabcclient.1

#cannot be built with assuan2
CMAKE_ARGS+=	-DWITH_Assuan:BOOL=off

.include <bsd.port.mk>
