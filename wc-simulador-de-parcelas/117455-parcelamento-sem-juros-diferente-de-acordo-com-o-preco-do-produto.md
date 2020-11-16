# Parcelamento sem juros diferente de acordo com o preço do produto

Em certos casos você pode precisar que certos produtos tenham um número diferente de parcelas sem juros.

Isso é especialmente útil se você oferece taxas diferentes a partir de um certo valor.

O código abaixo vai configurar 3 vezes sem juros para produtos acima de R$ 350,00.  

```php
add_filter( 'wcsp_max_installments_no_fee', 'wcsp_no_fee_certain_products', 10, 2 ); function wcsp_no_fee_certain_products( $default, $product ) { if ( $product && $product->get_price() >= 350 ) { return 3; } return $default; }
```

No exemplo acima, basta trocar o número 350 pelo valor mínimo do produto e o 3 pelo número de parcelas sem juros.

___

Keywords: