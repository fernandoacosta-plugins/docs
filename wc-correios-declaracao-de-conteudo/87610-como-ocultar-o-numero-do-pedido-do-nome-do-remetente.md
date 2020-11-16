# Como ocultar o número do pedido do nome do remetente

Se você configurou o seu site para imprimir etiqueta junto da declaração, ela vem, por padrão, com o ID do pedido junto do endereço do destinatário.

Se quiser ocultar isso, basta adicionar o código a seguir ao seu site ([veja aqui como fazer isso](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)):

```php
add_filter( 'wc_correios_declaration_destination_display_order_id', '__return_false' );  

```

___

Keywords: