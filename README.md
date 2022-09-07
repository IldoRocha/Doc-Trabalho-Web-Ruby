# Projeto Web Ruby

## VirtualBox
> https://www.virtualbox.org

## Vagrant
> https://www.vagrantup.com

## GIT
> https://git-scm.com

## GitHub
> https://github.com

Visual Studio Code
https://code.visualstudio.com

Ruby
https://www.ruby-lang.org/

Ruby on Rails
https://rubyonrails.org/

Ruby Version Manager (RVM)
https://rvm.io/

PostgreSQL
https://www.postgresql.org/
---
Abrir o Git Bash
Rodar os comandos de teste

vagrant --version
git --version
---
Configurar o seu git

git config --global user.name “Iskailer”
git config --global user.email “iskailer......@...”
---
Criar um projeto no Github
Clonar o projeto para a pasta
c:\Projetos

git clone https://github.com/iskailer/rails-ini.git
cd rails-ini
---
Instalar plugin do vagrant

Vagrant plugin install vagrant-vbguest
---
criar Vagrantfile

vagrant init GuiDev/Ubuntu-Rails5x --box-version 1.0.0
---
Verificar Vagrantfile

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
---
Iniciar Vagrant

vagrant up
---
pausar a box
vagrant suspend

Para parar a box
vagrant halt
---
Conectar na maquina
vagrant ssh
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
