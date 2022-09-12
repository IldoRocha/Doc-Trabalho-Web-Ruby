# Guia Projeto Web Ruby

## Índice

|Utilitários|Ferramentas
|-|-|
|[Links úteis](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#links-%C3%BAteis)|[Vagrant](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#vagrant)|
|[Via Sacra](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#via-sacra)|[Git](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#git)
||[GitHub](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#github)

---

## Links úteis

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189574241-4769cceb-44a6-404a-b9cb-ae4111643dbc.png)

|Assunto|Link|
|-|-|
|**VirtualBox**|https://www.virtualbox.org|
|**Vagrant**|https://www.vagrantup.com|
|**GIT**|https://git-scm.com|
|**GitHub**|https://github.com|
|**Visual Studio Code**|https://code.visualstudio.com|
|**Ruby**|https://www.ruby-lang.org/|
|**Ruby on Rails**|https://rubyonrails.org/|
|**Ruby Version Manager (RVM)**|https://rvm.io/|
|**PostgreSQL**|https://www.postgresql.org/|

---

## Via Sacra

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

1. **Configurar ambiente**
    - [x] Baixa Git
    - [x] Baixa Git
1. **Vagrant**
    - [x] a
1. **b**
    - [x] a
    - [x] a
    - [x] a
    - [x] a

---

## Vagrant

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189573887-c8726a53-ae5c-47d3-9da3-b39bf37d2154.png)

> Utilizar o *Git Bash*

1. **Verificar a existência e versão de softwares**
    ```
    vagrant --version
    ```
    ```
    git --version
    ```
1. **Instalar plugin do vagrant**
    ```
    install vagrant-vbguest
    ```
1. **criar Vagrantfile**
    ```
    vagrant init GuiDev/Ubuntu-Rails5x --box-version 1.0.0
    ```
1. **Substituir conteúdo da Vagrantfile com as seguintes configurações**
    ```
    Vagrant.configure("2") do |config|
    config.vm.box = "GuiDev/Ubuntu-Rails5x"
    config.vm.box_version = "1.0.0"
    config.vm.network :forwarded_port, guest: 3000, host: 3000
    config.vm.network :forwarded_port, guest: 5432, host: 5432
    config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "1024"
    end
    end
    ```
1. **Iniciar Vagrant**
    ```
    vagrant up
    ```
1. **Pausar a box**
    ```
    vagrant suspend
    ```
1. **Para parar a box**
    ```
    vagrant halt
    ```
1. **Conectar na maquina**
    ```
    vagrant ssh
    ```
---

## Git

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189572566-b46fea5e-f0af-4a95-9ef0-e2a4553f15b8.png)

1. Configurar usuário
    1. - git config --global user.name "x"
    1. - git config --global user.email "x@y"

---

## GitHub

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189575894-05c0eedb-7496-468d-928f-ce1e5055eebe.png)

Utilizar GitHub para versionamento de código
Criar um projeto no Github
Clonar o projeto para a pasta
c:\Projetos

git clone https://github.com/iskailer/rails-ini.git
cd rails-ini

---

Verificar Ruby & Rails & PG
Ruby -v
Rails -v
psql --version

---

gem install rails
gem install rails -v 5.2.8
gem install rails –version=5.2.8

---

Acessar pasta compartilhada
cd ..
ls
cd vagrant

---

Acessar pasta compartilhada
24
cd ..
ls
cd vagrant

---

Usar o RVM
rvm list
rvm list known
rvm install 2.3
rvm use 2.6

---

Usar o Ruby puro
ruby nome_arquivo.rb

---

Usar o IRB - Interactive Ruby
Shell
irb
puts “teste direto”
“Feijao e bao demais”.reverse
exit

---

Pry (Gem)
gem install pry
pry
puts “teste direto”
“Feijao e bao demais”.reverse
exit

---

Rails
rails new projetinho

---

rails new projetinho

---

Rails
rails new projetinho
cd projetinho
rails server -> rails s -b 0.0.0.0

---

Princípios do rails
DRY
(Don’t
Repeat
Yourself)
CoC (Convention
Over
Configuration)

---

Ruby On Rails
PRIMEIRO APP/CRUD

---

MVC
Model - View - Controller

---

rails
rails new projetinho
rails _5.2_ new <nomedoprograma>
rails _5.2_ new <nomedoprograma> -d postgresql

---

CREATE, READ, UPDATE, DELETE
Operações básicas de manipulação
de banco de dados!

---

  SCAFFOLD
O rails possui um gerador/generator
chamado scaffold que cria
automagicamente um CRUD para
uma determinada “tabela”.

  ---
  
  rails generate scaffold <Model> <campo:tipo> <campo:tipo> ...
  
  ---
  
  CONVENÇÕES
  SEMPRE EM INGLÊS
  MODEL SEMPRE COM A PRIMEIRA
  MAIÚSCULA E NO SINGULAR
  TIPO STRING NÃO PRECISO DEFINIÇÃO
  
  ---
  
  rails generate scaffold <Model> <campo:tipo> <campo:tipo> ...
  rails g scaffold City description:string code:integer image
  
  ---
  
  O que ele já criou
  Views
  Helpers
  Controllers
  Models
  Migrations
  
  ---
  
  active record - Model
  Camada responsável pela lógica de dados
e negócio, ORM.
  Framework de banco de dados baseado
no padrão Active Record

  ---
  
  ORM?
  Uma técnica para mapear os dados
em um banco de dados para
classes/objetos na programação

  ---
  
  Migrations
۞ São uma funcionalidade do AR que
permite especificar as tabelas do bd
usando o Ruby;
۞ Permite ações no BD sem utilizar SQL;
۞ Disponibiliza a sequência de criação das
tabelas do projeto;
  Migrations controlam o que foi ou não
aplicado através do db/schema.rb;
۞ As migrations ficam em db/migrate;
۞ Ao criar as migrações é preciso aplicá-las
ao BD usando tasks predefinidas do Rails.
  
 Rails dbconsole
۞ rails dbconsole é o comando usado para
conectar ao banco de dados e executar
comandos para inspecioná-lo.
۞ Uma alternativa para os gerenciadores
próprios como o pgadmin
  rails dbconsole
  rails db
