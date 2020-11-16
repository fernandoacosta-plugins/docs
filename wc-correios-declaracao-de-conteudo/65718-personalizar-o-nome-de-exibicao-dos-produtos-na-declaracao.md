# Personalizar o nome de exibição dos produtos na declaração

Se por algum motivo você quer alterar o nome de algum produto na hora de imprimir a declaração, você pode fazer isso utilizando o código a seguir:  

add\_filter( 'wc\_correios\_declaration\_product\_name', 'wc\_correios\_declaration\_custom\_name', 10, 3 );  
function wc\_correios\_declaration\_custom\_name( $name, $item, $order ) {  
  $name = 'Nome personalizado';

  return $name;  
}

[Ver no Gist](http://gist.github.com/fernandoacosta/03b405792ae85f869af13d1033b13b30#file-functions-php).

Neste exemplo iremos alterar o nome de todos os produtos. Mas repare que há os parâmetros ```php
$item
``` e ```php
$order
```, então você pode criar regras avançadas, caso precise.

___

Keywords: