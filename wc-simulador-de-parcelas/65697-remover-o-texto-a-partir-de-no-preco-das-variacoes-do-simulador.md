# Remover o texto ‘A partir de’ no preço das variações do simulador

O comportamento padrão do simulador de parcelas em produtos variáveis é exibir sempre o menor valor como referência. No caso de haver preços distintos nas variáveis, a exibição será precedida do aviso “A partir de”, como na imagem:  

[![](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/c6456f4a-328e-49c3-95d9-841745ed0abe.png)](https://s3-eu-west-1.amazonaws.com/cdn.supporthero.io/article/2624/c6456f4a-328e-49c3-95d9-841745ed0abe.png)

Você pode querer manipular este texto. Para isso, utilize o filtro ```php
wc_simulador_parcelas_before_variation_price_text
```. No exemplo abaixo, iremos simplesmente ocultar o texto:

```php
add_filter( 'wc_simulador_parcelas_before_variation_price_text', '__return_empty_string' );
```

  

___

Keywords:variação,a partir de,customização