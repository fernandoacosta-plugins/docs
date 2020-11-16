# Ajustar a ordem dos preços no site

Por padrão, a ordem de exibição é a seguinte:

1.  Preço padrão do WooCommerce
2.  Preço parcelado
3.  Preço à vista/boleto

Com o código a seguir você muda a ordem para:

1.  Preço à vista
2.  Preço do WooCommerce
3.  Preço parcelado

Este código irá fazer a mudança na listagem:

```php
add_filter( 'wcsp_show_original_price', '__return_false', 100 ); add_filter( 'wcsp_card_price_before_ticket_loop', '__return_false', 100 ); add_filter( 'wcsp_card_price_after_ticket_loop', '__return_true', 100 ); add_filter( 'wcsp_original_with_credit_card', '__return_true', 100 );
```

Este código irá fazer a mudança dentro do produto:

add\_filter( 'wcsp\_show\_original\_price', '\_\_return\_false', 100 );  
add\_filter( 'wcsp\_card\_price\_before\_ticket\_main\_price', '\_\_return\_false', 100 );  
add\_filter( 'wcsp\_card\_price\_after\_ticket\_main\_price', '\_\_return\_true', 100 );  
add\_filter( 'wcsp\_original\_with\_credit\_card', '\_\_return\_true', 100 );  

Se você quer remover completamente o preço do WooCommerce, basta remover a última linha de cada código.

Não sabe onde inserir este código? [http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

  

___

Keywords: