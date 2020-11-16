# Como modificar o endereço padrão do remetente

Por padrão o plugin WooCommerce Declaração de Conteúdo para Correios exibe o endereço da loja definido em **WooCommerce -> Configurações**, função introduzida no WooCommerce 3.2.0, que também é a versão mínima necessária para que o plugin funcione corretamente.

Caso você esteja usando uma versão desatualizada – **o que pode causar problemas de segurança** -, você pode usar o código a seguir para que o plugin funcione corretamente.

O mesmo código é util caso você esteja interessado em modificar o endereço definido por padrão nas configurações citadas acima.

[Veja aqui onde adicionar este código](http://ajuda.fernandoacosta.net/article/show/65676-como-adicionar-codigos-php-no-wordpress-precisa-ser-no-functions-php).

```php
add_filter( 'wc_correios_declaration_store_address', 'wc_correios_declaration_custom_address' ); function wc_correios_declaration_custom_address() { return sprintf( '<strong>%s</strong><br /> %s<br /> %s<br /> %s<br /> %s - %s ', 'Nome do remetente', 'Linha 01', 'Linha 02', 'CEP', 'Cidade', 'Estado' ); }
```

  

[Ver no Gist](http://gist.github.com/fernandoacosta/89b5e729765c63c37afb9f9f2b13479e#file-functions-php).

Você só precisa modificar as informações das últimas linhas, Linha 01, Linha 02, Estado, etc.

Dúvidas? Escreva no chat que ajudo o mais breve possível.

  

___

Keywords: