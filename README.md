<h1 align="center">
    SISGEP
</h1>
<p align="center">
    Repositório base para desenvolvimento do sistema de gerenciamento de produtos SISGEP.
</p>

## 1. Projeto

O **SISGEP** é um app baseado em *php* e é executado em um servidor *Apache* com persistencia de dados em um banco *mariadb*. Ainda contamos com o auxílio do *phpmyadmin* para gereciamento do banco de dados através de uma interface gráfica no navegador.

O presente repositório tem por objetivo executar essa aplicação através da utilização da ferramenta [Docker](https://www.docker.com/). O Docker fornece os recursos necessários para a criação e gereciamento de *images* e *containers*, ferramentas poderosas na criação de ambientes de execução e desenvolvimento.

As imagens utilizadas para gerar o ambiente de desnvolvimento foram:
- [php:8.2.12-apache](https://hub.docker.com/_/php)
- [mariadb:latest](https://hub.docker.com/_/mariadb)
- [phpmyadmin:latest](https://hub.docker.com/_/phpmyadmin)

### 1.1 Pré-requisitos

Para executar a aplicação será necessário possuir o Docker instalado em sua máquina. Para quaisquer referências, suporte ou ajuda com instalação tente acessar a [documentação oficial do Docker](https://docs.docker.com/) ou a seção [Get started](https://www.docker.com/get-started/) do site oficial do Docker.

## 2. Execução do app

Com o Docker devidamente instalado, faça o clone ou download do repositório para o diretório em que deseja rodar a aplicação.

Feito isso, execute o seguinte comando no terminal dentro do diretório raiz da aplicação:

```bash
docker-compose --project-name sisgep up -d --build
```

Aguarde a inicialização completa dos serviços e acesse o endereço [localhost:8080/login.php](http://localhost:8080/login.php).

Tudo pronto, o **SISGEP** já está rodando.

## 3. *phpMyAdmin*

Para utilizar o phpmyadmin e gerenciar o banco de dados, utilize as credenciais abaixo:
> **Servidor**: db<br>**Usuário**: admin<br>**Senha**: 12345

*Obs.: As credenciais podem ser alteradas e configuradas pelo administrador aqualquer momento através dos arquivos de configurações das imagens e containers.*