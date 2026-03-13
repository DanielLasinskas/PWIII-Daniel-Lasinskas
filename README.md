# PWIII-Daniel-Lasinskas
Aula de programação web com Prof. João Siles

## 🚀 Criando um Projeto com Laravel

## 📋 O que você precisa?

* PHP 🐘
* Composer 🎼
* Laravel Installer ⚙️
* Node.js e NPM 🟢
* Git Bash 💻
* XAMPP 🔥
* Visual Studio Code 🧑‍💻

---

## 📂 Usando o Git Bash

1️⃣ Abra a pasta do **XAMPP** 📁
2️⃣ Abra a pasta **htdocs** 📂
3️⃣ Abra o **Git Bash** 💻

### 🔐 Configure seu Git

Faça login com seu nome:

```
git config --global user.name "Seu-nome"
```

Faça login com seu e-mail:

```
git config --global user.email Seu-email
```

### 📥 Clone seu repositório

```
git clone (Sua-url-do-git)
```

Abra sua pasta com:

```
cd sua-pasta
```

---

## ⚙️ Como instalar os componentes

Abra o **Windows PowerShell como administrador** 🛠️

Digite o seguinte comando:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://php.new/install/windows/8.4'))
```

---

## 🎯 Instalando o Laravel Installer

Digite o comando:

```
composer global require laravel/installer
```

---

## 🏗️ Criando a aplicação

Feche o **Windows PowerShell** ❌

Abra o terminal no seu projeto 💻

Use estes comandos:

```
cd --
cd --
cd C:
cd xampp
cd htdocs
cd seu-repositorio
```

Crie o projeto com:

```
laravel new example-app
```

---

## 🔧 Configuração do Projeto

Feche o terminal ❌

Abra o **Windows PowerShell** novamente 🛠️

Instale todas as dependências (cria a pasta vendor):

```
composer install
```

Instale as dependências JavaScript:

```
npm install
```

Gere os arquivos executáveis do NPM:

```
npm run build
```

---

## 📝 Configurando o ambiente

1️⃣ Abra o **Visual Studio Code** 🧑‍💻
2️⃣ Copie o arquivo `.env.example`
3️⃣ Renomeie para `.env`

Volte ao **Windows PowerShell** 🛠️

Digite:

```
php artisan
```

Gere a chave da aplicação:

```
php artisan key:generate
```

Execute as migrações do banco de dados:

```
php artisan migrate
```

Digite **Yes** quando solicitado ✅

---

## 💾 Salvando o projeto no Git

Feche tudo 🔒

Abra o **Git Bash** 💻

Digite:

```
cd seu-repositorio
git add .
git commit -m "Sua mensagem"
git push
```


