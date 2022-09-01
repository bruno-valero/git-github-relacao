# Git e Git Hub

O git gerencia o versionamento de arquivos local, ou seja na sua máquina, já o git hub gerencia o vercionamento de arquivos na nuvem. Isso torna possível operar num mesmo projeto a partir de máquinas diferentes.

## Commit de Arquivos do Git para o Git Hub

Para fazer o "upload" de um arquivo de sua máquina para o Guit Hub, primeiro certifique-se de [instalar o git](https://git-scm.com/downloads) em seu computador. Feito isso crie um diretório (pasta) para seu projeto e comece a trabalhar nele, quando você achar necessário fazer o "upload" do seu progresso, crie um repositorio no **Git Hub** com o nome do seu projeto (exemplo: meuprojeto), depois vá na pasta do projeto, pressione o botão direito do mouse e selecione **Git Bash Here**, é como se fosse o terminal do Git. Então você vai digitar as instruções abaixo:

`git init` (pressione ENTER) ----inicializa o Git<br><br>
Caso você queira enviar apenas um dos arquivos da pasta:<br>
`git add seuarquivo.extensão` (pressione ENTER) ----adiciona o arquivo na lista do commit<br><br>
Caso você queira enviar todos os arquivos da pasta:<br>
`git add .` (pressione ENTER) ----adiciona os arquivos na lista do commit<br><br>
`git commit -m "Título do seu Commit"` (pressione ENTER) ----cadastra os arquivos da lista no Git<br><br>
`git branch -M "main"` (pressione ENTER) ----altera a pranch para **main**<br><br>
copie o link do seu repositório recém criado no Git Hub (exemplo: https://github.com/seuperfil/seuprojeto.git)<br>
`git remote add origin "https://github.com/seuperfil/seuprojeto.git"` (pressione ENTER) ----faz a conexão com o repositório do Git Hub<br><br>
`git push -u origin main` (pressione ENTER) ----envia os arquivos do Git para o Git Hub<br><br>
Agora deve aparecer uma janela para fazer o login no Git Hub, clicke em **Entrar com o Browser** (algo do tipo), então entre no seu Git Hub e confirme que você autoriza o envio desse arquivo e que está ciente de que essa máquina a partir de agora poderá enviar arquivos livremente para seus repositórios do Git Hub. Agora basta dar refresh na página do Git Hub e verá todos os arquivos que enviou.

## Versionamento e Alteração dos Arquivos

A partir do momento que você enviar um arquivo a algum repositório do Git Hub, não será mais necessário criar a conexão para enviar as alterações feitas nesses arquivos.

Então caso você fez alguma alteração no seu projeto e quer enviar essas alterações ao Git Hub, vá no diretório (pasta) onde está o projeto, clicke com o botão direito do mouse, selecione **Git Bash Here** e digite as seguintes instruções:


Caso você queira enviar apenas um dos arquivos da pasta:<br>
`git add seuarquivo.extensão` (pressione ENTER) ----adiciona o arquivo na lista do commit<br><br>
Caso você queira enviar todos os arquivos da pasta:<br>
`git add .` (pressione ENTER) ----adiciona os arquivos na lista do commit<br><br>
`git commit -m "Título do seu Commit"` (pressione ENTER) ----cadastra os arquivos da lista no Git<br><br>
`git push origin main` (pressione ENTER) ----envia os arquivos do Git para o Git Hub<br><br>

## Branches e Ramificações

Até agora nós vimos como fazer conexão entre o Git e um repositório do Git Hub, como incluir um arquivo nesse repositório, e também como substituir ou alterar esses arquivos. Agora vamos ver como fazer ramificações através das Branches.

As ramificações servem para auxiliá-lo a contribuir com seu projeto sem comprometer os arquivos inicialmente enviados. Com isso é possível desenvolver alguns recursos em paralelo, sem precisar alterar o projeto principal. Ou polir seu projeto sem o risco de "estragar" o que tinha sido feito anteriormente, podendo até fazer comparações de como o projeto estava em cada etapa de seu desenvolvimento.

Para criar uma nova Branch, primeiro abra o **Git Bash** (conforme explicado anteriormente) no diretório (pasta) do projeto que contém as alterações que você quer ramificar, então digite as instruções:

`git checkout -b "nome-da-nova-branch"` (pressione ENTER) ----cria uma nova Branch e troca da Branch principal para a nova Branch<br><br>
Caso você queira enviar apenas um dos arquivos da pasta:<br>
`git add seuarquivo.extensão` (pressione ENTER) ----adiciona o arquivo na lista do commit<br><br>
Caso você queira enviar todos os arquivos da pasta:<br>
`git add .` (pressione ENTER) ----adiciona os arquivos na lista do commit<br><br>
`git commit -m "Título do seu Commit"` (pressione ENTER) ----cadastra os arquivos da lista no Git<br><br>
`git push origin "nome-da-nova-branch"` (pressione ENTER) ----envia os arquivos do Git para o Git Hub na nova Branch<br><br>
Caso você queira que sua branch principal seja atualizada com todas as alterações feitas na sua nova branch:<br>
`git checkout main` (pressione ENTER) ----troca da nova Branch para a Branch principal<br><br>
`git merge nome-da-nova-branch` (pressione ENTER) ----atualiza a Branch principal com todas as alterações feitas na nova Branch<br><br>
`git push origin main` (pressione ENTER) ----envia os arquivos do Git para o Git Hub na Branch principal<br><br>
