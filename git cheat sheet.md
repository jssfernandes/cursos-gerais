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


## Arquivo


## Mudança


## Stash


## Chery

