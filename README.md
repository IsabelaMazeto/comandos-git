# Comandos-Git
Aqui vai alguns comandos básicos do <a href="https://git-scm.com/book/pt-br/v1/Primeiros-passos-No%C3%A7%C3%B5es-B%C3%A1sicas-de-Git">GIT</a> para iniciantes: ❤️

* INICIALIZA UM REPOSITÓRIO GIT NO SEU PC:
**git init

* COPIA UM REPOSITÓRIO GIT NO SEU PC - MASTER:
**git clone https://isabelamazeto@bitbucket.org/isabelamazeto/teste.git

* REFERENCIA UM REPOSITÓRIO GIT NO SEU PC - MASTER:
**git remote add origin https://github.com/IsabelaMazeto/Comandos-Git.git

* MOSTRA O QUE TEM DE ALTERAÇÃO NA SUA BRANCH:
**git status

* ADICIONAR ARQUIVOS ALTERADOS PARA O COMMIT:
**git add . // ADD TUDO
**git add index.html // SÓ 1 ARQUIVO

* PARA FAZER O COMMIT DOS ARQUIVOS ALTERADOS:
**git commit -m "Primeiro Commit"

* PARA DESFAZER UM COMMIT:
**git reset numero_do_commit_informado_no_gitlog

* SOBE SEU PROJETO PRO REPOSITÓRIO MASTER:
**git push -u origin master

* MOSTRA TODAS AS BRANCHs:
**git branch

* PARA CRIAR UMA NOVA BRANCH:
**git branch nomebranch

* MUDA PARA A BRANCH ESCOLHIDA:
**git checkout nomebranch

* PARA ACESSAR UMA BRANCH JÁ EXISTENTE:
**git branch -t nomebranch origin/nomebranch

* SOBE SEU PROJETO PRA UMA BRANCH ESPECÍFICA:
**git push -u origin nomebranch

* BAIXA AS ALTERAÇÕES DO DIRETÓRIO PRA SUA BRANCH:
**git pull

* MERGE (significa juntar alterações feitas de locais diferentes):
**git merge master** (fazendo o merge entre o feature e a master)

* MOSTRA INFORMAÇÕES DETALHADAS DA BRANCH:
**git log

* PARA EXCLUIR UMA BRANCH:
**git checkout -b nomebranch

## GIT FLOW:

O <a href="https://medium.com/trainingcenter/utilizando-o-fluxo-git-flow-e63d5e0d5e04">Git Flow</a> é uma forma organizada de fazermos o versionamento dos nossos projetos.

* git flow init (para iniciar o Git Flow)
* git flow feature start NomeBranch (para criar uma nova branch)
* git flow feature finish NomeBranch (para finalizar a branch e fazer o merge com a develop)
* git flow release start 1.0.0 (para lançar uma versão)
* git flow release finish "1.0.0" (para finalizar a release)

Temos a master que é a branch principal, ao dar o "git flow init", ele irá criar a branch Develop que é uma cópia da Master, para podermos trabalhar nela com mais tranquilidade caso ocorra algum erro. Ao dar o comando "git flow feature start NomeBranch", este irá criar uma cópia da Develop e nesta branch você irá uma etapa do projeto, ao terminar esta etapa você finaliza essa branch, e ele irá juntar ela com a Develop, depois é só inicar outra branch de outra etapa do projeto que irá fazer. E assim vai até terminar todo o projeto e subir tudo para a Develop, depois que a Develop estiver pronta fazemos a junção com a Master que é a principal, lançando uma release (versão).
