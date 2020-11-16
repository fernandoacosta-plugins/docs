# Alterar a ordem da Aba de parcelamento no WooCommerce

Por padrão o parcelamento irá exibir a aba com prioridade 1, ou seja, ficará logo no começo, antes mesmo da descrição do produto.

Caso queira modificar a ordem, utilize o código abaixo.

```php
add_filter( 'wc_simulador_parcelas_tab_priority', 'custom_wc_simulador_parcelas_tab_priority' ); function custom_wc_simulador_parcelas_tab_priority() { return 50; }
```

[Ver no Gist](http://gist.github.com/fernandoacosta/efeb2984f4f1ec2608609d54757e96b2#file-functions-php).

Você pode alterar o número 50 por qualquer valor. Como 15, por exemplo, para colocar logo após a aba “Descrição.

  

___

Keywords:posição,personalizar simulador