# Alterar a posição do Simulador de Frete do WooCommerce

Atualização!

Agora é possível modificar essas opções diretamente no painel do seu site. Basta navegar até WooCommerce -> Configurações -> Produtos -> **Simulador de frete**.

  

  

  

  

  

  

  

  

  

  

  

  

  

  

Por padrão o plugin é exibido no hook ```php
woocommerce_product_meta_start
```, que significa estar após todos os detalhes do produto e junto das informações como SKU, categoria etc.

Você pode facilmente mudar a localização para outro lugar de sua preferência. Para isso utilize o código abaixo:

```php
add_action( 'init', 'mover_simulador_frete', 99 ); function mover_simulador_frete() { remove_action( 'woocommerce_product_meta_start', 'public_wc_shipping_simulator_show_simulator' ); add_action( 'woocommerce_single_product_summary', 'public_wc_shipping_simulator_show_simulator', 55 ); }
```

### Incluindo em outras posições

Se o código não deixou o simulador onde você queria, pode tentar exibi-lo em outros locais, basta trocar o```php
woocommerce_single_product_summary
``` por qualquer outro _hook_ do WooCommerce, como:

-   woocommerce\_after\_add\_to\_cart\_button: após o botão **Comprar**

### Entendendo o código

Essas poucas linhas de código fazem o seguinte:

-   Na linha um, você está adicionando a função personalizada ao carregamento do WordPress
-   Na linha três, você remove o simulador padrão
-   Na linha seguinte o simulador é adicionado novamente, agora no hook ```php
    woocommerce_single_product_summary
    ```, que é basicamente toda a barra lateral direita do produto no WooCommerce. Repare que nessa mesma linha há número ```php
    55
    ```, que é a prioridade de exibição. Você pode ir testando outros valores para alterar a posição. Se colocar ```php
    1
    ```, por exemplo, o simulador será exibido antes mesmo do título do produto.

Não sabe como adicionar essa função ao seu site? [Clique aqui e veja como funciona](https://fernandoacosta.net/blog/docs/adicionar-codigos-php-wordpress/).

  

___

Keywords:simulador de frete,posição,hook,visibilidade