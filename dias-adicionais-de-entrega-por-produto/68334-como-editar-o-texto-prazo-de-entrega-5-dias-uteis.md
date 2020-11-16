# Como editar o texto "Prazo de Entrega: 5 dias úteis"

Na página do produto, você verá algo assim:

[![](https://s3.eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/d97d1ac7-9647-4f18-b9d0-d1ede104202a.jpg)](https://s3.eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/d97d1ac7-9647-4f18-b9d0-d1ede104202a.jpg)

Se você quer modificar este texto, basta usar o código a seguir:

```php
add_filter( 'wc_adpp_product_message', 'custom_wc_adpp_product_message', 10, 2 ); function custom_wc_adpp_product_message( $message, $additional_days ) { $text = 'Envio: em até %s dias úteis após a produção'; return sprintf( '<p class="wc-adpp-info">%s</p>', sprintf( $text, $additional_days ) ); }
```

Você só precisa modificar o texto "**Envio: em até %s dias úteis após a produção**" para o que você preferir.

Repare que ali há um %s que será substituído pelo número definido nas configurações do plugin.  

Não sabe como adicionar este código? Veja no link: [http://ajuda.fernandoacosta.ne...](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

  

___

Keywords: