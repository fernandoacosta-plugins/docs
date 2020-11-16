# Como incluir variáveis personalizadas no lembrete de boleto

**Importante**. Este é um artigo de nível técnico. Personalizações não são cobertas pelo suporte.

O filtro wc\_boleto\_reminder\_placeholders permite que você cadastre variáveis extras à lista padrão do plugin. O filtro possui duas variáveis:

-   $vars: armazena a lista personalizada
-   $order: detalhes do pedido atual

O exemplo abaixo inclui a variável {endereco}:

```php
add_filter( 'wc_boleto_reminder_placeholders', 'wc_boleto_reminder_custom_vars', 10, 2 );  
function wc_boleto_reminder_custom_vars( $vars, $order ) {  
  $vars['{endereco}'] = $order->get_billing_address_1();   return $vars;  
}  

```

___

Keywords: