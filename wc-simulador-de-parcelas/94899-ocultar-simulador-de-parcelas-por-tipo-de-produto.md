# Ocultar simulador de parcelas por tipo de produto

<?php  
Se você busca ocultar o simulador para determinados tipos de produto que não possuem simulador, como assinaturas ou membros, você pode usar o código abaixo.

```php
add_filter( 'wcsp_is_available', 'wcsp_hide_post_type', 10, 2 );  
function wcsp_hide_post_type( $is_available, $product ) {  
  $types = array( 'subscription' );  
  if ( $product->is_type( $types ) ) {  
    return false;  
  }   return $is_available;  
}
```

Na lista 3 há a lista de tipos de produto que não terá o simulador. Se você quer incluir, por exemplo, um tipo de produto chamado booking, a linha 3 ficaria dessa forma:

  $types = array( 'subscription', 'booking' );

Por favor, note que você isso ocultará tudo relacionado ao simulador do produto que for dos tipos indicados.

___

Keywords: