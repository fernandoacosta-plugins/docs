# WC Frete Offline: actions e filters

O plugin possui uma série de filtros que permitem modificar o funcionamento padrão e torná-lo ainda mais poderoso. Se você é um desenvolvedor ou mesmo se arrisca com código, pode ler e interpretar muitas das funções disponíveis.

Irei listar aqui alguns _actions_ e _filters_ disponíveis no plugin principal que permitem criar novos recursos.

### Filtro: wc\_table\_shipping\_weight

Com este filtro é possível manipular o peso entregue no carrinho. Dessa forma, você pode, por exemplo, cadastrar uma tabela com peso máximo de 30 kg. Se os produtos pesarem mais que isso, nenhum método de envio será exibido. Você pode criar uma regra para que se o peso for maior que 30, calcular como se fosse 30.

Exemplo:

```php
add_filter( 'wc_table_shipping_weight', 'wcts_custom_weight', 10, 4 ); function wcts_custom_weight( $cart_weight, $package, $extra_weight, $weight_unit ) { if ( $cart_weight > 30 ) { $cart_weight = 30; } return $cart_weight; }
```

Pronto. Assim você evita que o peso dos produtos faça com que os métodos fiquem indisponíveis. Isso pode acarretar em pequenos prejuízos mas garante a venda. Há outros parâmetros na função que auxiliam a criar uma função ainda mais complexa e poderosa.

### Filtro: wc\_table\_shipping\_cost

Com este filtro você pode manipular o custo total do envio. Com isso você, por exemplo, combinar com o filtro _wc\_table\_shipping\_weight_ e cobrar um valor extra sempre que o pedido tiver mais que 30 kilos ou qualquer outro peso.

add\_filter( 'wc\_table\_shipping\_cost', 'wcts\_custom\_cost', 10, 4 );
function wcts\_custom\_cost( $cost, $rate, $package, $method ) {
  // funções personalizadas aqui
  return $cost;
}

**NOTA**: esta é uma seção técnica apenas para referência, não há suporte para criação de funções adicionais ao plugin.

___

Keywords: