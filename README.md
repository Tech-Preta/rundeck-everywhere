- # Rundeck Anywhere 

Este documento fornece instruções detalhadas sobre como instalar o Rundeck Anywhere em diferentes ambientes. 

Escolha a opção de instalação que melhor se adequa às suas necessidades

Siga os passos abaixo para instalar o Rundeck localmente.

[Guia de Instalação Local](https://gitlab.com/jackexperts/clientes/globalweb/projetonoc-centralizado/rundeck-anywhere/-/blob/main/local/install-local.md)

## Instalação via Docker

### Requisitos do Sistema

Certifique-se de ter o Docker instalado em seu sistema.

[Instalando o Docker](https://gitlab.com/jackexperts/clientes/globalweb/projetonoc-centralizado/rundeck-anywhere/-/blob/main/docker/install-docker.md) 

### Procedimento de Instalação com Docker

Siga os passos abaixo para instalar o Rundeck usando Docker.

[Guia de Instalação com Docker](https://gitlab.com/jackexperts/clientes/globalweb/projetonoc-centralizado/rundeck-anywhere/-/blob/main/docker/install-rundeck.md) 

## Instalação via Docker Compose

### Requisitos do Sistema

Certifique-se de ter o Docker Compose instalado em seu sistema.

[Requisitos do Sistema](https://gitlab.com/jackexperts/clientes/globalweb/projetonoc-centralizado/rundeck-anywhere/-/blob/main/docker/install-docker.md) 

### Procedimento de Instalação com Docker Compose

Siga os passos abaixo para instalar o Rundeck usando Docker Compose. Certifique-se de escolher o diretório com a stack desejada:

```
cd docker-compose/ldap

docker compose up -d
```


## Instalação via Manifestos do Kubernetes

### Requisitos do Sistema

Certifique-se de ter um cluster Kubernetes em execução e kubectl configurado.

### Procedimento de Instalação com Manifestos do Kubernetes

Siga os passos abaixo para instalar o Rundeck usando manifestos do Kubernetes.

```
cd kubernetes/manifests

kubectl apply -f .

```

## Instalação via Helm
### Requisitos do Sistema

Certifique-se de ter o Helm instalado e configurado em seu ambiente.


### Procedimento de Instalação com Helm

Siga os passos abaixo para instalar o Rundeck Anywhere usando Helm.

[Guia de Instalação com Helm](https://gitlab.com/jackexperts/clientes/globalweb/projetonoc-centralizado/rundeck-anywhere/-/blob/main/kubernetes/helm/rundeck/README.md).


```
git clone https://gitlab.com/jackexperts/clientes/globalweb/projetonoc-centralizado/rundeck-anywhere.git

cd helm/rundeck

helm install nome_do_release -n nome_do_namespace .

```

Escolha a opção de instalação apropriada com base nas suas necessidades e ambiente. Se encontrar problemas ou tiver dúvidas, consulte a [documentação oficial do Rundeck](https://docs.rundeck.com/)  ou entre em contato com a equipe de suporte.
