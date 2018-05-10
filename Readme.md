# Git e Github

### Estados do Git

	1- Untracket: É quando o arquivo foi inserido no repositório, mas o git não reconhece o arquivo ainda.
	2- Unmodified: Arquivo adicionado no git, mas não foi modificado
	3- Modified: Arquivo que foi modificado no git
	4- Staged: Enviar o arquivo para uma área reservada para ser commitado

O ciclo do GIT começa no 1 mas fica alterando entre 2, 3 e 4.

### Comandos do Git

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

### Inserir os arquivos do repositório local / remoto

	echo "# gitcourse" >> README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin git@github.com:gpd38/gitcourse.git
	git push -u origin master

### Criando copia de projeto de outras pessoas

	Na tela inicil do github existe um botão chamado "FORK". Este comando copia o repositório de outra pessoa para seu github. Após as modificações o github envia para o dono do projeto.

### Branches

	- Pode modificar sem alterar o local principal.
	- Múltiplas pessoas tabalhando.
	- Evita conflitos.

	Para criar branches utilize o comando git checkout -b <nome_do_branch>.

	Listar os branches utilize o comando git branch.

	Para apagar uma branch utilize o comando git branch -D <nome_do_branch>.

	Para mudar de uma branch para outra utilize o comando git checkout <nome_do_branch>.

###### Unindo Branches (Merge)

	O merge não é uma operação destrutiva, ou seja, ele não apaga o commit, ele cria um novo.

	C1 <- C2 <- C3 <- C4 <-------- C7
                   <- C5 <- C6 <-- C7

    O commit C7 une os commits C4 + C5 + C6