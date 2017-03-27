# Elasticsearch, Hebrew, Kibana, Docker

Run Elasticsearch and Kibana with [HebMorph][hebmorph] Hebrew analyzer in Docker.
No installation or configuration required.
Just pull and run.

Currently runs:

- Elasticsearch 2.4.2
- Kibana 4.6
- Analysis-Hebrew 2.4.2

# Run

Requires [docker-compose][compose] for linking between Elasticsearch and Kibana.

Uses the official [Elasticserach][elasticsearch docker]
and [Kibana][kibana docker] images.

```bash
# clone, run, PROFIT.
$ git clone git@github.com:oryband/elk-hebmorph-docker.git
$ cd elk-hebmorph-docker
$ docker-compose up
```

# Configuration

A default [index template][index template] uses HebMorph `hebrew` analyzer
for all new indices by default.

Each image mounts a configuration directory, which you can edit if needed.
The defaults should just work, though.

## Credits

Based on:

- [deviantony/docker-elk][docker-elk]
- [synhershko/elasticsearch-analysis-hebrew][analysis-hebrew]


[hebmorph]: http://code972.com/hebmorph
[docker-elk]: https://github.com/deviantony/docker-elk
[analysis-hebrew]: https://github.com/synhershko/elasticsearch-analysis-hebrew
[compose]: https://www.docker.com/products/docker-compose
[elasticsearch docker]: https://hub.docker.com/_/elasticsearch/
[kibana docker]: https://hub.docker.com/_/kibana/
[index template]: https://www.elastic.co/guide/en/elasticsearch/reference/1.7/indices-templates.html
