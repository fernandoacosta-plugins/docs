# Ocultar preço original das variações

Se você quer ocultar o preço original das variações, o do "A partir de" e deixar somente o preço nos produtos variáveis individuais, utilize o código abaixo:

```php
add_filter( 'woocommerce_get_price_html', 'hide_original_prices_variable', 20, 2 ); add_filter( 'wcsp_is_available', 'hide_original_prices_variable', 20, 2 ); add_filter( 'wcsp_show_original_price', 'hide_original_prices_variable', 20, 2 ); function hide_original_prices_variable( $show, $product ) { if ( $product->is_type( 'variable' ) && $product->get_variation_price( 'min' ) !== $product->get_variation_price( 'max' ) ) { return ''; } return $show; }
```

  

___

Keywords: