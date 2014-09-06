# Personalizando o Tema Roots

As instruções podem ser encontradas em [http://roots.io/roots-101/](http://roots.io/roots-101/)

A ideia é criar um tema filho e manter o diret[orio roots inalterado para permitir que baixemos as atualizações sem afetar o projeto.

O tema filho ficará em roots-fr

    git submodule init
    git submodule update
    cd roots
    sudo npm install -g grunt-cli bower
    npm install
    grunt dev
    grunt build

Após o Build os seguintes arquivos e diretórios são criados/atualizados

    roots/assets/css/main.css
    roots/assets/css/main.css.map
    roots/assets/css/main.min.css
    roots/assets/js/scripts.js
    roots/assets/js/scripts.min.js
    roots/assets/js/vendor/
    roots/assets/manifest.json
    roots/assets/vendor/


