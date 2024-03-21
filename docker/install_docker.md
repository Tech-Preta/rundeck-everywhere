# Instalação do Docker

O Docker é uma plataforma de código aberto que permite automatizar a implantação, escalonamento e gerenciamento de aplicativos em contêineres. Este guia fornece instruções passo a passo para instalar o Docker em diferentes sistemas operacionais.

## Pré-requisitos

Antes de começar, certifique-se de que seu sistema atende aos seguintes requisitos: 
- **Linux** : Kernel versão 3.10 ou superior. 
- **macOS** : macOS El Capitan 10.11 ou superior. 
- **Windows** : Versão Windows 10 Pro, Enterprise ou Education.
## Instalação do Docker no Linux 
1. Abra um terminal. 
2. Execute o seguinte comando para instalar as dependências necessárias:

```bash
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common
``` 
3. Adicione a chave GPG oficial do Docker:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
``` 
4. Adicione o repositório do Docker:

```bash
echo "deb [signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
``` 
5. Atualize os pacotes e instale o Docker:

```bash
sudo apt-get update

curl https://get.docker.com | bash

curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose

ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose 

systemctl enable docker

systemctl restart docker
``` 

6. Adicione seu usuário ao grupo `docker` para evitar a necessidade de usar `sudo` ao executar comandos Docker:

```bash
sudo usermod -aG docker $USER
``` 

7. Faça logout e login novamente para aplicar as alterações.

## Instalação do Docker no macOS 
1. Baixe o instalador do Docker para macOS [aqui](https://docs.docker.com/desktop/install/mac-install/) . 
2. Siga as instruções do instalador. 
3. Após a instalação, abra o Docker Desktop.
## Instalação do Docker no Windows 

1. Baixe o instalador do Docker para Windows [aqui](https://docs.docker.com/desktop/install/windows-install/). 

2. Siga as instruções do instalador. 
3. Após a instalação, abra o Docker Desktop.

## Verificando a instalação

Para verificar se a instalação foi bem-sucedida, abra um terminal e execute o seguinte comando:

```bash
docker --version
```

Você deve ver a versão do Docker instalada.
## Executando o primeiro contêiner

Para testar sua instalação, execute o seguinte comando para baixar e executar um contêiner de exemplo:

```bash
docker run hello-world
```

Se a instalação estiver correta, você verá uma mensagem indicando que seu sistema está configurado corretamente.
## Conclusão

A instalação do Docker foi concluída com sucesso! Agora você pode começar a criar, implantar e gerenciar aplicativos em contêineres. Consulte a [documentação oficial do Docker](https://docs.docker.com/)  para aprender mais sobre como usar o Docker.