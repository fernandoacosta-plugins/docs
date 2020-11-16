# Alterar a mensagem para CEPs que não sejam cobertos por nenhuma área de entrega

Quando algum CEP não está coberto nas configurações de área de entrega do seu site, a mensagem abaixo é exibida ao cliente:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/c4b361cf-d883-47ad-a5f8-6095121e40cf.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/c4b361cf-d883-47ad-a5f8-6095121e40cf.jpg)

Para mudar isso, basta usar o código abaixo:

```php
add_filter( 'wc_simulador_frete_no_methods_available', 'wcsf_no_methods_message' ); function wcsf_no_methods_message( $message ) { return 'Seu CEP não está em nossa área de atendimento.'; }
```

Basta ajustar o texto como preferir.

Não sabe onde inserir este código? [Veja aqui](https://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php).

Por favor, note que este código dá controle apenas ao simulador de frete, e não ao carrinho ou outras áreas. Essa central de ajuda é para este plugin apenas :)

___

Keywords: