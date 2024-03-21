# Instalação do Rundeck em docker com persistência de dados

O Rundeck pode ser executado em um contêiner Docker, facilitando a implantação e a escalabilidade. Este guia fornece instruções para instalar o Rundeck em um ambiente Docker com persistência de dados usando volumes Docker para armazenar configurações e histórico.

## Instalação do Rundeck em Docker 
1. Abra um terminal. 
2. Execute o seguinte comando para baixar a imagem Docker oficial do Rundeck:

```bash
docker pull rundeck/rundeck:4.17.0
``` 

## Persistência de Dados

Para garantir a persistência de dados, é recomendável usar volumes Docker para armazenar configurações e dados do Rundeck. Isso permite que você atualize ou reinstale o contêiner sem perder suas configurações. 

1. Crie volumes Docker para persistir dados do Rundeck:

```bash
docker volume create rundeck-config
docker volume create rundeck-data
``` 
2. Inicie o contêiner, montando os volumes criados:

```bash
docker run -d --name rundeck -p 4440:4440 -v rundeck-config:/home/rundeck/server/config -v rundeck-data:/home/rundeck/server/data rundeck/rundeck:4.17.0
```
## Configuração Inicial do Rundeck 
1. Aguarde alguns minutos para que o Rundeck inicialize completamente. 
2. Acesse o navegador e vá para `http://localhost:4440`. O painel de login do Rundeck deve aparecer. 
3. Faça login com as credenciais padrão (usuário: `admin`, senha: `admin`). 
4. Altere a senha padrão imediatamente após o primeiro login.
## Acesso ao Rundeck

Após a instalação e configuração inicial, o Rundeck está pronto para uso. Acesse o Rundeck através do navegador no endereço `http://localhost:4440`.

## Conclusão

Agora você pode começar a utilizar o Rundeck para automação de tarefas e gerenciamento de operações.

Consulte a [documentação oficial do Rundeck](https://docs.rundeck.com/)  para obter informações detalhadas sobre como configurar e usar o Rundeck de acordo com suas necessidades específicas.
