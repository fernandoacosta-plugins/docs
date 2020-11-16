# Modificar o texto padrão de prazo de entrega

Para alterar o texto padrão que diz **Entrega em até 5 dias úteis**, utilize o código abaixo:

```php
add_filter( 'ngettext', 'wc_simulador_frete_forecast_text', 20, 4 );  
function wc_simulador_frete_forecast_text( $translation, $single, $plural, $number ) {  
  // não mexer aqui!  
  if ( $plural !== 'Entrega em %d dias úteis' ) {  
    return $translation;  
  }   // edite seus textos aqui  
  if ( 1 === $number ) {  
    return 'Envio em 1 dia útil';  
  } else {  
    return 'Enviamos em até %d dias úteis';  
  }   return $plural;  
}
```

Repare que há instruções de qual linha você deve começar a mexer.

  

___

Keywords: