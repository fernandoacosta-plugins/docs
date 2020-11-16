# Personalizar a exibição do simulador

O plugin WooCommerce Simulador de Frete exibe uma tabela com os dados de entrega na página do produto. O plugin possui um estilo bastante básico, já que o objetivo é seguir os padrões do tema que está ativo no momento.

No entanto, em alguns casos o layout fica quebrado:

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/762f6338-684a-4ea6-8d50-1d5aa4b8fc25.png)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/762f6338-684a-4ea6-8d50-1d5aa4b8fc25.png)

Abaixo eu deixo um CSS personalizado para deixar o seu tema com um design mais profissional:

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/20141132-cf9e-4691-a296-413d26caa737.png)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/20141132-cf9e-4691-a296-413d26caa737.png)

Basta pegar o CSS que está abaixo e adicionar ao seu tema. 

Não sabe onde colocar esse CSS? [Clique aqui](https://fernandotest.supporthero.io/article/show/65711-como-adicionar-css-personalizado-ao-meu-tema).

#wc-shipping-simulator { margin-bottom: 30px; margin-top: 30px;  
}  
#wc-shipping-simulator .cep-number { margin-top: 0 !important; height: 40px; width: 45%; float: left; padding: 0 5px !important; line-height: 40px;  
}  
#wc-shipping-simulator h3 { font-size: 16px !important; margin-bottom: 10px;  
}  
#wc-shipping-simulator .button { width: 50%; margin: 0 0 20px 15px; height: 40px; float: left; font-size: 16px; max-width: 120px; text-transform: none; padding: 0 !important; line-height: 40px !important;  
}  
#wc-shipping-simulator .button.loading { background-color: #000;  
}  
#wc-shipping-simulator .table-freight { width: 100%;  
}  
#wc-shipping-simulator .table-freight thead { background: rgba(233, 233, 233, 0.58);  
}  
#wc-shipping-simulator .table-freight th,  
#wc-shipping-simulator .table-freight td { padding: 5px 10px;  
}  
#wc-shipping-simulator .table-freight tbody tr:nth-child(even) { background: rgba(233, 233, 233, 0.58);  
}  
#wc-shipping-simulator form { clear: both;  
}  
#wc-shipping-simulator form:before, #wc-shipping-simulator form:after { display: table; content: " ";  
}  
#wc-shipping-simulator form:after { clear: both;  
}

  

___

Keywords:css,layout,simulador de frete,estilo