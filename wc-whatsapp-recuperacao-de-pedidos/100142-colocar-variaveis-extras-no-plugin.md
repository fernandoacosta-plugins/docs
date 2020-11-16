# Colocar variáveis extras no plugin

O plugin possui diversas variáveis para permitir que você personalize sua mensagem para cada cliente, melhorando o engajamento e conversões.

**Importante**! Esta é uma personalização avançada e não coberta pelo suporte do plugin (que apenas resolve bugs no plugin). Use com cuidado.

Para incluir novas variáveis, utilize o filtro **wc\_whatsapp\_pending\_orders\_placeholders**. Ele possui dois parâmetros: placeholders (as variáveis originais) e a variável **$order**, que armazena todas as informações do pedido.

No exemplo abaixo, irei incluir o CPF como variável.

```php
add_filter( 'wc_whatsapp_pending_orders_placeholders', 'wc_whatsapp_cpf_variable', 10, 2 ); function wc_whatsapp_cpf_variable( $placeholders, $order ) { $placeholders['{cpf}'] = $order->get_meta( '_billing_cpf' ); return $placeholders; }
```

Agora basta usar a variável **{cpf}** na mensagem. Você pode usar este filtro para incluir qualquer variável necessária na sua loja.

No exemplo abaixo, iremos pegar os códigos de rastreamento com a variável **{tracking\_code}**:

add\_filter( 'wc\_whatsapp\_pending\_orders\_placeholders', 'wc\_whatsapp\_tracking\_code\_variable', 10, 2 );  
function wc\_whatsapp\_tracking\_code\_variable( $placeholders, $order ) {  
  $placeholders\['{tracking\_code}'\] = $order->get\_meta( '\_correios\_tracking\_code' );
  return $placeholders;  
}

  

___

Keywords: