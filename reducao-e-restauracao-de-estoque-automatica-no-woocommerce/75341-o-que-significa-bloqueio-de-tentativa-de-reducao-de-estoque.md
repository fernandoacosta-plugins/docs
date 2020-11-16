# O que significa "bloqueio de tentativa de redução de estoque"?

Você já deve ter visto notas do pedido como no exemplo abaixo:

[![](https://s3.eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/c7bcd588-c4a6-4402-a76e-d89bbf031b48.jpg)](https://s3.eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/c7bcd588-c4a6-4402-a76e-d89bbf031b48.jpg)

A mais antiga indica que o estoque foi reduzido imediatamente após a compra. Já a mais recente informa que houve uma tentativa de redução de estoque bloqueada.

Isso quer dizer que o plugin está funcionando corretamente e o estoque foi reduzido apenas uma vez, como tem que ser. Imediatamente após a realização do pedido.

A segunda tentativa, ou mesmo uma terceira ou quarta, não tem um momento certo para acontecer e depende de muitos fatores.

No caso do exemplo, o método de pagamento é cheque, que reduz o estoque assim que o pedido foi criado. Mas como o plugin **Redução e Restauração de estoque para WooCommerce** faz isso antes, essa segunda tentativa é bloqueada.

Em alguns casos, para determinados métodos de pagamento, o WooCommerce irá reduzir o estoque quando o pedido for pago, normalmente no status processando. Só nesse momento então que irá aparecer essa nota de bloqueio.

De qualquer forma, isso é apenas uma referência para saber que o plugin está funcionando corretamente. Se você não quer que essas notas sejam adicionadas aos seus pedidos, basta incluir este pequeno código no seu site:

```php
add_filter( 'wcsrm_log_attempts', '__return_false' );  

```

___

Keywords: