# Como mudar a ordem da exibição do prazo adicional

Se você quer mudar a ordem que o prazo é exibido, basta usar o código abaixo.

```php
remove_action( 'woocommerce_single_product_summary', 'wc_adpp_product_page_info', 35 ); add_action( 'woocommerce_single_product_summary', 'wc_adpp_product_page_info', 100 );
```

Na segunda linha há o número 100, que é o novo local de exibição. Basta mudar para o número que melhor se adapte ao seu tema.

___

Keywords: