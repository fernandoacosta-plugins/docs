# Adicionar botão "Não sei meu CEP" abaixo da calculadora de frete do WooCommerce

Embora isso não faça parte do plugin, você pode querer exibir o botão para o cliente encontrar o CEP dele no site dos Correios.

Para fazer isso, adicione o código abaixo ao functions.php seu site:

```php
add_action( 'woocommerce_after_shipping_calculator', 'find_my_postcode_link' ); function find_my_postcode_link() { echo '<small class="find-postcode-link"><a href="http://www.buscacep.correios.com.br/sistemas/buscacep/" target="_blank">Não sei meu CEP</a></small>'; }
```

Para personalizar o botão, há a classe .find-postcode-link, mas para isso você precisará de conhecimentos de CSS.

Veja aqui onde adicionar este código: [http://ajuda.fernandoacosta.ne...](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: