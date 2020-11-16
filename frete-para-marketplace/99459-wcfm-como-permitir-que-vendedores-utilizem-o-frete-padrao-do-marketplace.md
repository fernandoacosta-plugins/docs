# WCFM - Como permitir que vendedores utilizem o frete padrão do marketplace

Por padrão, o plugin desabilita as opções de frete nativas de cada marketplace porque **elas não são compatíveis com os métodos nacionais**. Dessa forma você pode configurar PAC e SEDEX, por exemplo, para todos os vendedores.

Se por algum motivo você quer permitir que os vendedores utilizem a opção de taxas fixas, basta incluir o código abaixo no seu site:

```php
add_filter( 'wc_split_shipping_disable_wcfm_shipping', '__return_false', 200 );
```

Isso é válido apenas para o marketplace WCFM.

Onde incluir este código? [http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

___

Keywords: