# 📖 Guia Didático do Git Flow

## 📌 Introdução ao Git Flow
O Git Flow é um modelo de ramificação do Git que organiza e otimiza o fluxo de desenvolvimento de software. Ele define diferentes tipos de branches para cada etapa do ciclo de vida do código.

## 🗂️ Estrutura do Git Flow
O Git Flow possui cinco principais tipos de branches:

### 1️⃣ **main (ou master)**
- **Função:** Contém a versão estável e em produção do projeto.
- **Uso:**
  - Apenas recebe merges de `release` e `hotfix`.
  - Nunca desenvolvemos diretamente nessa branch.
- **Exemplo:** `v1.0`, `v2.0`.

### 2️⃣ **develop**
- **Função:** Centraliza o código em desenvolvimento.
- **Uso:**
  - Base para novas funcionalidades (`feature`).
  - Quando um conjunto de funcionalidades está pronto para uma nova versão, cria-se uma `release`.
- **Exemplo:** Código em progresso para a próxima versão.

### 3️⃣ **feature**
- **Função:** Implementa novas funcionalidades ou melhorias.
- **Uso:**
  - Sempre criada a partir de `develop`.
  - Após finalizada, é mesclada de volta em `develop`.
  - Nome padrão: `feature/nome-da-feature`.
- **Exemplo:** `feature/adicionar-login`, `feature/integrar-api`.

### 4️⃣ **release**
- **Função:** Prepara uma nova versão estável do software.
- **Uso:**
  - Criada a partir de `develop` quando as features estão prontas.
  - Aqui acontecem testes finais, correções menores e ajustes de documentação.
  - Ao concluir, é mesclada em `main` (gerando uma nova versão) e em `develop`.
- **Exemplo:** `release/v1.0.0`, `release/v2.1.0`.

### 5️⃣ **hotfix**
- **Função:** Corrige rapidamente bugs críticos em produção.
- **Uso:**
  - Criada a partir de `main` em caso de erro urgente.
  - Após a correção, é mesclada em `main` e `develop`.
- **Exemplo:** `hotfix/corrigir-erro-login`, `hotfix/fix-api-timeout`.

## 📊 Fluxo de Trabalho no Git Flow

1. **Desenvolver novas funcionalidades** → `feature` → merge em `develop`.
2. **Preparar uma nova versão** → `release` → merge em `main` e `develop`.
3. **Corrigir bugs críticos** → `hotfix` → merge em `main` e `develop`.

## 🔗 Comandos Úteis no Git Flow

### ✅ **Instalando Git Flow**
```bash
sudo apt update
sudo apt install git-flow
```
Verifique a instalação:
```bash
git flow version
```

### ✅ **Iniciar Git Flow no repositório**
```bash
cd <meu-projeto>
git flow init
```
Durante a inicialização:
- **Branch de produção:** `main`
- **Branch de desenvolvimento:** `develop`

### 📌 **Criando e Trabalhando com Features**
Criar uma nova feature:
```bash
git flow feature start <nome-da-feature>
```
Trabalhar na feature:
```bash
git add .
git commit -m "Implementa nova funcionalidade"
```
Finalizar a feature:
```bash
git flow feature finish <nome-da-feature>
```

### 📌 **Criando e Trabalhando com Releases**
Criar uma release:
```bash
git flow release start v1.0.0
```
Finalizar a release:
```bash
git flow release finish v1.0.0
```

### 📌 **Criando e Trabalhando com Hotfixes**
Criar um hotfix:
```bash
git flow hotfix start corrigir-bug
```
Finalizar o hotfix:
```bash
git flow hotfix finish corrigir-bug
```

## 🔍 **Resolvendo Conflitos**
Se houver conflitos durante um merge:
```bash
git status
```
Edite os arquivos com conflito, depois:
```bash
git add arquivo_com_conflito.java
git commit -m "Resolvendo conflitos"
```

## 📌 **Resumo do Ciclo Completo**
| Tipo de Branch | Criada a partir de | Mesclada em |
|---------------|----------------|-------------|
| Feature | `develop` | `develop` |
| Release | `develop` | `main` e `develop` |
| Hotfix | `main` | `main` e `develop` |

Se precisar de mais detalhes, me avise! 🚀
