# Como personalizar o texto exibido após o preço com desconto

Se você configura 10% de desconto para pagamentos à vista, a exibição do seu site ficará mais ou menos assim:

R$ 100,00 ou  
R$ 90,00 _no boleto_

Se você definiu este desconto para transferência ou outro método, pode diretamente no painel do plugin em WooCommerce -> Configurações -> Produtos -> Simulador de Parcelas definir o texto customizado.

No entanto, se você quer algo mais avançado e que permita códigos HTML para uma customização mais profunda, pode utilizar os filtros disponibilizados dentro do código do plugin.

Nesta caso específico o filtro é ```php
wcsp_text_after_price
```. Veja um exemplo:

```php
add_filter( 'wcsp_text_after_price', 'custom_text_after_price' );  
function custom_text_after_price( $text ) {  
  return 'Example';  
}
```

No lugar de **Example** você pode customizar para qualquer texto que for necessário, incluindo códigos HTML.

___

Keywords:personalizar,html,avançado,filtros,actions