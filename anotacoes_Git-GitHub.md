Principais comandos GIT	

git config --global user.name "Fulano de tal"
git config --global user.email fulanodetal@exemplo.com
	configura o usuário e endereço de email que será carimbada nos commits para identificar quem fez as alterações
	o git ira utilizar esta informação para todas alterações neste sistema.
	Se quiser alterar o nome/email para algum projeto especifico utilize o comando sem a opção --global
git config --global --unset user.name
	remover configuração de username
	
git config user.name
	exibe o username configurado
	
git config user.email
	exibe o email configurado

git config --list 
	exibe todas as configurações
	
[git remote add origin] (https://github.com/andercol/livro-receitas.git)

​	linka o repositorio local com o repositorio remoto
​	Obs.: orign é um apelido, podendo ser subistituido por outro nome mas por convenção se utiliza o origin
​	
git remote rm origin ou upstream
​	remove um repositorio remoto

git remote -v
	lista os repositorios remotos cadastrados.
	
git push origin master	
	empurra o repositorio local para o repositorio remoto.

--------------
	Quando há conflitos é necessário baixar a versão do repositorio remoto e resolver o conflito do arquivo editando e deixando na versão final.
	Depois git add * e git commit -m "xxxxx"
	git push origin master
-------------

readme do git utiliza o padrão Markdown
	utilize o Typora.exe para editar.
	
git init
	inicia um repositório dentro de um diretório
	
git clone url
	copia um repositório remoto
	git remote -v dentro do repositorio clonado ira mostrar para onde ele está apontado.
	
Git remote add upstream git@github.com:gatein/gatein-portal.git
	adiciona um repositorio upstream
	Para sincronizar um repositorio utilize os 3 comandos abaixo de tempos em tempos
		Git checkout master
		Git fetch upstream
		Git rebase upstream/master
	ref.: https://pt.stackoverflow.com/questions/3389/como-atualizar-sincronizar-o-master-do-meu-reposit%C3%B3rio-no-github-com-o-master-or
	
	
git add . ou git add <<nome-arquivo>>
	adiciona arquivos na lista a ser comitado

git commit - m "mensagem de commit"
	salva as alterações realizadas no repositório

git push
	envia os commits locais para o repositório remoto

git pull
	atualiza o repositório local com as alterações existente no repositório remoto.

git merge
	junta alterações de duas branchs e também é utilizado na resolução de conflitos de alteração

git status
	exibe informações sobre o projeto e arquivos existentes comitados e não comitados

git log
	exibe os commits os autores e todo historico de alterações do projeto.

git branch <<nome da branch>>
	cria uma nova ramificação para iniciar uma nova alteração do projeto sem alterar a branch master "produção"