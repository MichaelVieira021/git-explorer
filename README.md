<div>
  <img src="./img/git-explorer.png" alt="Git Explorer Image">
</div>

Bem-vindo ao Git-explorer! Este repositório abrange não apenas os comandos essenciais do Git, mas também boas práticas, conceitos do SemVer e estratégias do GitFlow.

## Comandos Git
<details>
    <summary>Configuração Inicial</summary>
<div>

| Comando | Descrição   |
| ------- | ----------- |
| `git config --global user.name "nome-exemplo"` | Adicionar nome de usuário do GitHub |
| `git config --global user.email usuario@exemplo.com` | Adicionar e-mail do GitHub |
| `git config --global --unset user.email` | Remover e-mail do GitHub |
| `git config --global --unset user.name` | Remover nome de usuário do GitHub |
| `git config --global --list` | Exibir a lista de configurações atuais |
| `git config --list` | Exibir a lista de configurações atuais |
| `ssh-keygen -t ed25519 -C e-mail` | Gerar chave SSH |
| `eval $(ssh-agent -s)` | Verificar agente SSH |
| `ssh-add [caminho]` | Adicionar chave SSH ao seu ambiente de trabalho |

</div>
</details>

<details>
    <summary>Comandos Básicos</summary>
<div>

| Comando | Descrição |
| ------- | ----------|
| `git status` | Exibir status| 
| `git add [arquivo]` | Adicionar arquivos à área de preparação (staging) |
| `git add .` | Adicionar todos os arquivos novos à área de preparação (staging) |
| `git commit -m "mensagem"` | Confirmar as alterações com uma mensagem descritiva |
| `git tag -a [nome] -m "mensagem"` | Criar tag |
| `git tag` | Listar todas as tags |
| `git push origin [nome do branch]` | Enviar um branch para o seu repositório remoto |
| `git pull` | Atualizar o repositório local para o commit mais recente |
| `git pull origin [nome do branch]` | Puxar alterações do repositório remoto |
| `git blame NOME_ARQUIVO` | Mostra quem fez cada alteração em cada linha de um arquivo, fornecendo informações sobre a autoria das mudanças |


</div>
</details>

<details>
  <summary>Criar e Clonar Repositórios</summary>
<div>

| Comando | Descrição |
| ------- | ----------|
| `git init` | Iniciar o git dentro da pasta |
| `git clone [url]` | Clonar um repositório do GitHub |
| `git remote add origin ssh://git@github.com/[nome-de-usuario]/[nome-do-repositorio].git` | Adicionar um repositório remoto |
| `git remote -v` | Listar conexões remotas |
| `git remote set-url [nome do branch] [url]` | Alterar a URL |

</div>
</details>

<details>
  <summary>Trabalhando com Ramificações</summary>
<div>
 
| Comando | Descrição |
| ------- | ----------- |
| `git branch` | Listar todas as branches (o asterisco denota o branch atual) |
| `git branch -a` | Listar todas as branches (locais e remotas) |
| `git branch [nome do branch]` | Criar um novo branch |
| `git branch -d [nome do branch]` | Deletar um branch local |
| `git push origin --delete [nome do branch]` | Deletar um branch remoto |
| `git show-branch --all` | Listar todos os branches locais |
| `git push origin --delete [nome do branch]` | Deletar um branch remoto |
| `git checkout -b [nome do branch]` | Criar um novo branch e alternar para ele |
| `git checkout -b [nome do branch] origin/[nome do branch]` | Clonar um branch remoto e alternar para ele |
| `git checkout [nome do branch]` | Alternar para um branch |
| `git checkout -` | Alternar para o último branch acessado |
| `git checkout -- [nome-arquivo.txt]` | Descartar alterações em um arquivo |
| `git merge [nome do branch]` | Mesclar um branch no branch ativo |
| `git merge [branch de origem] [branch de destino]` | Mesclar um branch em um branch de destino |
| `git stash` | Armazenar alterações não commitadas em um diretório de trabalho temporário |
| `git stash list` | Lista todos os stashes disponíveis |
| `git stash apply NUM` | Aplica as mudanças salvas no stash de volta ao seu diretório de trabalho, se nenhum número for especificado, o último stash será aplicado |
| `git stash drop NUM` | Remove uma entrada específica do stash, se nenhum número for especificado, o último stash será removido |
| `git stash clear` | Remover todas as entradas armazenadas no diretório de trabalho temporário |
| `git stash pop` | Aplica as mudanças armazenadas do último stash e remove esse stash |

</div>
</details>

<details>
  <summary>Gerenciar Commits</summary>
<div>

