# Como oferecer desconto em um método de pagamento?

Ao comprar o plugin WooCommerce Simulador de Parcelas e Descontos você pode definir a taxa de juros de acordo com o seu gateway de pagamento, assim como limitar o número de parcelas e o valor mínimo, dentre outras coisas.

Além disso, é possível configurar um desconto para ser exibido no seu site. No boleto, por exemplo.

No entanto, o plugin é apenas um simulador, não irá afetar o checkout. Você precisa, para isso, configurar de outra forma. A forma mais simples, e grátis, é utilizando o plugin Payment Gateway Based Fees and Discounts for WooCommerce.

Com ele você pode adicionar taxas ou definir descontos por tipos de pagamento no WooCommerce.

[Faça download aqui](https://br.wordpress.org/plugins/checkout-fees-for-woocommerce/).

A configuração é bem simples, basta seguir as informações descritas na página do plugin disponível no link acima. Então simplesmente configure o mesmo valor de desconto no simulador e nesse novo plugin.

Lembrando que o desconto será aplicado **no método de pagamento**, então no caso do PagSeguro nativo ou outros plugins que levem para outro ambiente que não seja o da loja não vai funcionar corretamente. Repare que no painel do WooCommerce há apenas uma tela para configurar boleto e parcelamento no PagSeguro, justamente porque não há essa separação. Mas boa parte dos métodos possui a separação entre cartão e boleto, então você não terá problemas.

___

Keywords:desconto,boleto,transferência,método de pagamento