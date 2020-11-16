# Ocultar simulador quando o limite de parcelamento for 1x

Por padrão o plugin irá exibir algo como:

_Em até 1x de R$ 55,00_

No entanto, você pode querer remover essa informação nesses casos. Para isso, basta utilizar o código abaixo:

```php
<?php add_filter( 'wcsp_pre_installments_price', 'hide_installments_when_one', 10, 2 ); function hide_installments_when_one( $value, $product ) { $price = $product->get_price(); $min = WC_Simulador_Parcelas_Init::get_min_installment(); return ( $price < $min * 2 ) ? '' : $value; }
```

  

___

Keywords:parcelamento uma vez,parcelamento