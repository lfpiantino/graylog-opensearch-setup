# Solução de Problemas Comuns

## Graylog: Datanode is not available
- Verifique se o OpenSearch está escutando em 192.168.x.x:9200
- Ajuste o bind_host no opensearch.yml e reinicie o serviço

## MongoDB: interrupted at shutdown
- Verifique se o arquivo mongod.lock existe em /var/lib/mongodb/
- Apague o lock se necessário e reinicie com `sudo systemctl restart mongod`

## Invalid elasticsearch_version
- Corrija a linha no server.conf para:
```conf
elasticsearch_version = OpenSearch:2.0.0
```
