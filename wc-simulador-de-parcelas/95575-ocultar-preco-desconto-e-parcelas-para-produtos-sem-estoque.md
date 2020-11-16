# Ocultar preço (desconto e parcelas) para produtos sem estoque

Se você quer ocultar o simulador de parcelas e descontos em produtos que estejam sem estoque basta usar o pequeno snippet a seguir:

```php
add_filter( 'wcsp_is_available', 'wcsp_is_available_stock', 10, 2 );  
function wcsp_is_available_stock( $is_available, $product ) {  
  if ( ! $product->is_in_stock() ) {  
    $is_available = false;  
  }   return $is_available;  
}
```

Não sabe onde inserir este código? **[Veja aqui](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)**!

___

Keywords: