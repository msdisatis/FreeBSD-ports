# Created by: Po-Chuan Hsieh <sunpoet@FreeBSD.org>
# $FreeBSD$

PORTNAME=	pew
PORTVERSION=	1.1.5
CATEGORIES=	devel python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Tool to manage multiple virtualenvs

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}virtualenv>=1.11:devel/py-virtualenv@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}virtualenv-clone>=0.2.5:devel/py-virtualenv-clone@${PY_FLAVOR}

NO_ARCH=	yes
USE_PYTHON=	autoplist concurrent distutils
USES=		python shebangfix

GH_ACCOUNT=	berdario
USE_GITHUB=	yes

SHEBANG_FILES=	pew/shell_config/complete_deploy

.include <bsd.port.pre.mk>

.if ${PYTHON_REL} < 3000
RUN_DEPENDS+=	${PYTHON_PKGNAMEPREFIX}backports.shutil_get_terminal_size>=0:devel/py-backports.shutil_get_terminal_size@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pathlib>=0:devel/py-pathlib@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}shutilwhich>=0:sysutils/py-shutilwhich@${PY_FLAVOR}
.endif

.include <bsd.port.post.mk>
