# semantic-version-test

Na máquina do dev só é necessário instalar o node e configurar o commitlint.

## Imagem utilizada: 
docker run -it ubuntu

## Instalar os pacotes: 
    apt-get update; apt-get install -y nodejs npm git; npm i -g npx
  
## Install plugins: 
    npm i -g semantic-release@next @semantic-release/git@next @semantic-release/commit-analyzer@next @semantic-release/release-notes-generator@next @semantic-release/npm@next @semantic-release/changelog@next
    npm install -g @commitlint/cli @commitlint/config-conventional
    echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
    
## Configurando commitlint
	npm install -g @commitlint/cli @commitlint/config-angular
	echo "module.exports = {extends: ['@commitlint/config-angular']}" > ~/commitlint.config.js
	echo "cat "$1" | commitlint; exit $?" > ~/githooks/commit-msg
  	git config --local core.hooksPath ~/githooks/

## Configurar git:
	git config --global user.email"diego.lucasilva@gmail.com"
	git config --global user.name "Diego Lucas"
	git remote add origin git@github.com:diegolucasilva/semantic-version-test.git
	cd ~/.ssh/ ; ssh-keygen; cat ~/.ssh/id_rsa.pub
	ssh -T git@github.com

## Para publicar: 
    npx semantic-release --no-ci

## Variaveis configuradas pipeline:
    GH_TOKEN, GIT_AUTHOR_EMAIL, GIT_COMMITTER_EMAIL, GIT_AUTHOR_NAME, GIT_COMMITTER_NAME


	

    
