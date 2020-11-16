# Como alterar o título da calculadora de frete

## Atualização!

Agora é possível fazer isso diretamente pelo seu painel. Basta navegar até WooCommerce -> Configurações -> Produtos -> **Simulador de frete**.

O título padrão é “Calcule o prazo e valor do frete deste produto”. Você pode modificá-lo como preferir, basta adicionar o código abaixo ao seu site:

```php
add_filter( 'wc_shipping_simulator_calculator_title', 'wcs_calculator_title' );  
function wcs_calculator_title() {  
  return 'Novo título';  
}
```

Não esqueça de mudar onde diz **Novo título** pelo texto que você quer exibir.

Onde adicionar este código? [Veja aqui](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php).

___

Keywords:frete,titulo do simulador,simulador de frete,calculadora