| Comando | Descrição |
| ------- | ----------|
| `git rebase -i HEAD NUM` | Inicia um rebase interativo que inclui os commits em relação ao HEAD (Informe o numero de commits em relação ao HEAD) Alterar pick por "S" nos commits a unir|
| `git rebase -i HASH_DO_COMMIT_ANTERIOR` | Inicia um rebase interativo até o commit especificado pelo hash (hash do commit anterior ao qual deseja trabalhar) Alterar pick por "S" nos commits a unir |
| `git cherry-pick HASH` | Aplica as mudanças introduzidas por um commit específico no topo da branch atual |
| `git bisect start` | Inicia uma sessão de bisect, uma técnica para encontrar um commit específico que introduziu um problema |
| `git bisect bad HEAD` | Marca o commit atual como ruim, indicando que o problema está presente |
| `git bisect good HASH` | Marca o commit como bom |
| `git bisect good 'ou' bad` | Informar ao bisect |
| `git bisect reset` | Sai do modo de bisect e restaura o estado do repositório para o estado anterior ao início |
| `git show HASH` | Mostra os detalhes do commit especificado pelo hash |
| `git log` | Visualizar todos os commits |
| `git log -p` | Visualizar todos os commits com mais informações |
| `git log --oneline` | Visualizar todos os commits com menos informações |
| `git log -n NUM` | Limitar o numero de commit exibidos |
| https://devhints.io/git-log| Criar logs personalizados |
| `git diff` | Exibe as diferenças entre as mudanças no seu diretório de trabalho e o que está na área de preparação |
| `git diff COMMIT1 COMMIT2` | Exibe as diferenças entre dois commits específicos |
| `git diff HEAD` | Exibe as diferenças entre o diretório de trabalho e o último commit |
| `git diff NOME_DO_ARQUIVO` | Exibe as diferenças em um arquivo específico |

</div>
</details>

<details>
  <summary>Desfazer Alterações</summary>
<div>
 
| Comando | Descrição |
| ------- | ----------- |
| `git rm -r [pasta]` | Remove de forma definitiva uma pasta e todo o seu conteúdo do controle de versão |
| `git rm [arquivo]` | Remove um arquivo do controle de versão |
| `git revert HASH` | Reverter ultimo commit |
| `git revert -n <hash-do-ultimo-commit-a-manter>` | Reverter uma série de commits |
| `git reset --hard HASH` | Remover commit e suas alterações |
| `git reset --soft HASH` | Remover commit e manter alterações |
| `git commit --amend` | Alterar ultimo commit |
| `git rm [arquivo]` | Remove um arquivo do controle de versão |
| `git clean -nd` | Visualiza quais arquivos não rastreados seriam removidos pelo `git clean` sem realmente executar a remoção |
| `git clean -fd` | Remove arquivos e pastas não rastreados (cuidado ao usar esse comando) |
| `git clean -i` | Inicia uma remoção interativa de arquivos não rastreados |

</div>
</details>

<details>
  <summary>Comandos do Terminal </summary>
<div>

| Comando | Descrição |
| ------- | --------- |
| `cd [caminho]` | Altera o diretório atual |
| `mkdir [nome]` | Cria um novo diretório |
| `ls` | Lista todos os arquivos no diretório |
| `ls NOME-DA-PASTA` | Lista todos os arquivos da pasta |
| `ls -a` | Lista todos os arquivos no diretório, incluindo os ocultos |
| `clear` | Limpar a tela do terminal |
| `Touch [nome.txt]` | Criar um arquivo vazio |
| `nano [nome.txt]` | Editor de texto simples para editar o arquivo especificado |
| `cat [nome.txt]` | Exibe o conteúdo de um arquivo |
| `rm [arquivo]` | Remover arquivos |
| `rm -rf [dir]` | Remove um diretório e seu conteúdo de forma recursiva |
| `pwd` | Exibe o caminho completo do diretório atual |
| `mv` | Move ou renomeia arquivos e diretórios |
| `sudo` | Executa um comando com privilégios de administrador |

</div>
</details>

## Versionamento Semântico

<details>
    <summary>O que é SemVer?</summary>

</details>

<details>
  <summary>Especificação de versionamento semântico</summary>
<div>
 
  </div>
</details>

<details>
  <summary>Por que usar?</summary>
<div>
 
  </div>
</details>

## Estratégias do GitFlow

<details>
  <summary>Introdução ao GitFlow</summary>
<div>
 
  </div>
</details>

<details>
  <summary>Main</summary>
<div>
 
  </div>
</details>

<details>
  <summary>Develop</summary>
<div>
 
  </div>
</details>

<details>
  <summary>Feature</summary>
<div>
 
  </div>
</details>

<details>
  <summary>Hotfix</summary>
<div>
 
  </div>
</details>

<details>
  <summary>Release</summary>
<div>
 
  </div>
</details>




