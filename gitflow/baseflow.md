# 📌 O que é Git Flow?
```bash
Git Flow é um modelo de fluxo de trabalho criado por **Vincent Driessen** que estrutura
o ciclo de vida do desenvolvimento em diferentes ramificações com propósitos específicos.
Esse modelo torna o gerenciamento de código mais organizado e facilita a colaboração
entre desenvolvedores.
```
## 🎯 Objetivo Principal
```bash
✅ Facilitar a colaboração em equipe, garantindo um fluxo bem definido de desenvolvimento.
✅ Organizar as entregas (“deploys”) de versões para produção.
✅ Gerenciar múltiplas versões de um sistema de forma eficiente.
✅ Evitar conflitos de merge desnecessários e manter a estabilidade da branch principal.
```
## 🚀 Como Começar com Git Flow

### 📌 Passo 1: Instalar o Git Flow
```bash
No Ubuntu (ou sistemas baseados em Debian), instale o Git Flow com:


sudo apt update
sudo apt install git-flow


Verifique se a instalação foi bem-sucedida:


git flow version


Para Windows, se você já tem o Git instalado, pode usar o Git Flow pelo terminal do
**Git Bash** ou configurar manualmente as branches.
```
### 📌 Passo 2: Iniciar o Git Flow no Repositório
```bash
Acesse o diretório do seu projeto:


cd <meu-projeto>


Inicie o Git Flow no repositório:


git flow init


O comando acima irá guiá-lo para definir os nomes padrões das branches
(geralmente `main`, `develop`, `feature`, `release`, `hotfix` e `support`).
```
---

## 📖 Introdução ao Aprendizado do Git Flow
```bash
O Git Flow é um dos modelos de branching mais utilizados em equipes de
desenvolvimento, principalmente para projetos que possuem um ciclo de entrega bem
definido. Ele se baseia no Git tradicional, adicionando convenções sobre quando e
como criar novas branches.
```
### 🛠️ Principais Conceitos do Git Flow:
```bash
- **`main`**: Contém a versão de produção do software.
- **`develop`**: Branch principal para desenvolvimento, onde novas funcionalidadessão integradas antes do release.
- **`feature/*`**: Criada para desenvolver novas funcionalidades e depois ser mesclada na `develop`.
- **`release/*`**: Usada para preparar uma nova versão antes de ser integrada na `main`.
- **`hotfix/*`**: Criada para corrigir bugs urgentes na `main` sem afetar o fluxo de desenvolvimento.

Ao adotar esse modelo, sua equipe ganha mais controle sobre o ciclo de vida do código,
 garantindo entregas mais organizadas e seguras.
```
---

📌 **Próximos Passos:**
```bash
No próximo documento, vamos detalhar a estrutura do Git Flow, explicando o uso das branches
e exemplos práticos do fluxo de trabalho. 😉
```
