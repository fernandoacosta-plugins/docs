# WCFM: preencher CEP para loja principal

Caso você utilize o marketplace WCFM e ofereça produtos da loja principal, devido a um má prática do plugin, é necessário incluir o código abaixo no seu site:

```php
add_filter( 'wcfmmp_popluate_store_data', 'wcfm_main_shop_data', 10, 2 ); function wcfm_main_shop_data( $settings, $id ) { if ( 1 !== intval( $id ) ) { return $settings; } $settings['address'] = array( 'street_1' => '', 'street_2' => '', 'city' => '', 'zip' => WC()->countries->get_base_postcode(), 'state' => WC()->countries->get_base_state(), 'country' => 'BR', ); return $settings; }
```

Este código vai adicionar o CEP da loja e permitir o cálculo corretamente.

Veja que na terceira linha há o número 1.

Esse é o ID do usuário. Em 99% dos casos será esse mesmo, mas às vezes o ID do usuário administrador é diferente, aí basta modificar neste local.

Não sabe onde incluir este código? Veja: [https://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php](https://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: