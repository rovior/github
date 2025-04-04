Aqui está o passo a passo formatado em **Markdown (`.md`)** para conectar **Git** ao **GitHub**:  

---

### 📌 Conectando Git ao GitHub  

```md
# 🚀 Conectando Git ao GitHub

## 🔹 Passo 1: Verificar se o Git está instalado
Abra o terminal e digite:
```bash
git --version
```
Se o Git estiver instalado, ele mostrará a versão. Caso contrário, instale com:

- **Ubuntu/Debian**:
  ```bash
  sudo apt update && sudo apt install git -y
  ```
- **Windows**: Baixe e instale o [Git para Windows](https://git-scm.com/downloads).

---

## 🔹 Passo 2: Configurar o usuário no Git
Defina seu nome e e-mail:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
Verifique se foi configurado corretamente:
```bash
git config --list
```

---

## 🔹 Passo 3: Criar um repositório no GitHub
1. Acesse [GitHub](https://github.com/) e faça login.
2. Clique em **New repository**.
3. Dê um nome ao repositório e clique em **Create repository**.

---

## 🔹 Passo 4: Conectar um repositório local ao GitHub

### 📌 Se já tem um projeto local:
```bash
cd /caminho/do/projeto
git init
git add .
git commit -m "Primeiro commit"
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPO.git
git push -u origin main
```

### 📌 Se deseja clonar um repositório existente:
```bash
git clone https://github.com/SEU-USUARIO/NOME-DO-REPO.git
```

---

## 🔹 Passo 5: Autenticação no GitHub
O GitHub exige **token** em vez de senha. Para gerar:
1. Vá para [Configurações > Developer Settings > Personal Access Tokens](https://github.com/settings/tokens).
2. Clique em **Generate new token**, selecione as permissões e copie o token.
3. No primeiro `git push`, use o token como senha.

---

## 🔹 Passo 6: Comandos básicos do Git
- Verificar status do repositório:
  ```bash
  git status
  ```
- Adicionar arquivos para commit:
  ```bash
  git add .
  ```
- Criar um commit:
  ```bash
  git commit -m "Mensagem do commit"
  ```
- Enviar alterações para o GitHub:
  ```bash
  git push origin main
  ```
- Atualizar a cópia local com alterações do GitHub:
  ```bash
  git pull origin main
  ```

---

Agora seu Git está conectado ao GitHub! 🚀
```

---

Quer que eu crie um arquivo `.md` para você com esse conteúdo? 😊
