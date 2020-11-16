# Integração do Frete Offline com ERP

Se você pretende integrar o plugin de Frete Offline para WooCommerce com algum ERP, na maior parte dos casos é necessário informar o ID do método na integração.

Dessa forma o seu ERP é capaz de identificar qual método de envio foi selecionado pelo cliente no momento da compra.

Para os métodos criados com a tabela de frete offline, o ID será algo como ```php
wcts_21
```

Onde ```php
wcts_
``` é um prefixo padrão e ```php
21
``` é o ID da instância do método no WooCommerce.

## Identificando o ID da instância

Nas áreas de entrega do WooCommerce você verá os métodos criados. O primeiro passo é clicar em Editar no método que você quer identificar o ID.

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/9f67906e-a386-4764-a443-cde9348c7ff4.jpg)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/9f67906e-a386-4764-a443-cde9348c7ff4.jpg)

A URL será parecida com essa: ```php
http://url-do-meu-site/wp-admin/admin.php?page=wc-settings&tab=shipping&instance_id=64
```

Repare que há, ali, um trecho **instance\_id=64**. Então, nesse caso, o ID é **64.**

O valor final que você deverá informar no ERP é ```php
wcts_64
```

Em alguns casos, como no ERP Bling, você precisará manipular o ID do método, já que ele utiliza este campo, que por padrão é **wc\_table\_shipping**, independente se você usa PAC, SEDEX ou qualquer outra transportadora.

Para isso, adicione o código a seguir ao seu site:

```php
add_filter( 'woocommerce_shipping_rate_method_id', 'custom_rate_method_id', 80, 2 ); function custom_rate_method_id( $rate_id, $rate ) { if ( 'wc_table_shipping' === $rate_id ) { $rate_id = 'wcts_' . $rate->get_instance_id(); } return $rate_id; }
```

Pronto. Agora você pode usar os mesmos IDs mencionados acima (wcts\_123...).

Não sabe como adicionar códigos ao seu site? Veja o artigo [http://ajuda.fernandoacosta.ne...](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php)

Se você usa Tiny, o aliás não será apenas wcts\_64, mas sim wcts\_64:64 (repetind o ID).

___

Keywords:frete com tabela,tabela de frete,correios offline