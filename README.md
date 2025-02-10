# 🚀 Jenkins com Docker Compose

Este repositório fornece um ambiente pronto para uso do **Jenkins** com **Docker Compose**, permitindo sua inicialização com um único comando.

## 📌 Requisitos

Antes de iniciar, certifique-se de ter os seguintes itens instalados no seu sistema:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- Git (opcional, caso deseje clonar este repositório)

## 📂 Estrutura do Repositório

```
jenkins-docker-setup/
│── Dockerfile            # Personalização da imagem do Jenkins
│── docker-compose.yml    # Configuração do ambiente Docker
│── README.md             # Documentação (este arquivo)
```

## 🛠 Como Usar

### 1️⃣ Clonar o repositório (opcional)
Se ainda não clonou o repositório, execute:
```sh
git clone https://github.com/seu-usuario/jenkins-docker-setup.git
cd jenkins-docker-setup
```

### 2️⃣ Subir o ambiente
Agora, execute o seguinte comando para iniciar o Jenkins:
```sh
docker-compose up -d
```
Isso iniciará os containers em modo **detached (em segundo plano)**.

### 3️⃣ Acessar o Jenkins
Depois que os containers estiverem rodando, abra o navegador e acesse:
```
http://localhost:8080
```

Para obter a senha inicial do Jenkins, utilize:
```sh
docker exec jenkins-blueocean cat /var/jenkins_home/secrets/initialAdminPassword
```
Copie a senha e cole no assistente de configuração inicial do Jenkins.

### 4️⃣ Parar e remover o ambiente
Se precisar parar os containers, use:
```sh
docker-compose down
```
Isso desligará e removerá os containers, mas os dados do Jenkins continuarão salvos no volume Docker.

## 📦 Personalização
Se quiser modificar a versão do Jenkins ou adicionar mais plugins, edite o `Dockerfile` e recompile a imagem com:
```sh
docker build -t meu-jenkins-personalizado .
```

## 📝 Licença
Este repositório está sob a licença MIT. Sinta-se à vontade para utilizar e modificar como preferir! 🎉

