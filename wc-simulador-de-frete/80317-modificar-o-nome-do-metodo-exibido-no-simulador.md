# Modificar o nome do método exibido no simulador

O plugin Simulador de Frete possui diversos filtros que permitem adaptar o funcionamento às necessidades da sua loja. Com o filtro _wc\_simulador\_frete\_method\_label_ você pode modificar o texto exibido no método de entrega.

Veja um exemplo. O formato padrão é este:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/8e93503b-8ed3-4fdb-afed-81bbffea2da1.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/8e93503b-8ed3-4fdb-afed-81bbffea2da1.jpg)

O texto diz "Entrega em até x dias úteis" (quando disponível). Se você quer mudar para, por exemplo, "Você receberá em até x dias úteis", pode usar o código abaixo:

```php
add_filter( 'wc_simulador_frete_method_label', 'fa_replace_default_simulator_label' );  
function fa_replace_default_simulator_label( $label ) {  
  return str_replace( 'Entrega em', 'Você recebe em ', $label );  
}
```

O resultado final será este:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/65a3f5e6-e7f2-44e9-9228-9abeff35437f.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/65a3f5e6-e7f2-44e9-9228-9abeff35437f.jpg)

  

IMPORTANTE: customizações de desenvolvimento não fazem parte do suporte oferecido ao plugin.

___

Keywords: