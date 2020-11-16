# Mudar local de exibição do preço parcelado

Na configuração básica, o preço do parcelado aparece **antes** do preço com desconto. Caso queira mudar essa regra, basta utilizar o pequeno código que está a seguir. Isso irá mover o preço parcelado para **depois** do preço com desconto.  

```php
/** * Página do produto * exibir o valor parcelado APÓS o valor com desconto */ add_filter( 'wcsp_card_price_before_ticket_main_price', '__return_false' ); add_filter( 'wcsp_card_price_after_ticket_main_price', '__return_true' ); /** * Listagem de produtos * exibir o valor parcelado APÓS o valor com desconto */ add_filter( 'wcsp_card_price_before_ticket_loop', '__return_false' ); add_filter( 'wcsp_card_price_after_ticket_loop', '__return_true' );
```

Repare que, se quiser, você pode mudar o preço só na página do produto ou apenas na listagem geral.  

Não sabe como adicionar este código ao seu site? [Confira aqui](https://fernandoacosta.net/blog/docs/adicionar-codigos-php-wordpress/)!

___

Keywords:parcelamento,exibição do preço