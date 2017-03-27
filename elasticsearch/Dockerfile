# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:5.2.2

MAINTAINER Ory Band <oryband@gmail.com>

ENV HEBMORPH_VERSION=5.2.2
ENV HEBMORPH_FILE hebmorph-lucene-$HEBMORPH_VERSION

# install hebmorph plugin
RUN ./bin/elasticsearch-plugin install https://bintray.com/synhershko/elasticsearch-analysis-hebrew/download_file?file_path=elasticsearch-analysis-hebrew-5.2.2.zip

# Copy the hspell data files,
COPY ./hspell-data-files plugins/analysis-hebrew/hspell-data-files

# Disable X-Pack
# see https://www.elastic.co/guide/en/x-pack/current/xpack-settings.html
#     https://www.elastic.co/guide/en/x-pack/current/installing-xpack.html#xpack-enabling
ENV xpack.security.enabled=false
ENV xpack.monitoring.enabled=false
ENV xpack.graph.enabled=false
ENV xpack.watcher.enabled=false