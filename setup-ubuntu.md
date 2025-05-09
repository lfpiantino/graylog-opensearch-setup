# Passo a passo para instalação do Graylog Server com MongoDB e OpenSearch

## 1. Atualização do sistema
```bash
sudo apt update && sudo apt upgrade -y
```

## 2. Instalação do MongoDB
```bash
# Adicionar repositório e instalar
sudo apt install mongodb-org -y
sudo systemctl enable mongod
sudo systemctl start mongod
```

## 3. Instalação do OpenSearch
```bash
# Ajuste o arquivo /etc/opensearch/opensearch.yml conforme necessário
sudo systemctl enable opensearch
sudo systemctl start opensearch
```

## 4. Instalação do Graylog
```bash
# Ajustar /etc/graylog/server/server.conf
sudo systemctl enable graylog-server
sudo systemctl start graylog-server
```

Verifique os serviços com:
```bash
sudo systemctl status mongod
sudo systemctl status opensearch
sudo systemctl status graylog-server
```
