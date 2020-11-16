# Integração com o tema Electro

O tema electro possui dois modelos de layout Padrão e extendido. No modelo Extendido ele uma outros filtros que não o padrão do WooCommerce, por isso é necessário uma pequena customização para que suas configurações funcionem como esperado.

Primeiro, certifique-se de ter a versão mais recente instalada.

Depois, adicione o código a seguir ao seu site:

```php
remove_action( 'woocommerce_single_product_summary', array( 'WCSP_Apply_Rules', 'clear_product_function' ), 9999 );  
add_action( 'woocommerce_after_single_product_summary', array( 'WCSP_Apply_Rules', 'clear_product_function' ), 1 );
```

Não sabe onde incluir este código? [Veja aqui](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)! 

Se não quiser mais usar o modelo Extendido, não esqueça de remover este código :)

Por que esse ajuste não está diretamente no plugin?

É possível identificar o tema e as configurações através do plugin, mas isso deixaria ele mais pesado sem motivos, por isso eu sempre opto por códigos rápidos como esse.

___

Keywords: