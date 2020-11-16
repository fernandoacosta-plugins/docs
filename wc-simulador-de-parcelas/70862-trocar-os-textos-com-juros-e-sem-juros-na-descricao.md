# Trocar os textos "com juros" e "sem juros" na descrição

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/558be822-2cf7-48b9-b0b9-1704c9b6691a.jpg)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/558be822-2cf7-48b9-b0b9-1704c9b6691a.jpg)

Na imagem acima você vê a exibição padrão do plugin WC Simulador de Parcelas.

Após as parcelas é informado o texto com ou sem juros dependendo da situação. Se você quer modificá-lo pode usar o código abaixo como exemplo.

```php
add_filter( 'wcsp_fee_label', 'custom_wcsp_fee_label', 10, 2 );  
function custom_wcsp_fee_label( $text, $interest_fee ) {  
  if ( $interest_fee ) {  
    $text =  'c/ juros';  
  } else {  
    $text =  's/ juros';  
  }   return $text;  
}
```

No código mudamos os textos para "c/ juros" e "s/ juros", mas você pode editar para os textos que quiser. 

Se não sabe como adicionar este código veja como aqui na documentação.

___

Keywords: