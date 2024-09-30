Aqui estão duas partes importantes: uma lista dos **comandos Git mais usados** e um **passo a passo completo para realizar um commit** em um repositório Git.

### **Comandos Mais Usados em Git**

| **Comando** | **Descrição** |
|-------------|---------------|
| `git init` | Inicializa um novo repositório Git local no diretório atual. |
| `git clone <URL>` | Faz o clone (cópia) de um repositório remoto para o seu computador. |
| `git status` | Mostra o status atual do repositório, listando arquivos modificados e prontos para commit. |
| `git add <arquivo>` | Adiciona um arquivo específico à "staging area" (área de preparação) para o próximo commit. |
| `git add .` | Adiciona **todos os arquivos modificados** à staging area. |
| `git commit -m "mensagem"` | Cria um commit com uma mensagem que descreve as mudanças feitas. |
| `git commit -am "mensagem"` | Adiciona e faz o commit de todos os arquivos modificados (que já estão sendo rastreados) em uma única etapa. |
| `git log` | Exibe o histórico de commits do repositório. |
| `git branch` | Lista as branches (ramificações) existentes. |
| `git checkout <nome-da-branch>` | Alterna entre branches existentes. |
| `git checkout -b <nome-da-branch>` | Cria uma nova branch e alterna para ela imediatamente. |
| `git merge <nome-da-branch>` | Faz a fusão das mudanças de outra branch com a branch atual. |
| `git pull` | Atualiza o repositório local com as mudanças do repositório remoto (equivalente a `git fetch` + `git merge`). |
| `git push` | Envia os commits locais para o repositório remoto. |
| `git reset --soft HEAD^` | Desfaz o último commit, mas mantém as alterações no staging area. |
| `git reset --hard HEAD^` | Desfaz o último commit e também as mudanças feitas no código. |
| `git stash` | Armazena temporariamente as mudanças não commitadas, deixando a área de trabalho limpa. |
| `git stash apply` | Aplica as mudanças armazenadas pelo `git stash`. |

---

### **Passo a Passo para Fazer Commit em um Repositório Git**

Aqui está um processo completo que inclui desde a clonagem de um repositório até o envio de commits para o GitHub.

#### **1. Clonar um Repositório Remoto (se já existir)**

Caso você já tenha um repositório no GitHub ou outro serviço, primeiro faça o clone dele:

```bash
git clone <URL-do-repositório>
```

#### **2. Inicializar um Novo Repositório (se for um novo projeto)**

Se você está começando um novo projeto do zero, primeiro inicialize o Git no diretório:

```bash
git init
```

#### **3. Verificar o Status Atual do Repositório**

Antes de fazer um commit, verifique o status dos arquivos modificados:

```bash
git status
```

#### **4. Adicionar Arquivos à Staging Area**

Para preparar os arquivos que você quer incluir no commit, use o comando `git add`. Pode adicionar um arquivo específico ou todos de uma vez:

- Adicionar um arquivo específico:

  ```bash
  git add <nome-do-arquivo>
  ```

- Adicionar todos os arquivos modificados:

  ```bash
  git add .
  ```

#### **5. Fazer o Commit das Mudanças**

Após adicionar os arquivos à staging area, crie um commit com uma mensagem descritiva:

```bash
git commit -m "Mensagem explicando o que foi modificado"
```

#### **6. Verificar o Histórico de Commits (Opcional)**

Se quiser visualizar o histórico de commits feitos no repositório, pode usar:

```bash
git log
```

#### **7. Conectar o Repositório Local a um Repositório Remoto (se necessário)**

Se você criou o repositório localmente e ainda não está conectado a um repositório remoto (por exemplo, GitHub), adicione o repositório remoto:

```bash
git remote add origin <URL-do-repositório-remoto>
```

#### **8. Enviar as Mudanças para o Repositório Remoto**

Agora, envie suas mudanças para o repositório remoto (no GitHub, por exemplo):

```bash
git push origin <nome-da-branch>
```

Se você estiver na branch principal (normalmente chamada `main` ou `master`), o comando seria:

```bash
git push origin main
```

Se for a primeira vez enviando essa branch para o remoto, pode ser necessário usar:

```bash
git push -u origin main
```

Isso define a branch padrão para futuros `git push`.

---

### **Resumo do Processo**

1. Clone ou inicialize o repositório:
   ```bash
   git clone <URL>  # ou git init para novo repositório
   ```
2. Verifique o status:
   ```bash
   git status
   ```
3. Adicione os arquivos modificados:
   ```bash
   git add .  # ou git add <arquivo>
   ```
4. Crie o commit com uma mensagem descritiva:
   ```bash
   git commit -m "Descrição do commit"
   ```
5. Se necessário, conecte ao repositório remoto:
   ```bash
   git remote add origin <URL-do-repositório>
   ```
6. Envie as mudanças para o repositório remoto:
   ```bash
   git push origin main  # ou outra branch
   ```

Esses passos cobrem o processo básico de trabalhar com o Git e realizar commits.