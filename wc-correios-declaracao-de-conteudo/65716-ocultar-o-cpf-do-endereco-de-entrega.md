# Ocultar o CPF do endereço de entrega

Desde a versão 1.3 o plugin exibe o CPF do destinatário, quando disponível. Se quiser removê-lo, você pode adicionar esta linha de código ao seu ```php
functions.php
```:

```php
add_filter( 'wc_correios_declaration_show_cpf', '__return_false' );
```

___

Keywords:cpf,ocultar cpf,destinatário