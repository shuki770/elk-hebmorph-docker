FROM elasticsearch:2.4.2
MAINTAINER Ory Band <oryband@gmail.com>

ENV HEBMORPH_VERSION=2.4.0
ENV ELASTICSEARCH_VERSION=2.4.2
ENV HEBMORPH_FILE hebmorph-lucene-$HEBMORPH_VERSION

# Copy the hspell data files,
COPY ./hspell-data-files /var/lib/hspell-data-files

# install hebmorph plugin
RUN ./bin/plugin install https://bintray.com/synhershko/elasticsearch-analysis-hebrew/download_file?file_path=elasticsearch-analysis-hebrew-2.4.2
