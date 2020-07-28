Guide

Set xpack to false in elasticsearch.yml

Enter elastic container and generate certs

bin/elasticsearch-certutil ca

 bin/elasticsearch-certutil cert --ca elastic-stack-ca.p12

Get out of the elastic container and copy them to host

 docker cp <elasticsearch_container>:/usr/share/elasticsearch/elastic-certificates.p12 .

 docker cp <elasticsearch_container>:/usr/share/elasticsearch/elastic-stack-ca.p12 .

Enter elastic container again and generate passwords for every tool

 bin/elasticsearch-setup-passwords auto

Default elastic user: elastic

Use Default elastic user in kibana login screen in order to have full access

Generated Passwords

Changed password for user apm_system
PASSWORD apm_system = 06aQWcr6agWRQcvgdKZ6

Changed password for user kibana
PASSWORD kibana = j0utCig1DT12yIWnKjy7

Changed password for user logstash_system
PASSWORD logstash_system = WGAjvmkMTIBueCMgc0HF

Changed password for user beats_system
PASSWORD beats_system = 5Jv41EdtR1SAvW0ElUuF

Changed password for user remote_monitoring_user
PASSWORD remote_monitoring_user = L2qMZpjfYh7yn7X9JH5b

Changed password for user elastic
PASSWORD elastic = nUk1MamJZDYfrXorYtZp


