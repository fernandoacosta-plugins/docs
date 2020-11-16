# Salvar dados adicionais da tabela de frete nos detalhes do pedido

NOTA: esta é uma seção avançada e não é possível oferecer suporte a customizações. Tenha certeza de que está familiarizado antes de fazer mudanças.

Se você possui várias colunas na sua tabela com informações que não são propriamente relevantes ao cálculo mas que podem ser úteis futuramente, você pode usar o filtro wc\_table\_shipping\_rate para salvar esses dados como metadata.

Este filtro possui 3 argumentos:

-   $args = os detalhes básicos do método de envio
-   $rate = todos os detalhes que vieram da sua tabela
-   $method = todos os detalhes e funções do método de envio

Um exemplo é se você não exibe ao cliente o nome da transportadora selecionada mas gostaria de salvá-lo na tela de pedidos:

Basta usar o código abaixo:

```php
add_filter( 'wc_table_shipping_rate', 'wcts_save_shipping_company_name', 10, 3 );  
function wcts_save_shipping_company_name( $args, $rate, $method ) {  
$row = $rate['row'];  
$map = $rate['map'];  
$args['meta_data']['Transportadora Escolhida'] = isset( $row[ $map['label'] ] ) ? $row[ $map['label'] ] : 'Não foi possível identificar a transportadora'; return $args;  
}
```

  

O resultado final será assim:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/e28cfb72-c572-4224-9b57-5abdbdf77e59.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/e28cfb72-c572-4224-9b57-5abdbdf77e59.jpg)

  

___

Keywords: