# Guia Projeto Web Ruby

## Índice

|Ferramentas|Utilitários|Comandos|
|-|-|-|
|[Vagrant](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#vagrant)|[Links úteis](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#links-%C3%BAteis)|[Scaffold](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#scaffold)
|[Git](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#git)|[Via Sacra](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#via-sacra)
|[GitHub](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#github)|[Dentro da VM](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#dentro-da-vm)
|[Virtual Box](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#virtual-box)|[Comandos](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#comandos)
|[Rails](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#rails)|
|[PostgreSQL](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#postgresql)|
|[Ruby Version Manager (RVM)](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#ruby-version-manager-rvm)|

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

- [x] Criar repositório no GitHub
- [x] Criar pasta para o projeto
- [x] Checar existência e versões dos softwares

---

## Vagrant

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189581078-6b90d0bb-de54-4bbc-8501-c0183ed2e78d.png)

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
    Vagrant plugin install vagrant-vbguest
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

![image](https://user-images.githubusercontent.com/85770280/189580965-a4212a91-090f-48b1-8361-4207fdcbc341.png)

1. Configurar usuário

    ```
    git config --global user.name "Antedeguemon"
    ```
    ```
    git config --global user.email "email@.com"
    ```

---

## GitHub

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189575894-05c0eedb-7496-468d-928f-ce1e5055eebe.png)


- Utilizar GitHub para versionamento de código
- Criar um projeto no Github
- Clonar o projeto para a pasta c:\Projetos

```
git clone https://github.com/iskailer/rails-ini.git
```    
```
cd rails-ini
```

---

## Virtual Box

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189581023-59280385-0e6a-4daa-b934-81647860a3c9.png)

---

## Rails

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189581422-a93255b6-eb39-455d-8918-d3637459221e.png)

1. **Princípios do rails**
      * DRY Don’t Repeat Yourself
      * CoC Convention Over Configuration

1. **Verificar a existência e versão de softwares**

    ```
    Rails -v
    ```
1. **Gems**
    ```
    gem install rails
    ```
    ```
    gem install rails -v 5.2.8
    ```
    ```
    gem install rails –version=5.2.8
    ```
    
---

## PostgreSQL

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189582178-e6409d58-2fb1-4af9-99da-134a7adfb473.png)

1. **Verificar a existência e versão de softwares**

    ```
    psql --version
    ```

---

## Ruby Version Manager (RVM)

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189582378-05f033ee-c162-4a8f-be89-64db0a7dab04.png)

```
rvm list
```
```
rvm list known
```
```
rvm install 2.3
```
```
rvm use 2.6
```

---

## Dentro da VM

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

![gif](https://thumbs.gfycat.com/ShadyYearlyBovine-max-1mb.gif)

1. **Acessar pasta compartilhada**

1. **Usar o Ruby puro**
    ```
    ruby nome_arquivo.rb
    ```

1. **Usar o IRB - Interactive Ruby**

    ```
    Shell
    irb
    puts “teste direto”
    “Feijao e bao demais”.reverse
    exit
    ```

1. **Usar o Pry (Gem)**

    ```
    gem install pry
    ```
    ```
    pry
    puts “teste direto”
    “Feijao e bao demais”.reverse
    exit
    ```

1. **Rails**

    ```
    rails new projetinho
    ```
    ```
    rails server -> rails s -b 0.0.0.0
    ```
    ```
    rails _5.2_ new <nomedoprograma>
    ```
    ```
    rails _5.2_ new <nomedoprograma> -d postgresql
    ```

---

## Comandos

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/edit/main/README.md#%C3%ADndice)

  #### SCAFFOLD  
  
  1. **Convenções**
        * Sempre em inglês
        * Model sempre com a primeira maiúscula e no singular
        * Tipo string não precisa de definição

  1. **Itens criados pelo SCAFFOLD**
        * Views
        * Helpers
        * Controllers
        * Models
        * Migrations

  ```
  rails generate scaffold <Model> <campo:tipo> <campo:tipo> ...  
  ```
  ```
  rails g scaffold City description:string code:integer image
  ```
  
  ---

