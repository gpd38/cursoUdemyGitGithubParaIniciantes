Estados do Git

	1- Untracket: É quando o arquivo foi inserido no repositório, mas o git não reconhece o arquivo ainda.
	2- Unmodified: Arquivo adicionado no git, mas não foi modificado
	3- Modified: Arquivo que foi modificado no git
	4- Staged: Enviar o arquivo para uma área reservada para ser commitado

O ciclo do GIT começa no 1 mas fica alterando entre 2, 3 e 4.

Comandos do Git

	- git status: Informar como está o git/repositório neste momento.
	- git add: Insere o arquivo na área que será enviada para o git
	- git commit: 
	- git log: Informa o número do commit, autor e data
		- git log --graph
	- git diff: O git mostra as modificações 
	- git checkout: Resetar a ultima modificação efetuada em um arquivo do git
	- git HEAD <commit>: A alteração que tinha sido desfeita e commitada é refeita, ou seja, o arquivo volta para a versão da suposta edição errada.
	- git reset:
		--soft: 
		--mixed: Arquivo modificado, mas não adicionado no stage
		--hard(Cuidado): Matar o commit e qualquer modificação. Limpa até do log.
	- git clone: clonar todo o repositório remoto para sua maquina local
	- fork: copia o repositório de outra pessoa para seu github. Após as modificações o github envia para o dono do projeto.

Inserir os arquivos do repositório local / remoto

	echo "# gitcourse" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin git@github.com:gpd38/gitcourse.git
	git push -u origin master