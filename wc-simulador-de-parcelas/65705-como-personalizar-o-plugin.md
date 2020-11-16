# Como personalizar o plugin

O plugin WC Simulador de Parcelas possui uma série de estilos padrão que funcionam na maioria dos temas. No entanto, é possível customizar para deixar a exibição de descontos e parcelas da forma que você quiser.

Veja abaixo as principais classes do plugin para que você possa personalizá-las. Conhecimentos de CSS são necessários.

```php
/* este é o preço do produto no boleto */ .woocommerce .wc-simulador-parcelas-offer .woocommerce-Price-amount { /* afeta todos os locais */ } .woocommerce .products .wc-simulador-parcelas-offer .woocommerce-Price-amount { /* afeta apenas no loop de produtos */ } .woocommerce .summary .wc-simulador-parcelas-offer .woocommerce-Price-amount { /* afeta apenas na página interna do produto */ } /* container do preço no boleto */ /* utilize :before para definir uma imagem personalizada de fundo; */ .woocommerce .entry-summary .wc-simulador-parcelas-offer { } /* texto "no boleto/transferência" */ .woocommerce .wc-simulador-parcelas-detalhes-valor { /* afeta todos os locais */ } .woocommerce .products .wc-simulador-parcelas-detalhes-valor { /* afeta apenas no loop de produtos */ } .woocommerce .summary .wc-simulador-parcelas-detalhes-valor { /* afeta apenas na página interna do produto */ } /* este é o texto sobre quantidade de parcelas "em até x vezes de R$ X,xx" */ /* ainda tem duas classes adicionais */ /* .no-fee e .fee-included */ /* que permitem personalizações diferentes se houver ou não juros */ .woocommerce .wc-simulador-parcelas-parcelamento-info { /* afeta todos os locais */ } .woocommerce .products .wc-simulador-parcelas-parcelamento-info { /* afeta apenas no loop de produtos */ } .woocommerce .summary .wc-simulador-parcelas-parcelamento-info { /* afeta apenas na página interna do produto */ } /* container das informações de parcelamento */ /* utilize :before para definir uma imagem personalizada de fundo; */ .woocommerce .entry-summary .wc-simulador-parcelas-parcelamento-info-container { }
```

[Ver no Gist](http://gist.github.com/fernandoacosta/bd1414550b315e75f0a6cae92665fcb4#file-style-css).

___

Keywords:css,personalização,simulador de parcelas