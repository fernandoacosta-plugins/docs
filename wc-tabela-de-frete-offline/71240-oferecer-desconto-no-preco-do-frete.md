# Oferecer desconto no preço do frete

Se você quiser oferecer desconto no frete pode fazer isso usando a opção de **Taxa de manuseio** do plugin. Basta preencher com valores negativos.

Se quiser oferecer desconto para estados específicos, basta criar uma área de entrega para essa região, com a mesma tabela, e incluir somente os estados selecionados.

Ou, para mais controle e possibilidades, utilize o código abaixo para oferecer desconto de 27% no custo total do frete. Altere o valor para a porcentagem que preferir.

Utilize para oferecer descontos permanentes ou promoções pontuais.

```php
add_filter( 'wc_table_shipping_cost', 'wcts_shipping_discount', 10, 1 ); function wcts_shipping_discount( $cost ) { $percentage = 27; $discount = ( $percentage / 100 ) * $cost; return $cost - $discount; }
```

  

___

Keywords:desconto frete,taxa frete