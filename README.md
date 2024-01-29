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
<div>

```
O SemVer, ou Versionamento Semântico, é uma convenção para atribuição de versões a software,
com o objetivo de facilitar a compreensão das mudanças no código pelos desenvolvedores e usuários.
A versão é representada por três números no formato MAJOR.MINOR.PATCH, como por exemplo, 1.2.3.
```

</div>
</details>

<details>
  <summary>Especificação de versionamento semântico</summary>
<div>
 
```
O Versionamento Semântico (SemVer) possui regras claras sobre quando aumentar os números em uma versão.
principais (MAJOR);
secundários (MINOR);
correções (PATCH);

Aqui estão as especificações:

MAJOR version (X.y.z):
Deve ser incrementado quando são feitas alterações incompatíveis com versões anteriores.
Geralmente, isso inclui mudanças significativas que quebram a compatibilidade com versões anteriores,
como alterações na API que não são retrocompatíveis.

MINOR version (x.Y.z):
Deve ser incrementado quando funcionalidades são adicionadas de maneira retrocompatível.
Isso indica a adição de novas funcionalidades ou aprimoramentos à API,
mas sem quebrar a compatibilidade com versões anteriores.

PATCH version (x.y.Z):
Deve ser incrementado para correções de bugs retrocompatíveis.
Indica que foram feitas correções de bugs ou pequenas melhorias
que mantêm a compatibilidade com versões anteriores.

Ao incrementar o MAJOR version, os números MINOR e PATCH devem ser redefinidos para zero.
Exemplo: 1.2.3 → 2.0.0.

Ao incrementar o MINOR version, o número PATCH deve ser redefinido para zero.
Exemplo: 1.2.3 → 1.3.0.

Ao incrementar o PATCH version, apenas o próprio número PATCH deve ser incrementado.
Exemplo: 1.2.3 → 1.2.4.

Versão Inicial (0.y.z):
O SemVer permite que projetos declarem uma fase inicial de desenvolvimento usando a versão principal zero (0.y.z).
A versão inicial (0.y.z) é indicativa de desenvolvimento inicial, onde qualquer coisa pode mudar a qualquer momento.
Durante esta fase, a API pública não deve ser considerada estável.

Versão 1.0.0:
A versão 1.0.0 marca um ponto em que o desenvolvedor considera que a API pública atingiu um nível de estabilidade.
A partir da versão 1.0.0, as regras de incremento de versão são mais claramente definidas,
proporcionando consistência no gerenciamento de versões.

Exemplo Prático:
Se um projeto está em suas fases iniciais, ele pode começar com versões como 0.1.0, 0.2.0,
indicando um desenvolvimento em andamento. Ao atingir a estabilidade e a definição da API pública,
eles podem lançar a versão 1.0.0 para marcar o compromisso com a retrocompatibilidade.
``` 

</div>
</details>

<details>
  <summary>Por que usar?</summary>
<div>
 
```
É uma forma simples de numerar versões, usando três números principais (MAJOR.MINOR.PATCH).
Aqui estão algumas razões para usá-lo:

Entendimento Simples:
Os três números facilitam para desenvolvedores e usuários entenderem as mudanças no software.

Tomada de Decisões Fácil:
Ajuda na decisão de quando aumentar cada parte da versão.

Consistência no Versionamento:
Proporciona consistência, evitando ambiguidades na gestão de versões.

Automatização do Próximo Número de Versão:
Permite a determinação automática do próximo número de versão a ser aplicado
``` 

</div>
</details>

## Estratégias do GitFlow

<details>
  <summary>Introdução ao GitFlow</summary>
<div>

```
O Gitflow foi um método inovador para gerenciar ramificações no Git, 
considerados práticas recomendadas para o desenvolvimento contínuo e DevOps modernos.
Facilita a colaboração, designando funções específicas aos ramos e delineando interações
```
</div>
</details>

<details>
  <summary>Main</summary>
<div>

```
FUNÇÃO:
Representa a branch principal e estável do código. É a versão de produção do software.

USO:
Cada commit nessa branch reflete uma versão do software que foi ou será implantada em produção.
```  
</div>
</details>

