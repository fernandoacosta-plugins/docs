# Como trocar o texto do botão “Calcular” no simulador

## Atualização!

Agora é possível fazer isso diretamente pelo seu painel. Basta navegar até WooCommerce -> Configurações -> Produtos -> **Simulador de frete**.

  

Muito simples! Basta utilizar o código abaixo. Nele, o texto exibido será “Calcular Frete” e você pode -modificar como for melhor no seu caso.

```php
add_filter( 'wc_shipping_simulator_button_text', 'fa_wc_simulador_frete_botao' ); function fa_wc_simulador_frete_botao() { return 'Calcular Frete'; }
```

Não sabe como adicionar este código ao seu site? [Confira aqui](https://fernandoacosta.net/blog/docs/adicionar-codigos-php-wordpress/)!

  

___

Keywords:​Botões,texto do botão,personalizar,texto