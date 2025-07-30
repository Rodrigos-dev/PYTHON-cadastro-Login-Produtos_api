# 🐍 API de Cadastro, Login e Produtos com Django REST Framework

Este repositório contém uma API robusta desenvolvida com **Python** e **Django REST Framework (DRF)**, com suporte completo a **cadastro de usuários com avatar**, **login com JWT (access e refresh token)**, e **cadastro de produtos por usuário**, utilizando **MySQL** como banco de dados e **Docker** para orquestração de ambiente.

---

## 🚀 Funcionalidades

- ✅ Cadastro de usuários
- 🖼️ Upload de avatar com relação **OneToOne** com o usuário
- 🔐 Autenticação com JWT (access e refresh tokens)
- 📦 Cadastro de produtos com relação **ManyToOne** com o usuário
- 🐳 Ambiente completo com Docker + Docker Compose
- 🗃️ Banco de dados MySQL
- 📦 Relações OneToOne e ManyToOne implementadas

---

## 🧰 Tecnologias Utilizadas

- [Python 3.11+](https://www.python.org/)
- [Django](https://www.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [MySQL](https://www.mysql.com/)
- [Docker & Docker Compose](https://www.docker.com/)
- [JWT Authentication](https://jwt.io/)

---

rodar com Docker

*no .env configure o banco de dados -> host tem que ser 'db'

* 1 crie a tabela no banco de dados
  
* terminal -> docker-compose up -d db

------------------------------------------------
* agora crie um banco de dados 

- docker exec -it mysql-container bash

- mysql -u root -p

- -> digite a senha do seu banco

-CREATE DATABASE python_login_cadastro_produtos

----------------------------------------------------------------

--ou em uma linha de comando apenas para criar o banco 
->docker exec -i nome_do_seu_container_mysql mysql -u seu_usuario -pseu_senha -e "CREATE DATABASE nome_do_seu_banco;"

-----------------------------------------------------------------------

para ver se o banco foi criado

mysql -u root -p -e "SHOW DATABASES;"

----------------------------------------------------------------------

* terminal -> docker-compose stop db

* agora rode -> docker-compose up -d

* para parar -> docker-compose down

------------------------------------------------------------

* agora rode td docker-compose up -d

*************************

rodar com comando Python DRF

* confgure o .env host tem que ser localhost

* crie o banco de dados nome -> python_login_cadastro_produtos

*  .\venv\Scripts\activate 

* pip install -r requirements.txt

* python manage.py makemigrations   

* python manage.py migrate 

* python manage.py runserver 

