FROM debian
LABEL maintainer "Yushin Washio <yuwash at yandex dot com>"

# make is just extra as I often use it for pandoc
RUN set -ex \
	&& apt-get update && apt-get install -y --no-install-recommends \
		pandoc \
		pandoc-citeproc \
		texlive-lang-european \
		texlive-latex-recommended \
		make \
	&& rm -rf /var/lib/apt/lists/*

# mount your project directory here
WORKDIR /project
