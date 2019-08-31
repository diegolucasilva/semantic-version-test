# semantic-version-test

## Imagem utilizada: 
docker run -it ubuntu

## Instalar os pacotes: 
    apt-get update; apt-get install -y nodejs npm git; npm i -g npx

## Configurar git:
	git config --global user.email"diego.lucasilva@gmail.com"
	git config --global user.name "Diego Lucas"
	git remote add origin git@github.com:diegolucasilva/semantic-version-test.git
	cd ~/.ssh/ ; ssh-keygen; cat ~/.ssh/id_rsa.pub
	ssh -T git@github.com

## Configurando commitlint
	npm install -g @commitlint/cli @commitlint/config-angular
	echo "module.exports = {extends: ['@commitlint/config-angular']}" > ~/commitlint.config.js
	echo "cat "$1" | commitlint; exit $?" > ~/githooks/commit-msg
  	git config --local core.hooksPath ~/githooks/

## Para publicar: 
    npx semantic-release --no-ci

####  Fiz mas acho que não precisa:
##### Instalar os modulos (versionei a pasta node_mudules pensando na esteira, não sei se é possivel deixar os módulos já na máquina tipo igual o maven no .m2)
      npm install
      
      
##### Configurar token
    export GH_TOKEN="my value"      # gerar o token no GitHub

##### Install os plugins manualmente: 
    npm i -D semantic-release@next @semantic-release/git@next @semantic-release/commit-analyzer@next @semantic-release/release-notes-generator@next @semantic-release/npm@next @semantic-release/changelog@nex
    npm install -D commitizen
    npm i -D husky
    npm install -g @commitlint/cli @commitlint/config-conventional
    echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js


	

    
