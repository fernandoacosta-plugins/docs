# Ocultar o preço do boleto em determinados produtos

Antes de prosseguir, é importante saber que o plugin é apenas um simulador, então qualquer regra que você aplicar nele não terá efeito no checkout, somente visualmente. Então as regras devem ser aplicadas de outras formas nos seus métodos de pagamento (usando plugins, por exemplo).

O filtro para ocultar o preço por boleto é: 

```php
wcsp_ticket_visibilty
```

No exemplo abaixo mostro como ocultar o preço por boleto se o produto já estiver em oferta.

add\_filter( 'wcsp\_ticket\_visibilty', 'hide\_discount\_price\_from\_offers', 20, 2 );  
function hide\_discount\_price\_from\_offers( $visibility, $product = false ) {  
  if ( $product && $product->is\_on\_sale() ) {  
    return 'none';  
  }
  return $visibility;  
}

Você pode adaptar o código de acordo com suas necessidades.

___

Keywords: