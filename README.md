

# CURSO GIT GITHUB - DIO 📚
### Minhas anotações de estudo


## 🧱 Entendendo tratativa do arquivo

A linguagem GIT possui nivéis de preparação quando estamos tratando um arquivo para incluir em um repositório remoto.

| Nivel   | Descrição | observação |
| :---------- | :--------- | :---------- |
| `1`      | ***inclusão***/***Untracked*** | Arquivos que acabaram de ser alterados ou incluidos, fazem parte do ***untracked***. |
| `2` | ***Preparação***/***contexto*** | Adcionados via `git add` esses arquivos existem no contexto do programa mas ainda não estão integrados.                    |
| `3` | ***Commit***/***Integrados*** | Utilizando o comando `commit` os arquivos estão prontos para serem adcionados a integração local e aguardando serem inseridos ao repositório remoto via `push`. |


## 📌 Receita de bolo para inclusão de um repositório local para o GitHub

⚙ `git init` = inicia o repositório / prepara a pasta para receber as propriedades para o git

```
git remote add origin [link] = conecta seu repositorio local a um remoto

git branch -M main = renomeia nossa Branch para main

git push -u origin main 
```
### Outros comandos:

⚙ `git clone [link]` = Clonar repositório vindo do GitHub.

⚙ `git clone [link] [nome]` = Alterar nome na criação da pasta que será clonada do GitHub.

⚙ `git push` = Envia os commits feitos localmente para o diretório remoto.

⚙ `git pull` = Obtem todas as alterações que foram feitas no repositório remoto e adciona ao repositório local.

## 🔍 Comandos importantes

⚙ `git config` = Exibirá todas as configurações, sintaxes presentes dentro do git.


⚙ `git status` = Retorna o status dos arquivos e de todos dados presente na pasta, até os que não fazem parte de um commit.


⚙ `git add [arquivo]` = Adcionar arquivos do **nivel 1** para o **nivel 2**.

⚙ `git .` = Se colocar apenas o ponto ele obtem tudo incluído no **nivel 1** e adciona ao **nivel 2**.

⚙ `git commit -m"[mensagem]"` = Envia um commit linkado a uma mensagem ou uma observação.

❗ ***Obs.*** O GIT não reconhece arquivos/diretórios vazios sem arquivos, para entrar em um commit precisa existir um dado.


⚙ `git log` = Exibe um histórico de todos commits feitos dentro da pasta.

⚙ `git restore [arquivo]` = Ele restaura o arquivo que foi modificado para a última versão commitada.

❗ ***Obs.*** Esse comando descarta todas as alterações feitas entre seu último commit e antes do restore então atenção.

⚙ `git commit --amend -m"[mensagem]"` = Altera a mensagem colocada no último commit feito.

## 🔄 Tipos de resets dentro do GIT

⚙ `git reset --soft [id do último commit]` = O último commit feito retorna ao status de preparação dos arquivos, ou seja, eles estão no nível de preparação para dar um git add então um git commit.

❗***SOFT:*** `Nivel 3 para o Nivel 2`

⚙ `git reset --mixed [id do último commit]` = O último commit feito retorna ao status de recebimento dos arquivos, ou seja, eles estão no nível de untracked(novos) para dar um git add então um git. commit.

❗❗***MIXED:*** `Nivel 2 para o Nivel 1`

⚙ `git reset --hard [id do último commit]` = Deleta tudo que foi criado/feito após o commid indicado na seção de indicar o id.

❗❗❗***HARD:*** `Nivel 1 apagado`

⚙ `git ref log` = Exibe um histórico das alterações e commits.

❗ ***Obs.*** Todas as alterações devem ser feitas antes de enviar para o repositório remoto a fim de prever possíveis incompatibilidades e de arquivos corrompidos.

⚙ `git reset [arquivo]` = ***Situacional*** - Caso ocorra de após dar um `git add .` querer remover um arquivo desse nível de preparação o comando serve para retirá-lo dessa operação e retornar ao **nível 1**.

⚙ `rm -rf .git` = ***Situacional*** - Caso tenha dado um `git init` em uma pasta errada, este comando remove a preparação do diretório.

## 💾 Dicas valiosas

! `mkdir [nome]` = Criar uma pasta no repositório.

! `Ctrl + L` = Limpa tela do GIT.

! `cat .[arquivo]` = lê e exibe o valor/texto dentro do arquivo.

***Ex:***

•	*Cat .git-credentials*

•	*Cat .gitconfig*