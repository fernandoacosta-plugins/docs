# Como modificar o nome do remetente

O nome padrão do remetente é o nome configurado da sua loja.

Para modificar isso, pode fazer com este código:

```php
add_filter( 'wc_correios_declaration_store_name', 'wccd_custom_store_name' );  
function wccd_custom_store_name() {  
  return 'Novo remetente';  
}
```

  

___

Keywords: