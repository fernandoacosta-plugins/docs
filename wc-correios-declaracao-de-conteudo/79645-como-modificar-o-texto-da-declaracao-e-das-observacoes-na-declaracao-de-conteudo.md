# Como modificar o texto da declaração e das observações na Declaração de conteúdo

Os textos exibidos no plugin são o padrão definidos pelos Correios, mas se por algum motivo você deseja modificá-los pode usar os códigos a seguir.

## Declaração

```php
add_filter( 'wc_correios_declaration_text', 'custom_wc_correios_declaration_text' );  
function custom_wc_correios_declaration_text() {  
  return 'Minha declaração personalizada';  
}
```

Resultado:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/b4e9adba-78c3-44e5-bce2-eb07e0220363.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/b4e9adba-78c3-44e5-bce2-eb07e0220363.jpg)

## Observações

add\_filter( 'wc\_correios\_declaration\_observations', 'custom\_wc\_correios\_declaration\_observations' );  
function custom\_wc\_correios\_declaration\_observations() {  
  return 'Minhas observações personalizadas';  
}

Resultado:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/96aed19c-e833-4aad-ae51-07679fdefe13.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/96aed19c-e833-4aad-ae51-07679fdefe13.jpg)

  

Inclua os códigos personalizados no seu site: [http://ajuda.fernandoacosta.ne...](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: