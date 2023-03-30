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
### Adicionar
Adiciona todos os arquivos ou diretórios modificados
```bash
git add .
```
Adiciona somente o arquivo meu_programa.py;
```bash
git add meu_programa.py
```
Adiciona somente o diretorio meu_diretorio;
```bash
git add meu_diretorio
```
Adiciona um arquivo que está no .gitignore;
```bash
git add -f meu_programa_gitignore.py
```

### Remover
Remover arquivo
```bash
git rm meu_arquivo.txt
```
Remover diretório
```bash
git rm -r diretorio
```

### Commitar
Comitar um arquivo
```bash
git commit meu_programa.py
```
Comitar vários arquivos
```bash
git commit file1.txt file2.txt
```
Comitar informando mensagem
```bash
git commit meuarquivo.txt -m "minha mensagem de commit"
```


## Mudança
Mostrar as modificações totais do projeto
```bash
gitk 
```
Modificações antes de enviar as modificações para o repositório remoto (commit)
```bash
git diff
```
Estado dos arquivos/diretório
```bash
git status
```
Alterar mensagens de commit já realizado
```bash
git commit --amend -m "Minha nova mensagem"
```
Alterar últimos commits, modificando as mensagens
```bash
git rebase -i HEAD-3
```


## Stash
Criar um stash, salvar temporariamente as modificações
```bash
git stash
```
Listar os stashes criados
```bash
git stash list
```
Voltar ao último stash
```bash
git stash apply
```
Voltar ao stash com índice 2
```bash
git stash apply stash@{2}
```
Criar um branch a partir de um stash
```bash
git stash branch minha_branch
```


## Chery-Pic
Copia as informações desse commit 
```bash
git cherry-pick <commit-id>
```
Copia todos os commits entre o commit A e o commit B, inclusive A e B.
```bash
git cherry-pick A^..B
```
Copia todos os commits entre o commit A e o commit B, excluindo A.
```bash
git cherry-pick A..B
```

