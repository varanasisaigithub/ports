# Created by: Yuri Pankov <yuri.pankov@gmail.com>
# $FreeBSD$

PORTNAME=	glipper
PORTVERSION=	1.0
PORTREVISION=	9
CATEGORIES=	deskutils gnome
MASTER_SITES=	SF/${PORTNAME}/${PORTNAME}/${PORTNAME}%20${PORTVERSION}

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Clipboard manager for the GNOME panel

USE_BZIP2=	yes
USE_GMAKE=	yes
USES=		pathfix gettext iconv
USE_GNOME=	gnomeprefix intltool pygnomedesktop pygnomeextras
USE_PYTHON=	2.5+
INSTALLS_ICONS=	yes
GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--libdir=${PREFIX}/libexec

GCONF_SCHEMAS=	glipper.schemas

post-patch:
	@${REINPLACE_CMD} -e 's|glib/gtypes.h|glib.h|g' \
		${WRKSRC}/glipper/keybinder/tomboykeybinder.h

.include <bsd.port.mk>
