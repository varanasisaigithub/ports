# Created by: Cristiano Rolim Pereira <cristianorolim@hotmail.com>
# $FreeBSD$

COMMENT=	RELP input/output module for rsyslog
MASTERDIR=	${.CURDIR}/../rsyslog6-devel

MNAME=	relp
LIB_DEPENDS=	relp.0:${PORTSDIR}/devel/librelp

USEs=		pkgconfig

CONFIGURE_ARGS+=--enable-relp

PLIST_FILES+=	lib/rsyslog/imrelp.la \
		lib/rsyslog/imrelp.so \
		lib/rsyslog/omrelp.la \
		lib/rsyslog/omrelp.so

do-install:
	@${INSTALL_PROGRAM} \
		${WRKSRC}/plugins/omrelp/.libs/omrelp.so ${PREFIX}/lib/rsyslog
	@${INSTALL_DATA} \
		${WRKSRC}/plugins/omrelp/omrelp.la ${PREFIX}/lib/rsyslog
	@${INSTALL_PROGRAM} \
		${WRKSRC}/plugins/imrelp/.libs/imrelp.so ${PREFIX}/lib/rsyslog
	@${INSTALL_DATA} \
		${WRKSRC}/plugins/imrelp/imrelp.la ${PREFIX}/lib/rsyslog
.include "${MASTERDIR}/Makefile"
