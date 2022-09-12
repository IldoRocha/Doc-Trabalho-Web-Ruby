# Guia Projeto Web Ruby

## Índice

|Ferramentas|Utilitários|Sub|
|-|-|-|
|[Vagrant](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#vagrant)|[Links](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#links)|[Scaffold](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#scaffold)
|[Git](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#git)|[Via Sacra](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#via-sacra)|[Tasks](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#tasks)
|[GitHub](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#github)|[Dentro da VM](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#dentro-da-vm)|[Embedded Ruby](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#embedded-ruby)
|[Virtual Box](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#virtual-box)|[Comandos](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#comandos)|[Helper](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#helper)
|[Rails](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#rails)||[Rotas](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#rotas)
|[PostgreSQL](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#postgresql)|
|[Ruby Version Manager (RVM)](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#ruby-version-manager-rvm)|
|[VSCode](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#vscode)||

---

## Links

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

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

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

- [x] Criar repositório no GitHub
- [x] Criar pasta para o projeto
- [x] Checar existência e versões dos softwares

---

## Vagrant

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

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

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

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

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

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

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189581023-59280385-0e6a-4daa-b934-81647860a3c9.png)

---

## Rails

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

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

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189582178-e6409d58-2fb1-4af9-99da-134a7adfb473.png)

1. **Verificar a existência e versão de softwares**

    ```
    psql --version
    ```

---

## VSCode

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

![image](https://user-images.githubusercontent.com/85770280/189603243-508b7a6f-8825-4e03-91b8-563a8df683ce.png)

1. Extensões úteis
    - Ruby
    - Rails
    - Gem Lens
    - Ruby Solargraph
    - endwise

---

## Ruby Version Manager (RVM)

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

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

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

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
    RAILS_ENV=production rails s -b 0.0.0.0
    ```
    ```
    rails s -b 0.0.0.0 -e production
    ```
    ```
    rails _5.2_ new <nomedoprograma>
    ```
    ```
    rails _5.2_ new <nomedoprograma> -d postgresql
    ```

---

## Comandos

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

  ### Scaffold
  
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
  
  1. **Outros generators**
```
rails generate
rails generate controller pagina_inicial
rails destroy controller pagina_inicial
rails d controller pagina_inicial
rails g controller welcome index
rails g scaffold State acronym description
rails g migration AddStateToCities state:references
```
  
  ### Tasks
  
  1. **Definição**
        * Tarefas predefinidas que o rails pode executar
        * Generators geram, tasks executam
```
rails -T
```
```
rails -T db
```
```
rails db:create
```
```
rails db:drop
```
```
rails db:migrate
```
```
rails db:rolllback
```
```
rails db:seed
```
```
rails g task dev db_setup
```

```
desc "Configura o banco de dados do zero"
    task db_task: :environment do
    if Rails.env.development?
        puts %x(rails db:drop)
        puts %x(rails db:create)
        puts %x(rails db:migrate)
        puts %x(rails db:seed)
    else
        puts "ambiente de producao!"
    end
end
```

1. **NPM para instalar o YARN**
    ```
    sudo apt install npm
    ```

---

## Embedded Ruby

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

1. **Forma de mesclar código ruby com texto**
    - <% o que estiver aqui não exibe %>
    - <%= o que estiver aqui exibe %>

---

## Helper

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

1. **Helper link_to**

    ```
    <%= link_to 'Exibir', '/cities'%>
    <%= link_to 'Exibir', city %>
    ```

1. **Helper imagem**
    ```
    <td><img src="<%=city.image%>" width="25px" height="25px"></td>
    <td><%=image_tag city.image, width: 25, height: 25%></td>
    <td><%=image_tag city.image, size: "25x25"%></td>
    ```
    
1. **Helper data**
    ```
    <%= Date.today %>
    <%= Date.today.strftime("%d/%m/%Y") %>
    <%= br_date(Date.today) %>
    —------------- helper
    module ApplicationHelper
    def br_date(us_date)
    us_data.strftime("%d;%m;%Y")
    end
    end
    ```
    
1. **cities_helper.rb***
    ```
    def formata_cep(n_cep)
        cep = n_cep.to_s
        cep_formatado = cep[0..1]
        cep_formatado << "."
        cep_formatado << cep[2..4]
        cep_formatado << "-"
        cep_formatado << cep[5..7]
        cep_formatado
    end
    ```
    
---

## Rotas

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)

1. **Mapeamento padrão usando a instrução root to**
    - Root to: “welcome#index”

1. **routes.rb**
    ```
    Rails.application.routes.draw do
        get "welcome/index"
        resources :cities
        get "/cities", to: "cities#index"
        root to: "welcome#index"
    end
    ```
    
1. **Para criar sua própria rota declare o verbo a url e o controler#action que deve responder a roda digitada**
    - get “inicio”, to: “welcome#index”

1. **Seeds**
    ```
    State.create(id: 24, description: 'Santa Catarina',
    acronym: 'SC')
    State.create(id: 25, description: 'Sergipe', acronym: 'SE')
    State.create(id: 26, description: 'São Paulo', acronym:
    'SP')
    State.find_or_create_by!(id: 27, description: 'Tocantins',
    acronym: 'TO')
    ```
    
---

[Voltar ao índice](https://github.com/IldoRocha/Trabalho-Web-Ruby/blob/main/README.md#%C3%ADndice)
