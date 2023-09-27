

# CURSO GIT GITHUB - DIO 📚
## Minhas anotações de estudo

A linguagem GIT possui nivéis de preparação quando estamos tratando um arquivo para incluir em um repositório remoto.

| Nivel   | Descrição | observação |
| :---------- | :--------- | :---------- |
| `1`      | `#8B0000` inclusão | Arquivos que acabaram de ser alterados ou incluidos, fazem parte do *untracked* |
| `2` | `#32CD32` Preparação | Uma vez adcionados via **git add** esses arquivos existem no contexto do programa mas ainda não estão "registrados"                    |
| `3` | `#8B008B` Commit | Uma vez que o comando commit é inserido os arquivos estão prontos para serem adcionados ao repositório remoto |



**Ctrl + L =** Limpar o terminal

git config = exibirá todas as configurações, sintaxes presentes dentro do git.
git clone [link] = clonar repositório vindo do GitHub
git clone [link] [nome] = Alterar nome na criação da pasta que será clonada do GitHub
Cat .[arquivo] = lê e exibe o valor/texto dentro do arquivo
mkdir [nome] = Criar pasta
git init = inicia repositório/ prepara pasta para receber propriedades para o git
git remote add origin [url] = conectando minha pasta a uma origem vinda de outro repositório, url do GitHub
git status = retorna o status dos arquivos e de todos dados presente na pasta, até os que não fazem parte de um commit
Ex:
•	Cat .git-credentials
•	Cat .gitconfig

git add [arquivo] = adcionar arquivo no contexto do git/preparando para inclusão
git commit -m"[mensagem]" = envia um commit linkado a uma mensagem ou uma observação
O git não reconhece pastas/ diretórios vazios sem arquivos, para entrar em um commit precisa existir um arquivo
git . = se colocar apenas o ponto ele obtem tudo que não foi incluído na preparação e adciona na base para o commit
git push = envia os commits para o diretório remoto
git log = exibe um histórico de todos commits feitos dentro da pasta
rm -rf .git = situacional caso tenha dado um git init em uma pasta errada, este comando remove a preparação do diretório
git restore [arquivo] = ele restaura o arquivo que foi modificado para a última versão commitada.
Obs. Esse comando descarta todas as alterações feitas entre seu último commit e antes do restore então atenção.
git commit --amend -m"[mensagem]" = altera a mensagem colocada no último commit feito
git reset --soft [id do último commit] = O último commit feito retorna ao status de preparação dos arquivos, ou seja, eles estão no nível de preparação para dar um git add então um git commit.
git reset --mixed [id do último commit] = O último commit feito retorna ao status de recebimento dos arquivos, ou seja, eles estão no nível de untracked(novos) para dar um git add então um git commit.
git reset --hard [id do último commit] = Deleta tudo que foi criado/feito após o commid indicado na seção de indicar o id
git ref log = exibe um histórico das alterações e commits
OBS. Todas as alterações devem ser feitas antes de enviar para o repositório remoto a fim de prever possíveis incompatibilidades e de arquivos corrompidos
git reset [arquivo] = Caso ocorra de após dar um git add . querer remover um arquivo desse nível de preparação o git reset serve para retirá-lo dessa operação e retornar ao nível de status untracked
git push -u origin main = configurar nossa main como a main do nosso repositório remoto
git pull = obtem todas as alterações que foram feitas no repositório remoto e adciona ao repositório local


Receita de bolo para inclusão de um repositório para o github
git remote add origin [link]
git branch -M main = renomeia nossa Branch para main
git push -u origin main
