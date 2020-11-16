# Código de rastreio para adicionar ao pedido

A Jadlog possui 3 formas de rastrear um pedido:

-   Shippment ID (código de rastreio)
-   CTE
-   Nota fiscal

O plugin utiliza a primeira opção. Sendo assim, para que as notificações de rastreio e a atualização após a entrega funcionem você deve usar esse código de rastreio.

No entanto, se por algum motivo você prefere outra opção, pode utilizar algum dos códigos abaixo conforme sua necessidade.

Caso queira informar **em todos os pedidos o CTE** do envio:

```php
add_filter( 'wc_jadlog_tracking_method', 'wc_jadlog_cte_tracking_method' );  
function wc_jadlog_cte_tracking_method() {  
  return 'cte';  
}
```

Caso queira utilizar o número da Nota fiscal:

add\_filter( 'wc\_jadlog\_tracking\_method', 'wc\_jadlog\_nfe\_tracking\_method' );  
function wc\_jadlog\_nfe\_tracking\_method() {  
  return 'nf';  
}

Não sabe como adicionar esse código? [https://ajuda.fernandoacosta.n...](https://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: