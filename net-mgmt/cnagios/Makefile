# Created by: Alexander Y. Grigoryev <alexander.4mail@gmail.com>
# $FreeBSD$

PORTNAME=	cnagios
PORTVERSION=	0.30
CATEGORIES=	net-mgmt
MASTER_SITES=	ftp://noc.hep.wisc.edu/src/cnagios/ \
		ftp://noc.hep.wisc.edu/src/cnagios/old-versions/

MAINTAINER=	alexander.4mail@gmail.com
COMMENT=	Curses-based interface for nagios

LICENSE=	ISCL

RUN_DEPENDS=	nagios>=3.0:${PORTSDIR}/net-mgmt/nagios

NAGIOSDIR?=	/var/spool/nagios
ETCDIR=		${PREFIX}/etc/nagios
GNU_CONFIGURE=	YES
CONFIGURE_ARGS=	--with-etc-dir="${ETCDIR}" \
		--with-var-dir="${NAGIOSDIR}" \
		--with-status-file="${NAGIOSDIR}/status.dat" \
		--with-nagios-data=3
USE_PERL5=	YES
ALL_TARGET=	cnagios

MAN1=		cnagios.1

post-install:
	@if [ ! -f ${ETCDIR}/cnagiosrc ]; then \
		${CP} -p ${ETCDIR}/cnagiosrc.sample ${ETCDIR}/cnagiosrc ; \
	fi
	@if [ ! -f ${ETCDIR}/cnagios.help ]; then \
		${CP} -p ${ETCDIR}/cnagios.help.sample ${ETCDIR}/cnagios.help ; \
	fi
	@if [ ! -f ${ETCDIR}/cnagios.pl ]; then \
		${CP} -p ${ETCDIR}/cnagios.pl.sample ${ETCDIR}/cnagios.pl ; \
	fi

.include <bsd.port.mk>
