# Remover a exibição do prazo da página do produto

Assim que você instala este plugin, uma mensagem começa a ser exibida na página do produto:

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/852aaebd-ade4-4d31-9481-5f76be79176e.jpg)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/852aaebd-ade4-4d31-9481-5f76be79176e.jpg)

O texto padrão é "Prazo de entrega: imediato". Se um número de dias é definido, isso também é exibido. No exemplo acima, o prazo são 100 dias.

Se você quer editar este texto, veja este artigo: [Como editar o texto "Prazo de entrega: 10 dias úteis"](http://ajuda.fernandoacosta.net/article/show/68334-como-editar-o-texto-prazo-de-entrega-5-dias-uteis). 

Mas se você quer removê-lo por completo, você está no local certo.

Simplesmente adicione o código abaixo ao seu site:

```php
remove_action( 'woocommerce_single_product_summary', 'wc_adpp_product_page_info', 35 );
```

Não sabe como adicionar códigos? [Veja aqui](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)!

Este será o resultado final:

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/4f31f740-87e5-4ed4-a1a2-9b76ae5c6905.jpg)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/4f31f740-87e5-4ed4-a1a2-9b76ae5c6905.jpg)

Pronto!

___

Keywords: