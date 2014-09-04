# Tema filho roots-fr

Instruções para personalização do Tema Roots podem ser encontradas
em [http://roots.io/roots-101/](http://roots.io/roots-101/)

Temas filho necessitam obrigatóriamente apenas do arquivo style.css, entretanto
suponha que desejemos usar uma Entity Product e uma Entity Vehicle

Poderemos personalizar os arquivos abaixo:

    functions.php, archive-product.php, single-product.php, single-vehicle.php

e o diretório templates poderá conter:

    content-page.php, content-product.php, content-single.php, content-vehicle.php e page-header.php

Cada arquivo adicional a ser personalizado deve ser copiado de seu original
no diretório roots

## Passo a passo para criar o tema filho à partir do tema roots

    pwd # certifique-se de estar em roots-fr
    # extras.php pode ser alterado para personalizar o tema
    mkdir lib
    cp ../roots/lib/extras.php lib
    # conte[udo woocommerce
    echo "<?php woocommerce_content(); ?>" > archive-product.php
    echo " " >> archive-product.php
    # personalização da configuração
    cp ../roots/lib/config.php lib
    # lib/init.php is used to register navigation menus, sidebars,
    # and define add_theme_support() for WordPress core functionality
    # such as post thumbnails. You should also define your custom
    # image sizes with add_image_size() and add any support for post
    # formats in this file.
    cp ../roots/lib/init.php lib
    # lib/scripts.php is used to tell WordPress which CSS and JS files
    # to enqueue. Only one CSS file is enqueued: assets/css/main.min.css.

Scripts are enqueued in the following order:

The latest jQuery via Google CDN with local fallback (if enabled in lib/config.php) in the header
A lean Modernizr build in the header
assets/js/scripts.min.js in the footer






