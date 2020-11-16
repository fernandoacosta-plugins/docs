# Exibir boleto parcelado apenas para certos tipos de usuário

Se você quer exibir a opção de boleto parcelado por um tipo específico de usuário, pode usar o código a seguir:

```php
add_action( 'woocommerce_available_payment_gateways', 'wc_hide_boleto_parcelado' );  
function wc_hide_boleto_parcelado( $gateways ) {  
  $role = 'vendor';  
  if ( isset( $gateways['wc_ticket_installments'] ) && ! in_array( $role, wp_get_current_user()->roles ) ) {  
    unset( $gateways['wc_ticket_installments'] );  
  }   return $gateways;  
}
```

Ele vai exibir o boleto parcelado apenas para usuários do tipo **vendor**. Mude essa palavra pelo nome da role do usuário no seu site.

Não sabe onde incluir este código? [Veja aqui](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)! 

  

___

Keywords: