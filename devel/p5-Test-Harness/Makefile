# Created by: Shell Hung <shell@shellhung.org>
# $FreeBSD$

PORTNAME=	Test-Harness
PORTVERSION=	3.28
CATEGORIES=	devel perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Run perl standard test scripts with statistics

LICENSE=	ART10 GPLv1
LICENSE_COMB=	dual

PERL_CONFIGURE=	yes

MAN3=		App::Prove.3 \
		App::Prove::State.3 \
		App::Prove::State::Result.3 \
		App::Prove::State::Result::Test.3 TAP::Base.3 \
		TAP::Formatter::Base.3 \
		TAP::Formatter::Color.3 \
		TAP::Formatter::Console.3 \
		TAP::Formatter::Console::ParallelSession.3 \
		TAP::Formatter::Console::Session.3 \
		TAP::Formatter::File.3 \
		TAP::Formatter::File::Session.3 \
		TAP::Formatter::Session.3 \
		TAP::Harness.3 \
		TAP::Harness::Beyond.3 \
		TAP::Object.3 \
		TAP::Parser.3 \
		TAP::Parser::Aggregator.3 \
		TAP::Parser::Grammar.3 \
		TAP::Parser::Iterator.3 \
		TAP::Parser::Iterator::Array.3 \
		TAP::Parser::Iterator::Process.3 \
		TAP::Parser::Iterator::Stream.3 \
		TAP::Parser::IteratorFactory.3 \
		TAP::Parser::Multiplexer.3 \
		TAP::Parser::Result.3 \
		TAP::Parser::Result::Bailout.3 \
		TAP::Parser::Result::Comment.3 \
		TAP::Parser::Result::Plan.3 \
		TAP::Parser::Result::Pragma.3 \
		TAP::Parser::Result::Test.3 \
		TAP::Parser::Result::Unknown.3 \
		TAP::Parser::Result::Version.3 \
		TAP::Parser::Result::YAML.3 \
		TAP::Parser::ResultFactory.3 \
		TAP::Parser::Scheduler.3 \
		TAP::Parser::Scheduler::Job.3 \
		TAP::Parser::Scheduler::Spinner.3 \
		TAP::Parser::Source.3 \
		TAP::Parser::SourceHandler.3 \
		TAP::Parser::SourceHandler::Executable.3 \
		TAP::Parser::SourceHandler::File.3 \
		TAP::Parser::SourceHandler::Handle.3 \
		TAP::Parser::SourceHandler::Perl.3 \
		TAP::Parser::SourceHandler::RawTAP.3 \
		TAP::Parser::Utils.3 \
		TAP::Parser::YAMLish::Reader.3 \
		TAP::Parser::YAMLish::Writer.3 \
		Test::HACKING.3 \
		Test::Harness.3

PLIST_SUB=	P5_PREFIX="p5"
MAN1=		p5prove.1

pre-patch:
	@${MV} ${WRKSRC}/bin/prove ${WRKSRC}/bin/p5prove
	@${REINPLACE_CMD} "s,^bin/prove$$,bin/p5prove," ${WRKSRC}/MANIFEST
	@${REINPLACE_CMD} "s,'bin/prove','bin/p5prove'," ${WRKSRC}/Makefile.PL

post-patch:
	@${REINPLACE_CMD} -e '/INSTALLDIRS/d' ${WRKSRC}/${CONFIGURE_SCRIPT}

.include <bsd.port.mk>
