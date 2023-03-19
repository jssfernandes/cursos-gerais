# Git Cheat Sheet

## Git
Verificar a versão do git instalada
```bash
git --version
```
Configurar o nome
```bash
git config --global user.name "NOME"
```
Configurar o e-mail
```bash
git config --global user.email "EMAIL"
```
Enviar arquivo ao repositorio remoto
```bash
git remote add origin git@github.com:"USUARIO_GITHUB"/"REPOSITORIO"
```
Verificar os arquivos enviados
```bash
git remote -v
```
Sincronizar o repositorio local com o remoto
```bash
git remote add origin https://github.com/[USUARIO]/[REPOSITORIO].git
```

### Iniciando um Repositorio
Inicia um repositorio local
```bash
git initi
```
Cria uma cópia do repositorio local
```bash
git clone ssh://git@github.com/[USUARIO]/[REPOSITORIO].git
```

## Log
Exibir historico dos ultimos commits
```bash
git log
```
Exibir historico com diff dos ultimos 3 commits
```bash
git log -p -3 
```
Exibir historico no CAMINHO_DO_ARQUIVO
```bash
git log --<CAMINHO_DO_ARQUIVO>
```
Exibir historico de commits com informações resumidas em uma linha. (Existem outros tipos)
```bash
git log --pretty=oneline
```
Exibir historico de modificacoes de um arquivo
```bash
git log --diff-filter=M --<CAMINHO_DO_ARQUIVO>
```
Exibir historico de um determinado autor
```bash
git log --author=<USUARIO>
```

## Branch
Cria um branch com o nome nova-branch
```bash
git branch nova-branch
```
Cria uma branch nova com o nome nova-branch e muda o codigo e a referencia para essa no nova-branch
```bash
git checkout -b nova-branch
```
Muda o codigo atual e a referencia para a branch nova-branch
```bash
git checkout nova-branch
```
Muda o codigo para a branch principal: main
```bash
git checkout main
```
Deleta a nova-branch
```bash
git branch -d nova-branch
```
Lista as branchs criadas
```bash
git branch
```
Lista as branchs criadas com os logs de commit
```bash
git branch -v
```
Cria uma branch remota  com o nome nova-branch
```bash
git push origin nova-branch
```
Cria uma branch remota com o nome diferente da branch local
```bash
git push origin nova-branch:branch-nome-diferente
```
Download de todos os arquivos do repositorio remota para o repositorio local
```bash
git pull origin main
```
Download de todos as branchs remotas
```bash
git fetch origin
```
Download de uma branch remota para edicao
```bash
git checkout -b nova-branch origin/nova-branch
```
Realiza o merge entre as branchs, ou seja, junta o ramo na arvore principal
```bash
git merge nova-branch 
```


## Arquivo


## Mudança


## Stash


## Chery

