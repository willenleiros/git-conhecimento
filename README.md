# Git

Git é um sistema de controle de versão distribuído gratuito e de código aberto projetado para lidar com tudo, desde projetos pequenos a muito grandes com velocidade e eficiência.

# Iniciando

| Comando | Resultado |
| :--------: | :--------: |
| `git init`   |  Inicia um projeto git localmente  |
| `git config --global user.name "Fulano de Tal"`   |  Configura um nome de usuario com escopo global para ser utilizado nos trabalhos com o Git  |
| `git config --global user.email fulanodetal@exemplo.br`   |  Configura um email com escopo global para ser utilizado nos trabalhos com o Git  |

# Trabalhos em uma Sprint

Para trazer uma cópia do projeto que está em um repositorio remoto você deve executar o seguinte comando `https://github.com/willenleiros/git-conhecimento.git`

| Comando | Resultado |
| :--------: | :--------: |
| `git checkout dev`   |  Muda para branch de desenvolvimento  |
| `git pull origin dev`	|	Puxa o trabalho para o repositório local	|
| `git checkout -b feature/nome-branch`  | Cria uma nova branch de trabalhos e muda para a mesma  |
| `git add .`  | Adiciona todas as alterações na área de preparação do Git |
| `git commit -m "feat: ops fiz alguma coisa" -m "issue: IMW-700"`  | Marcar as alteracões feitas que estão na área de preparação e adiciona mensagens explicativas sobre o trabalho  |
| `git push origin HEAD`  | Envia o trabalho para repositório remoto criando uma branch com mesmo nome da branch local |

# Utilizados diariamente

| Comando | Resultado |
| :--------: | :--------: |
| `git status`  | Verifica alterações feitas no projeto   |
| `git log`  | Ver histórico de commits   |
| `git reset --hard origin/master`  | Descartar projeto local e trazer tudo que tem de novo no git remoto |
| `git remote prune origin`  | Deletar referencias de branch remotas excluídas    |
| `git clean -f`  | Remove arquivos que ainda não estão na área de preparação    |
| `git clean -d`  | Remove diretórios que ainda não estão na área de preparação  |

# Rebase

"Rebase é um dos dois utilitários do Git que se especializam em integrar alterações da ramificação para outra." ([Atlassian](https://www.atlassian.com/br/git/tutorials/rewriting-history/git-rebase))

| Comando | Resultado |
| :--------: | :--------: |
| `git checkout dev`	|	Muda para branch de desenvolvimento	|
| `git pull origin dev`	|	Puxa o trabalho para o repositório local	|
| `git checkout <branch>`	|	Muda para branch onde vai ser feito o rebase	|
| `git rebase dev`	|	Junta o código local com o código online e mostra os conflitos	|
(corrige os conflitos)
| `git add .`	|	Prepara todos os arquivos	|
| `git rebase --continue`	|	Continua o rebase depois de resolver os conflitos manualmente	|
| `:q`	|	"Quit" quando o git mandar a mensagem você responde com esse comando	|
| `git push --force origin HEAD`	|	Envia o trabalho para repositório remoto, criando uma branch com mesmo nome da branch local	|


