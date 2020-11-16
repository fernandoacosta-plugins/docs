# Trocar o status que o lembrete de review é enviado

Por padrão, o plugin irá enviar o lembrete apenas quando o pedido for marcado como concluído.

Se quiser mudar este comportamento, você pode usar o código abaixo:

```php
add_filter( 'wc_advanced_reviews_reminder_status', 'custom_review_reminder_status' );  
function custom_review_reminder_status( $status ) {  
  return 'processing';  
}
```

  

___

Keywords: