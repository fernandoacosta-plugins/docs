# Como incluir lembretes para pagamento via Transferência ou Cheque

O plugin **Lembrete de boleto para WooCommerce** envia, claro, lembrete de boletos.

Mas se você vende via transferência bancária ou cheque (métodos nativos do WooCommerce) pode querer enviar esses mesmos lembretes.

Para isso, basta incluir o código abaixo no seu site:

```php
add_filter( 'wc_boleto_reminder_get_payment_data', 'boleto_reminder_bacs_cheque', 20, 2 ); function boleto_reminder_bacs_cheque( $args, $order ) { if ( in_array( $order->get_payment_method(), array( 'bacs', 'cheque' ) ) ) { $args = array( 'method_name' => $order->get_payment_method_title(), 'payment_url' => $order->get_view_order_url(), ); } return $args; }
```

Por padrão, esse código está enviando para a página de **ver pedido**. Se você quiser, pode mudar a URL para um link personalizado onde você mostra todos os detalhes para onde fazer a transferência e qual e-mail enviar o comprovante, por exemplo.

O resultado final da linha em questão ficaria assim:

'method\_name' => 'http://meusite.com/como-fazer-transferencia',

Onde incluir esse código? [http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: