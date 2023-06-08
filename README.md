# Comandos do Git :sunglasses:

<div align="center">
  <img src="https://github.com/PW-creator/gitbashcomandos/assets/72416696/ae19c684-b34a-4d6f-9c29-12ab42b3e6ab" widht="300px" height="300px"/>
</div>

### Organizei algumas anotações minhas de comandos usuais do dia-a-dia com o git e gihtub e estou compartilhando aqui para novatos no tema ou experientes que queiram um local fixo com essas infos e querem utilizar de base no ambiente de desenvolvimento.

<hr>

### Comandos Iniciais:

git init - Inicializa um repositório.
  - Função: Cria um novo repositório Git vazio ou reinicializa um repositório existente.

git status - Obtém o status do repositório.
   - Função: Mostra o status atual do repositório, exibindo os arquivos modificados, adicionados ou excluídos.
   
<hr>

### Configuração do Autor:

Antes de realizar qualquer interação com o Git, é necessário informar suas informações de autor para que as alterações sejam atribuídas corretamente. Para fazer isso:

git config --local user.name "Seu nome aqui"
  - Função: Configura o nome do autor localmente para o repositório atual.
  
git config --local user.email "seu@email.aqui"
  - Função: Configura o email do autor localmente para o repositório atual.
  
Obs: Você pode substituir --local por --global para configurar as informações de autor globalmente na máquina.

Exemplo:

git config --global user.name "Seu nome aqui"
git config --global user.email "seu@email.aqui"

<hr>

### Gerenciamento de Alterações:

git add . - Adiciona todos os arquivos para monitoramento do Git.
  - Função: Adiciona todas as alterações feitas nos arquivos do repositório ao índice do Git, preparando-os para o commit.
  
git commit -m "<mensagem>" - Realiza um commit com uma mensagem descritiva.
  - Função: Grava as alterações feitas no repositório como um novo commit, com uma mensagem que descreve as alterações.
 
git log -p - Visualiza detalhadamente todos os logs de alterações.
  - Função: Mostra um histórico detalhado de todos os commits feitos no repositório, exibindo as diferenças das alterações.
  
git log --oneline - Visualiza de forma resumida em uma linha cada commit.
  - Função: Mostra um histórico resumido de todos os commits feitos no repositório, exibindo apenas uma linha por commit.

<hr>

### Ignorar Arquivos:

Crie um arquivo chamado .gitignore na raiz do repositório e liste dentro dele os nomes de arquivos e pastas que deseja ignorar.
  - Função: O arquivo .gitignore define quais arquivos e pastas devem ser ignorados pelo Git ao rastrear as alterações, exemplo abaixo vai ignorar a pasta img:

<div align="center">
  <img src="https://github.com/PW-creator/gitbashcomandos/assets/72416696/00031539-3fd8-401b-ad0e-736743a28fe1"/>
</div>
   
<hr>

### Trabalhando com Ramificações (Branches):

git branch - Lista as branches disponíveis.
  - Função: Exibe uma lista de todas as branches existentes no repositório.
  
git branch <nome> - Cria uma nova branch para desenvolvimento.
  - Função: Cria uma nova branch com o nome especificado, a partir da branch atual.
  
git checkout <nome> - Altera para a branch especificada.
  - Função: Altera o HEAD (ponteiro para a branch atual) para a branch especificada.
  
git merge <nome-da-branch> - Realiza a mesclagem (merge) de uma branch na branch atual.
  - Função: Combina as alterações da branch especificada na branch atual.
  
git rebase <nome-da-branch> - Realiza o rebase da branch especificada na branch principal.
  - Função: Aplica as alterações da branch especificada no topo da branch principal, reescrevendo a história do repositório.
  
<hr>

### Trabalhando com Repositórios Remotos:

git remote - Mostra o nome do repositório remoto.
  - Função: Exibe o nome do repositório remoto configurado para o repositório local.
  
git remote add <nome> <url> - Adiciona um novo repositório remoto.
  - Função: Adiciona um novo repositório remoto com o nome e a URL especificados.
  
git remote -v - Exibe as URLs de fetch e push do repositório remoto.
  - Função: Exibe as URLs configuradas para enviar e receber dados do repositório remoto.
  
git clone <endereço-do-repositório> <nome-da-pasta> - Clona um repositório remoto para uma pasta local.
  - Função: Cria uma cópia local de um repositório remoto na pasta especificada.
  
git push <nome-do-repositório> <branch> - Envia os dados para o repositório remoto.
  - Função: Envia as alterações do repositório local para o repositório remoto especificado.
  
git pull <nome-do-repositório> <branch> - Puxa as alterações do repositório remoto.
  - Função: Atualiza o repositório local com as alterações do repositório remoto especificado.
  
git remote rename <nome-atual> <novo-nome> - Renomeia um repositório remoto.
  - Função: Altera o nome de um repositório remoto configurado.

<hr>

### Outros Comandos Úteis:

mkdir <nome-da-pasta> - Cria uma nova pasta.
  - Função: Cria uma nova pasta com o nome especificado.
  
cd .. - Volta para a pasta anterior.
  - Função: Navega para o diretório pai do diretório atual.
  
git diff - Mostra as diferenças entre o código atual e o código não commitado.
  - Função: Exibe as diferenças entre o estado atual dos arquivos e o último commit.
  
git checkout -- <nome-do-arquivo> - Desfaz as alterações feitas em um arquivo.
  - Função: Descarta as alterações feitas em um arquivo específico e o restaura para o estado do último commit.
  
git reset HEAD <nome-do-arquivo> - Remove um arquivo do índice (staging area).
  - Função: Remove um arquivo do índice (staging area), permitindo que suas alterações sejam desfeitas antes de fazer um novo commit.
  
git revert <hash-do-commit> - Desfaz um commit específico.
  - Função: Desfaz um commit específico, criando um novo commit que reverte as alterações introduzidas pelo commit anterior.
  
git stash - Salva um status para uso posterior, sem fazer commit.
  - Função: Armazena temporariamente as alterações atuais em um stash, permitindo que você limpe o diretório de trabalho sem fazer commit.
  
git stash list - Lista todos os stashes salvos.
  - Função: Exibe uma lista de todos os stashes (estados salvos) disponíveis no repositório.
  
git stash apply <número> - Aplica uma alteração específica do stash.
  - Função: Aplica uma alteração específica do stash ao diretório de trabalho, preservando o stash para uso futuro.
  
git stash drop <número> - Remove um item específico do stash.
  - Função: Remove um item específico do stash, excluindo-o permanentemente do repositório.
  
git stash pop - Aplica as modificações salvas e remove o stash.
  - Função: Aplica as alterações salvas pelo stash mais recente ao diretório de trabalho e remove o stash da lista de stashes.
  
git tag - Mostra todas as tags disponíveis.
  - Função: Exibe uma lista de todas as tags (versões) disponíveis no repositório.
  
git tag -a <nome-da-versão> -m "<mensagem>" - Adiciona uma nova tag (versão) ao projeto.
  - Função: Cria uma nova tag com o nome especificado e uma mensagem descritiva.
  
Exemplo:

git tag -a v0.1.0
  
git tag -a v0.1.0 -m "Primeira versão BETA do projeto"
  
  

# Obrigado a todos que visitaram esse repositório, estarei fazendo mais conteúdos como esses que podem agregar a comunidade principalmente da galera que tá començando.
