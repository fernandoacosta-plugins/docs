# Ocultar o preço original do produto

Por padrão, se você tem um produto que custa R$ 100,00 e pode ser parcelado em até 10x sem juros, você verá algo assim no seu site:

-   R$ 100,00  
    R$ 90,00 no boleto  
    10x de R$ 10,00 sem juros

Você pode querer ocultar o preço original. Para isso, basta adicionar a seguinte linha de código no seu site:

```php
<?php /** * Ocultar preço nas variações */ add_filter( 'wc_simulador_parcelas_display_original_price_variation', '__return_false' ); /** * Ocultar preço em produtos simples */ add_filter( 'wc_simulador_parcelas_display_original_price', '__return_false' );
```

[Ver no Gist](http://gist.github.com/fernandoacosta/edb1de32b87c327f3cf4928f87f3c1a8#file-functions-php).  

Não sabe como adicionar este código ao seu site? [Confira aqui](https://fernandoacosta.net/blog/docs/adicionar-codigos-php-wordpress/)!

  

___

Keywords:preço original,ocultar preço,remover preço