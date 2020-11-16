# Exibir a tabela de parcelamento ANTES do botão comprar

Basta adicionar este código ao seu site:

```php
add_action( 'woocommerce_single_product_summary', function() {  
  echo do_shortcode( '[wcsp_table]' );  
}, 29 );
```

Este código irá exibir a tabela de parcelamento antes do botão comprar no seu site. A tabela pode ser exibida em mais de um lugar. Se você quer evitar que isso aconteça, certifique-se de desabilitar a exibição padrão nas configurações do plugin.

___

Keywords: