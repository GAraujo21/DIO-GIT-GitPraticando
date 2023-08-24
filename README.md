# DIO | Resumos Git e GitHub

Repositório para armazenar resumos sobre o Git e GitHub do curso Versionamento de Código com Git e GitHub.

## 📖 Documentação 
- [Documentação Git](https://docs.github.com/pt)
- [Git Hub](https://github.com/)
## 💻 Comandos no Respositório Local


| Comandos | O que fazem |
|----------|-------------|
| Gravando alterações no repositório local | [Resumo](https://web.dio.me/course/versionamento-de-codigo-com-git-e-github/learning/599dd3dd-d189-474f-a55c-22f37b4472da?back=/track/santander-bootcamp-2023-fullstack-java-angular&tab=undefined&moduleId=undefined) 
| **cd (nome da pasta)** | mudamos através do bash, a pasta q estamos.
| **touch (nome da pasta/nome do arquivo.tipo)** | criar um arquivo dentro da pasta que você indicar. Exemplo: touch resumo/resumos.md
|**echo (arquivo/texto que irá adicionar > arquivo onde o antecessor será adicionado)** | adiciona um arquivo dentro de algum outro. Exemplo echo “Olá mundo” > arquivo-exemplo.txt; ou echo resumos/ > .gitignore;
|**git init** | inicializa um repositório local na pasta em que você está |
|**rm -rf (nome do git // .git)** | “rm”é a abreviação para remove, “r” é "recursivo", ou seja, o comando irá percorrer todos os diretórios e subdiretórios para excluir arquivos, e “f” indica "force" ou "forced", o que significa que o comando não solicitará confirmação antes de excluir os arquivos um comando que remove diretórios e arquivos de forma recursiva e sem pedir confirmação. Esse comando foi usado para excluir um repositório git que foi inicializado erroneamente. |
|**git restore (nome do arquivo a ser restaurado)** | caso você tenha feito uma alteração sem querer, e usar o git status, vai aparecer que houve modificação, mas pode usar o git restore para restaurar o arquivo. |
| **git commit -m “(msg a commitar)”** | serve para mandar mensagem das alterações que foram feitas. Geralmente vem após alguma alteração, modificação, adicionamento ou exclusão de algum arquivo. |
|**git commit –amend -m “(msg a commitar)”**| você edita o último commit.|
| **git reset –soft (a hash do commit que queremos retornar)** | você desfaz o commit mais recente, mas mantém as alterações na área de preparação (staging area) e no diretório de trabalho. Isso significa que as alterações que você tinha preparado para o commit anterior permanecerão na área de preparação e também estarão presentes em seus arquivos de trabalho.|
|**git reset –mixed (a hash do commit que queremos retornar)** | é o comando padrão do reset. Ele desfaz o commit mais recente e remove as alterações da área de preparação (staging area), mas mantém as alterações no diretório de trabalho. |
|**git reset --hard (a hash do commit que queremos retornar)**| Essencialmente, com ***git reset*** --hard, você está descartando todas as alterações no diretório de trabalho e na área de preparação até o commit especificado, o que pode ser perigoso porque as alterações não salvas serão perdidas permanentemente |
|**git reflog** | é usado no Git para exibir o log de referências, que inclui informações sobre as mudanças de referência, como movimentos de branches e redefinições (resets). Ele permite que você veja um histórico detalhado das ações que afetaram as referências do Git no seu repositório.|
| **git reset (nome do arquivo)** | Remove o arquivo x da área de preparação, mantendo as alterações no arquivo no diretório de trabalho.|
| **git restore –staged (nome do arquivo) •	git restore –staged (nome do arquivo)** | Move as alterações do arquivo x da área de preparação de volta para o diretório de trabalho |

#### ***OBS.:*** *essas alterações devem ser feitas aqui, antes de enviadas ao repositório remoto. O ideal, caso já tenha enviado os arquivos, é subir outro arquivo e por no commit explicando.*

## ⌨️👨‍💻🫵 Comandos GitBash para Repositório Remoto
| Comandos | O que fazem |
|----------|-------------|
|**git add origin (URL do github)**| está vinculando o repositório local ao remoto.|
|**git branch -M main** | forçando a alteração do nome da branch, da atual para main.|
|**git push - u origin main** | é usado para enviar suas alterações locais para um repositório remoto no Git. ***‘git push’***: É o comando que envia suas alterações locais para um repositório remoto; ***‘-u’***: É a opção abreviada de ***--set-upstream***, que configura a branch local como a upstream (ramificação principal de rastreamento) da branch no repositório remoto; ***‘origin’:*** É o nome do repositório remoto padrão. O nome "origin" é frequentemente usado para se referir ao repositório remoto a partir do qual você clonou ou onde você deseja enviar suas alterações; ***‘main’***: É o nome da branch local que você deseja enviar para a branch correspondente no repositório remoto.|
|**git pull** | O comando ***git pull*** é usado para buscar as alterações mais recentes de um repositório remoto e incorporá-las ao seu repositório local. Basicamente, ele combina duas ações: ***git fetch***, que busca as alterações do repositório remoto, e ***git merge***, que incorpora essas alterações à sua branch local. Pode ser também git pull origin main. |
|**git checkout -b (nome da branch)** | Cria uma nova branch e muda para ela direto. |
|**git checkout (nome da branch)** | Muda para a branch chamda |
|**git branch -v** | É usado para listar os branches existentes no seu repositório Git, juntamente com informações adicionais sobre o último commit em cada branch. A opção -v significa "verbose" (detalhado), e ela exibe o hash do último commitÉ usado para listar os branches existentes no seu repositório Git, juntamente com informações adicionais sobre o último commit em cada branch. A opção -v significa "verbose" (detalhado), e ela exibe o hash do último commit |
|**git branch** | Lista todas as branchs existentes no repositório |
|**git merge (nome da branch que quer mesclar)** | mescla uma branch na outra |
|**git branch -d (nome da branch)** | é usado para excluir um branch local que já foi completamente mesclado (merged) em outro branch |
|**git fetch origin main** | é usado para buscar as alterações mais recentes do branch "main" no repositório remoto chamado "origin". ***‘git fetch:’*** Isso instrui o Git a buscar as informações mais recentes do repositório remoto. ***'origin':*** É o nome do repositório remoto de onde você deseja buscar as informações. Geralmente, "origin" é o nome padrão dado ao repositório remoto de onde você clonou seu repositório local. ***‘main’:*** É o nome do branch que você deseja buscar do repositório remoto. Neste caso, "main" é o nome do branch. |
|**git diff** | é usado para mostrar as diferenças entre as alterações não confirmadas (unstaged) nos seus arquivos em comparação com o último commit |
|**git diff (branch1 e branch2)** | mostra a diferença entre uma branch e outra |
|**git clone URL --branch (nome da branch) –single-branch** | está clonando uma branch especifica e só ela, de um repositório remoto. |
|**git stash** | é usado para temporariamente salvar as alterações não confirmadas (unstaged e staged) em um local temporário chamado "stash", permitindo que você limpe sua área de trabalho para realizar outras operações, como alternar de branch ou buscar alterações remotas. Isso é útil quando você não deseja fazer um commit das alterações em andamento, mas precisa alternar para um estado diferente no seu repositório. |
|**git stash list** | Para ver a lista de stashes guardados, você pode usar o comando |

## 🔍 Referências 
- [DIO](https://web.dio.me/)