<details>
  <summary>Develop</summary>
<div>

```
FUNÇÃO:
É a branch de desenvolvimento principal, onde as novas funcionalidades são integradas
antes de serem enviadas para produção.

USO:
Os desenvolvedores trabalham nas branches de feature e, quando concluídas,
mesclam suas alterações na branch develop para integração.
```   
</div>
</details>

<details>
  <summary>Feature</summary>
<div>

```
Função:
Cada branch de feature representa uma nova funcionalidade ou melhoria específica.

Uso:
As branches de feature são criadas a partir da branch develop,
onde os desenvolvedores implementam e testam suas funcionalidades.
Após a conclusão, a branch de feature é mesclada de volta na develop
```  
</div>
</details>

<details>
  <summary>Hotfix</summary>
<div>

```
Função:
Usada para correções rápidas de bugs críticos em produção.

Uso:
Quando um bug crítico é detectado na versão de produção (branch main),
uma branch de hotfix é criada, a correção é implementada, e
a branch de hotfix é mesclada tanto na main quanto na develop.
```  
</div>
</details>

<details>
  <summary>Release</summary>
<div>

```
Função:
Prepara o código para um próximo lançamento ou versão.

USO:
Quando a develop atinge um ponto estável e está pronta para uma nova versão, uma branch de release é criada.
Essa branch é usada para realizar ajustes finais, testes e preparar a versão.
Após a conclusão, a branch de release é mesclada na main e develop, marcando o lançamento.
``` 
</div>
</details>

## Commit Convencional

<details>
<summary>Resumo</summary>
<div>

```
Conventional Commits é uma convenção para mensagens de commit 
que simplifica a criação de um histórico compreensível. 
Essa abordagem facilita o desenvolvimento de ferramentas automatizadas e 
se alinha ao SemVer, destacando recursos, correções e alterações 
importantes nas mensagens de commit.

```
- A mensagem de commit deve ser estruturada da seguinte forma:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```
</div>
</details>

<details>
<summary>Tipos Padrões</summary>
<div>

```
fix: 
Commits do tipo fix visam corrigir bugs na base de código, 
alinhando-se ao conceito de PATCH no Versionamento Semântico.

feat: 
Commits do tipo feat introduzem novos recursos na base de código, 
seguindo a lógica de MINOR no Versionamento Semântico.

BREAKING CHANGE: 
Commits que incluem um footer BREAKING CHANGE: ou anexam um ! após o tipo/escopo 
indicam alterações significativas na API, 
correlacionando-se com o conceito de MAJOR no Versionamento Semântico.
```
</div>
</details>

<details>
  <summary>Exemplos</summary>
<div>

- Mensagem de commit com descrição e rodapé de alteração significativa

```
feat: permitir que o objeto de configuração fornecido estenda outras configurações

BREAKING CHANGE: a chave `extends` no arquivo de configuração agora é usada para estender outros arquivos de configuração
``` 
***
- Mensagem de commit com ! para chamar a atenção para uma alteração significativa

```
feat!: enviar um e-mail ao cliente quando um produto for enviado
```
***
- Mensagem de commit com escopo e ! para chamar a atenção para uma alteração significativa
```
feat(api)!: enviar um e-mail ao cliente quando um produto for enviado
```
***
- Mensagem de commit com ambos ! e rodapé BREAKING CHANGE
```
chore!: descontinuar o suporte ao Node 6

BREAKING CHANGE: utilizar recursos JavaScript não disponíveis no Node 6.

```
***
- Mensagem de commit sem corpo

```
docs: corrigir ortografia do CHANGELOG
```
***
- Mensagem de commit com escopo

```
feat(lang): adicionar idioma polonês
```
***
- Mensagem de commit com corpo de vários parágrafos e vários rodapés
```
fix: prevenir corridas de solicitações

Introduzir um ID de solicitação e uma referência à última solicitação. Ignorar
respostas recebidas que não sejam da última solicitação.

Remover timeouts que eram usados para mitigar o problema de corrida, mas agora são
obsoletos.

Revisado por: Z
Refs: #123
```
</div>
</details>


