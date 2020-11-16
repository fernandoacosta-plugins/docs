# Utilize um separador personalizado na sua tabela

Por padrão, o plugin utiliza o separador **vírgula** para identificar as colunas de uma tabela. Se sua tabela usa outro formato, o ideal é modificar a formatação para usar vírgula.

Se mesmo assim você preferir trocar o separador para outro valor, como **ponto-e-vírgula**, adicione o código abaixo no seu site:

```php
add_filter( 'wc_table_shipping_delimiter', 'wcts_use_custom_delimiter' ); function wcts_use_custom_delimiter( $delimiter ) { return ';'; }
```

Não sabe onde adicionar este código? [Veja aqui](https://fernandotest.supporthero.io/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php).

A _forma de fazer essa mudança_ pode depender do local onde você está gerando a tabela, então verifique neste programa ou sistema operacional como fazer isso.

Algumas sugestões:

1\. Copiar e colar toda a tabela para dentro do Google Docs. E então exportar novamente como CSV.

2\. [Ver este artigo](https://www.officetooltips.com/office_2016/tips/change_the_semicolon_to_a_comma_or_vice_versa.html) e entender como fazer a mudança no sistema operacional, se aplicável.

___

Keywords: