FROM openjdk:jre-slim
LABEL maintainer "Yushin Washio <yuwash at yandex dot com>"

# make is just extra as I often use it for pandoc
RUN set -ex \
	&& apt-get update && apt-get install -y --no-install-recommends \
		pandoc \
		pandoc-citeproc \
		texlive-lang-european \
		texlive-lang-czechslovak \
		texlive-lang-english \
		texlive-lang-french \
		texlive-lang-german \
		texlive-lang-polish \
		texlive-lang-portuguese \
		texlive-lang-spanish \
		texlive-latex-recommended \
		biber \
		texlive-bibtex-extra \
		texlive-latex-extra \
		texlive-fonts-recommended \
		lmodern \
		make \
	&& rm -rf /var/lib/apt/lists/*

# mount your project directory here
WORKDIR /project
