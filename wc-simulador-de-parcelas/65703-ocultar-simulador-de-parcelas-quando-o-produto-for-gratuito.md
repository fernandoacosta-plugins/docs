# Ocultar simulador de parcelas quando o produto for gratuito

No momento até quando o produto é gratuito o simulador é exibido, o que pode ser um pouco estranho em alguns casos. Com o código abaixo você pode resolver esse problema.

Há duas possibilidades: remover completamente a informação de preço ou simplesmente exibir o valor como **R$ 0,00**. Fica a seu critério. Escolha apenas uma opção para evitar conflitos no seu site, claro.

Exibir o preço apenas como "R$ 0,00"

```php
add_filter( 'woocommerce_product_tabs', 'fa_remove_installments_custom_tab', 9999999 ); function fa_remove_installments_custom_tab( $tabs ) { unset( $tabs['wc-simulador-parcelas'] ); return $tabs; } add_filter( 'woocommerce_get_price_html', 'fa_custom_free_price', 999999, 2 ); function fa_custom_free_price( $price, $product ) { if ( 0 === $product->get_price() || empty( $product->get_price() ) ) { return wc_price( 0 ); } return $price; }
```

Remover o preço completamente:

add\_filter( 'woocommerce\_product\_tabs', 'fa\_remove\_installments\_custom\_tab', 9999999 );
function fa\_remove\_installments\_custom\_tab( $tabs ) {
  unset( $tabs\['wc-simulador-parcelas'\] );
  return $tabs;
}
add\_filter( 'woocommerce\_get\_price\_html', 'fa\_custom\_free\_price', 999999, 2 );
function fa\_custom\_free\_price( $price, $product ) {
  if ( 0 === $product->get\_price() || empty( $product->get\_price() ) ) {
    return;
  }
  return $price;
}

[Ver no Gist](http://gist.github.com/fernandoacosta/eb993a222530e0d00e52fc5e976f25a0#file-remover-o-preco-completamente-php).

Por que não remover nativamente essa função no plugin? Não faz parte do escopo do plugin manipular essas informações, alguns casos pode ser útil. Por isso temos este workaround.

___

Keywords:gratuito,produto gratis,grátis,sem preço