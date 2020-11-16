# Imprimir etiqueta dos Correios junto com a Declaração de Conteúdo

Se você quer imprimir etiquetas de envio junto com a declaração de conteúdo, basta adicionar esta linha de código ao seu site ([veja aqui onde adicionar](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)):

add\_filter( 'wc\_correios\_declaration\_print\_labels', '\_\_return\_true' );  

Após isso, você verá as etiquetas logo abaixo da declaração, prontas para serem recortadas.

[![](https://s3.eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/708d65dc-3730-4ff1-8b97-1ef38036fe6f.png)](https://s3.eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/708d65dc-3730-4ff1-8b97-1ef38036fe6f.png)

  

___

Keywords:etiqueta,etiquetas,envio,correios