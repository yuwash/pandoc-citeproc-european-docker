FROM yuwash/pandoc-citeproc-european:graphviz
LABEL maintainer "Yushin Washio <yuwash at yandex dot com>"

RUN set -ex \
	&& apt-get update && apt-get install -y --no-install-recommends \
		wget \
	&& rm -rf /var/lib/apt/lists/*
