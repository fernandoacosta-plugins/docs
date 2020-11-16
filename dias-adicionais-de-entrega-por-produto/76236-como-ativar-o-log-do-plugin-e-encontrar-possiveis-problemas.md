# Como ativar o log do plugin e encontrar possíveis problemas

Se você quer confirmar se o plugin está funcionando corretamente, pode ativar o log simplesmente incluindo a linha a seguir no seu site:

```php
add_filter( 'wc_additional_days_per_product_debug', '__return_true' );
```

Veja aqui como adicionar códigos PHP: [http://ajuda.fernandoacosta.ne...](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

Feito isso, simule novamente o frete. Um arquivo será gerado em WooCommerce -> Status -> Logs -> wc-additional-days...

Você pode ver todo o processo aí e também identificar alguma falha. Ao solicitar suporte, cole o log do plugin em pastebin.com e me envie o link para análise.  

___

Keywords: