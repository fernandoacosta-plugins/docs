# Exibir mensagem junto da calculadora do carrinho

Para exibir um aviso de que o prazo de fabricação do produto já está somado ao prazo de envio, adicione o código abaixo ao seu site:

```php
add_action( 'woocommerce_after_shipping_calculator', 'wcadpp_display_shipping_info' );  
function wcadpp_display_shipping_info() {  
  echo '<div class="woocommerce-message" role="alert">O prazo de entrega inclui o tempo de produção do produto</div>';  
}
```

  

  

___

Keywords: