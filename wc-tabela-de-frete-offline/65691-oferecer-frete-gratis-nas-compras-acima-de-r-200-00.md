# Oferecer frete grátis nas compras acima de R$ 200,00

Nas versões mais recentes do plugin você pode definir uma coluna da tabela a ser importada para informar o valor mínimo de compra para que o cliente ganhe frete grátis. Basta configurar como no exemplo:

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/f395e8eb-4e41-4b49-89ff-eb8f00e99347.png)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/f395e8eb-4e41-4b49-89ff-eb8f00e99347.png)

Se deixar o valor padrão que na imagem é “Não oferecer frete grátis”, sempre será utilizado o preço da coluna “Custo”.

Você adiciona uma coluna extra e informa o valor mínimo para cada faixa de CEP e peso.

Se você quer que determinada faixa **sempre** tenha frete grátis coloque valor 0 (zero).

Caso uma faixa **não tenha frete grátis**, deixe em branco.

___

## Via código

A opção acima facilita em muitos casos. Mas se você quer criar regras mais avançadas e **sabe personalizar**, pode fazer via código. Sendo assim, você pode querer definir isso via código, como explicado abaixo.

No código a seguir, utilizaremos o filtro ```php
wc_table_shipping_cost
``` para oferecer frete grátis em compras acima de R$ 200,00. Utilizando este filtro você consegue fazer qualquer tipo de mudanças que precise no custo do frete definido na tabela.

```php
add_filter( 'wc_table_shipping_cost', 'wcts_free_shipping', 10, 3 ); function wcts_free_shipping( $cost, $rate, $package ) { if ( 200 <= $package['contents_cost'] ) { $cost = 0; } return $cost; }
```

Isso vai aplicar frete grátis em todos os métodos offline acima de R$ 200. Se quiser aplicar a uma tabela específica, da transportadora X ou PAC, por exemplo, utilize o código abaixo:

add\_filter( 'wc\_table\_shipping\_cost', 'wcts\_free\_shipping', 10, 3 );
function wcts\_free\_shipping( $cost, $rate, $package ) {
  $id = 9999;
  if ( 200 <= $package\['contents\_cost'\] && $id === $rate\['id'\] ) {
    $cost = 0;
  }
  return $cost;
}

Isso vai dar frete grátis acima de R$ 200 apenas o método de **ID 9999**. Substitua o 9999 pelo seu ID e tudo está pronto. Para encontrar o ID, clique para editar o método de entrega offline e veja a URL, será algo assim:

.../wp-admin/admin.php?page=wc-settings&tab=shipping&instance\_id=16

Nesse caso o ID é 16.  

Se quiser oferecer frete grátis para estados específicos, utilize o código abaixo:

add\_filter( 'wc\_table\_shipping\_cost', 'wcts\_free\_shipping', 10, 3 );
function wcts\_free\_shipping( $cost, $rate, $package ) {
  $id     = 9999;
  $states = array( 'SP', 'RJ' );
  if ( 200 <= $package\['contents\_cost'\] && $id === $rate\['id'\] && in\_array( $package\['destination'\]\['state'\], $states ) ) {
    $cost = 0;
  }
  
  return $cost;
}

Veja a parte 

  $states = array( 'SP', 'RJ' );

Basta incluir os novos estados separados por vírgula usando o mesmo padrão.

Essa é uma configuração básica. Mais detalhes e opções avançadas requerem um pouco mais de programação.

**ATENÇÃO: em hipótese alguma cole dois desses códigos no seu site**. Como eles possuem o mesmo nome de função, seu site irá ficar fora do ar. Escolha um e ajuste como quiser.  

**Importante**! Note que o WooCommerce não exibe o texto frete grátis por padrão, apenas oculta o preço completamente para métodos gratuitos - isso não é configuração do plugin, mas sim comportamento da plataforma. Você pode modificar isso com este tutorial: [https://fernandoacosta.net/blo...](https://fernandoacosta.net/blog/2018/10/24/exibir-o-texto-frete-gratis-nos-metodos-de-envio-do-woocommerce/)

___

Keywords:frete grátis,customização,frete offline,correios