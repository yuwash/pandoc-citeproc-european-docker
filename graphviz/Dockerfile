FROM yuwash/pandoc-citeproc-european
LABEL maintainer "Yushin Washio <yuwash at yandex dot com>"

RUN set -ex \
	&& apt-get update && apt-get install -y --no-install-recommends \
		python-pygraphviz \
		ghostscript \
	&& rm -rf /var/lib/apt/lists/*

ENV PANDOCFILTERS_PATH=$HOME/pandocfilters

RUN set -ex \
	&& apt-get update && apt-get install -y --no-install-recommends \
		git \
		python-pip \
		python-setuptools \
	&& git clone --depth 1 \
		https://github.com/jgm/pandocfilters $PANDOCFILTERS_PATH \
	&& pip install -e \
		$PANDOCFILTERS_PATH \
	&& apt-get purge -y --auto-remove \
		git \
		python-setuptools \
	&& rm -rf /var/lib/apt/lists/*

# fix for the missing BoundingBox error happening with pdf
RUN sed -ie 's/latex="pdf"/latex="eps"/' \
	$PANDOCFILTERS_PATH/examples/graphviz.py
