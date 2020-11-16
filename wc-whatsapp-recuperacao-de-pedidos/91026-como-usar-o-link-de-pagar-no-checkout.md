# Como usar o link de pagar no checkout​​

Em alguns casos você pode querer exibir ao cliente a URL do checkout se o pedido for via cartão e estiver como pendente.

Por padrão, a URL enviada é a de visualização do pedido.

Basta usar o código abaixo:

```php
add_filter( 'wc_whatsapp_pending_orders_payment_data', 'fa_custom_whatsapp_url', 10, 2 );  
function fa_custom_whatsapp_url( $args, $order ) {  
  if ( $order->has_status( 'pending' ) && $args['payment_url'] === $order->get_view_order_url() ) {  
    $args['payment_url'] = $order->get_checkout_payment_url();  
  }   return $args;  
}
```

  

Não sabe onde inserir esse código? [http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: