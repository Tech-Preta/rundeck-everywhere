# Instalando o Rundeck

O Rundeck depende do Java 11 ou Java 8. Os pacotes Java 14 satisfarão essa dependência, no entanto, o Rundeck não funcionará corretamente com eles. Recomenda-se instalar manualmente o pacote openjdk-11-jre-headless.

```
sudo apt-get install openjdk-11-jre-headless
```

## Instalação rápida com apt
```
curl https://raw.githubusercontent.com/rundeck/packaging/main/scripts/deb-setup.sh 2> /dev/null | sudo bash -s rundeck
```

## Instalação manual com apt
Importe a chave de assinatura do repositório:

```
curl -L https://packages.rundeck.com/pagerduty/rundeck/gpgkey | sudo apt-key add -
```

Adicione o seguinte ao /etc/apt/sources.list.d/rundeck.list, substituindo as entradas existentes:

```
deb https://packages.rundeck.com/pagerduty/rundeck/any/ any main
deb-src https://packages.rundeck.com/pagerduty/rundeck/any/ any main

```

Atualize o cache do apt e instale:

```
sudo apt-get update
sudo apt-get install rundeck
```

# Iniciando o Rundeck

```
sudo systemctl daemon-reload
sudo service rundeckd start
```

Para verificar se o serviço foi iniciado corretamente, acompanhe os logs:

```
tail -f /var/log/rundeck/service.log
```

O serviço está pronto quando você visualizar algo semelhante a:


```
Grails application running at http://localhost:4440 in environment: production
```

# Fazendo login pela primeira vez
Acesse http://localhost:4440/ em um navegador.
Faça login com o nome de usuário "admin" e a senha "admin".
O Rundeck está agora instalado e em execução!