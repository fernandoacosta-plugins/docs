# Permitir métodos de entrega duplicados (mesmo nome e tabela de origem)

O plugin WC Tabela de Frete Offline tenta exibir aos clientes sempre o melhor resultado e, por isso, evita métodos de entrega duplicados.

Então se você definir, em uma só tabela, o método **Transportadora** duas vezes, somente um será exibido. Causaria confusão ao cliente ter duas opções com o mesmo nome e preço (ou, pior ainda, preços diferentes e mesmo prazo de entrega).

Se você deseja permitir que métodos duplicados fiquem visíveis aos clientes, basta utilizar o código a seguir:

```php
add_filter( 'wc_table_shipping_method_key', 'wcts_custom_method_key', 10, 4 ); function wcts_custom_method_key( $key, $post_id, $method_name, $method_title ) { return uniqid( 'method_' . $key . $post_id ); }
```

[Ver no Gist](http://gist.github.com/fernandoacosta/3f3e00537c1414b611650b63cea2aadb#file-functions-php).

Não sabe como inserir este código? [Veja aqui como fazer](https://fernandoacosta.net/blog/docs/adicionar-codigos-php-wordpress/)!

  

___

Keywords:métodos duplicados,transportadoras