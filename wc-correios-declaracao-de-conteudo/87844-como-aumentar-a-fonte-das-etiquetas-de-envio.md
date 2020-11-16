# Como aumentar a fonte das etiquetas de envio

Se você ajustou o seu site para imprimir a etiqueta junto da declaração e quer aumentar o tamanho da fonte, basta usar o código abaixo.

```php
add_action( 'wc_correios_declaration_head', 'wc_correios_declaration_custom_label_css' );  
function wc_correios_declaration_custom_label_css() {  
  ?>  
  <style type="text/css">  
    .declaration-label .label-content {  
      font-size: 16px !important;  
    }  
  </style>  
  <?php  
}
```

Para mudar o tamanho, basta trocar o 16 pelo número que preferir.

  

___

Keywords: