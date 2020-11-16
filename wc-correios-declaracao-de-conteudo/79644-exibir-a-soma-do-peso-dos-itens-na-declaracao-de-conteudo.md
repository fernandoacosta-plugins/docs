# Exibir a soma do peso dos itens na declaração de conteúdo

Para exibir uma linha com o peso total dos produtos de uma declaração basta utilizar o código a seguir:

```php
add_action( 'wc_correios_declaration_after_items', 'wc_correios_declaration_add_total_weight' ); function wc_correios_declaration_add_total_weight( $order ) { $weight = 0; foreach ( $order->get_items() as $key => $item ) { $product = $item->get_product(); $weight += method_exists( $product, 'get_weight' ) ? ( $product->get_weight() * $item->get_quantity() ) : 0; } ?> <div class="line-item footer"> <div class="order-total"> Peso total </div> <div class="order-price" contenteditable="true"> <?php echo $weight . ' ' . get_option( 'woocommerce_weight_unit' ); ?> </div> </div> <?php }
```

O resultado será este:

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/e679079c-b108-4a73-a90a-f983f2214849.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/e679079c-b108-4a73-a90a-f983f2214849.jpg)

  

___

Keywords: