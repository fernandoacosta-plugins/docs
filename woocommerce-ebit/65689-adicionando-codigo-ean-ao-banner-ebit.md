# Adicionando código EAN ao banner Ebit

Por padrão, o plugin não conta com o código EAN no banner, mas há essa possibilidade. Este atributo não está disponível pois nem todas as lojas o cadastram, e também não é um padrão do WooCommerce.

Mas o plugin conta com filtros que você pode modificar este comportamento. O código abaixo considera que o campo personalizado ```php
gtin-ean-pn
``` como o código EAN do produto.

No segundo arquivo o exemplo mostra o EAN como sendo o SKU do produto.

```php
add_filter( 'wc_ebit_eanCode', 'wc_ebit_custom_eancode', 10, 3 ); function wc_ebit_custom_eancode( $eancode, $product, $item ) { $product_id = $item->get_product_id(); if ( $custom_eancode = get_post_meta( $product_id, 'gtin-ean-pn', true ) ) { $eancode = $custom_eancode; } return $eancode; }
```

  

add\_filter( 'wc\_ebit\_eanCode', 'wc\_ebit\_custom\_eancode', 10, 3 );
function wc\_ebit\_custom\_eancode( $eancode, $product, $item ) {
  $product\_id = $item->get\_product\_id();
  if ( $custom\_eancode = $product->get\_sku() ) {
    $eancode = $custom\_eancode;
  }
  return $eancode;
}

[Ver no Gist](http://gist.github.com/fernandoacosta/f4be6cc194e4ed8370e832e35a3cc668#file-functions-sku-php).

Se você usa outro nome de campo neste atributo, basta modificá-lo na linha 5 do primeiro arquivo.

  

___

Keywords:ean,código ean,ebit,integração ebit