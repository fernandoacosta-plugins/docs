# Por que o PAC não aparece em alguns produtos

Mesmo com PAC ativo no CEP do usuário, durante a simulação o PAC fica oculto em alguns casos. O mesmo pode acontecer com o SEDEX, eventualmente.  

Normalmente isso acontece porque o produto custa menos que R$ 18,00 – mínimo exigido como valor declarado pelos Correios.

Então, na prática, está correto que o PAC não seja exibido. Mas em alguns casos PAC é a única forma que você tem de entregar o produto, mesmo com valor menor.

Para corrigir isso, basta adicionar um pequeno código ao seu site:

```php
add_filter( 'woocommerce_correios_shipping_args', 'wc_correios_simulador_declared_value' ); function wc_correios_simulador_declared_value( $args ) { if ( 18 > $args['nVlValorDeclarado'] ) { $args['nVlValorDeclarado'] = 18; } return $args; }
```

Esse código vai filtrar o valor declarado. Sempre que for menor que R$ 18,00, considera-se R$ 18,00 como valor declarado. Este código também irá aplicar a mesma correção no carrinho, no plugin WooCommerce Correios.

Não sabe como adicionar essa função ao seu site? [Clique aqui e veja como funciona](https://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php).

___

Keywords:valor declarado,pac,pac nao aparece,valor minimo