# Como ocultar o simulador em determinados tipos de produto

Por padrão, o simulador será exibido em todos os produtos exceto se:

-   Produto não precisa de entrega (digital, por exemplo)
-   Produto está fora de estoque
-   Produto é do tipo Grupo de Produtos ou Externo (link para outro site)

Então se você instalar plugins que adicionem métodos personalizados o plugin também funcionará. No entanto, alguns tipos de produto podem ter regras específicas ou funcionar com outros propósitos. Por isso você pode não precisar do simulador de frete neles.

Para incluir o tipo de produto customizado nas restrições basta usar o código abaixo:

```php
add_filter( 'wc_shipping_simulator_not_allowed_product_types', 'hide_wc_simulador_frete_types' );  
function hide_wc_simulador_frete_types( $product_types ) {  
  $product_types[] = 'simple';   return $product_types;  
}
```

No exemplo acima ocultamos o simulador para os produtos simples do WooCommerce. Basta mudar o nome **simple** pelo nome do seu tipo de produto personalizado.

___

Keywords: