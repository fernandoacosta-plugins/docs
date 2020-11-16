# Como configurar os formulários no Mautic

A configuração do plugin acontece em duas partes: no Mautic e no Elementor PRO.

## Mautic

No Mautic, vá até Componentes -> Formulários e crie um novo formulário.

O plugin funcionará com qualquer formulário, independente ou de campanha.

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/c356ebbb-e62e-4794-9a4e-279617a79c25.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/c356ebbb-e62e-4794-9a4e-279617a79c25.jpg)

Adicione quantos campos quiser e forem necessários para o seu formulário.

Preencha o primeiro campo da aba atributos com um nome amigável (será usado no Elementor).

Por exemplo: se é o campo Nome Completo você pode preencher como **nome-completo** ou **nomecompleto**.

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/f6eb2688-70b6-477f-8889-6125881f8bd3.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/f6eb2688-70b6-477f-8889-6125881f8bd3.jpg)

Salve o formulário e está pronto.

**Não inclua campos de captcha porque não será possível integrar ao Elementor**.  

Ao editar um formulário, na URL será exibido o ID deste formulário (guarde-o para inserir no Elementor):

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/ae7c6ece-1e27-4fcf-aefd-434c1bb5176b.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/ae7c6ece-1e27-4fcf-aefd-434c1bb5176b.jpg)

Na imagem acima, o ID é o número 1.  

## No Elementor

No seu Painel, navegue até Elementor -> Configurações -> Integração -> Mautic -> e informe a URL da sua instalação.

Agora, crie um formulário no Elementor PRO com os mesmos campos do formulário Mautic.

Dentro de cada campo, na aba Advanced, o **ID** deve ser o mesmo preenchido no Mautic, que no nosso exemplo era **nome-completo** ou **nomecompleto**.

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/c29bb276-7243-4785-9098-9c9401c13c78.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/c29bb276-7243-4785-9098-9c9401c13c78.jpg)

  

Nas **Ações após submissão**, selecione Mautic. Você pode configurar quantas ações quiser (Mailchimp, e-mail, webhook...) ou apenas o Mautic.

[![](https://d29l98y0pmei9d.cloudfront.net/article/2624/dd693ff1-a33b-463a-bf09-e411a9853e11.jpg)](https://d29l98y0pmei9d.cloudfront.net/article/2624/dd693ff1-a33b-463a-bf09-e411a9853e11.jpg)

Nas configurações específicas, informe o ID do **formulário no Mautic**. 

Pronto! Seu formulário já está integrado.

**Importante!** Os campos marcados como **obrigatórios** no Mautic também devem ser **obrigatórios no Elementor**, caso contrário haverá falha na validação.  

No entanto, se um campo é opcional no Mautic, ele pode ser obrigatório no Elementor.

Se um campo é opcional no Mautic, ele não precisa estar presente no Elementor.

Se o seu Mautic tem uma URL do tipo mautic.site.com/**index.php**/s/login

Você deve incluir o index.php na hora de preencher a URL do Mautic nas configurações do plugin. 

[](https://d29l98y0pmei9d.cloudfront.net/article/2624/ddde27c0-e518-4337-911f-f92c19e14847.jpg)

___

Keywords: