# Como abrir as conversas no app para desktop

**IMPORTANTE**! Isso é uma configuração do seu computador, não do plugin. Por isso não consigo oferecer suporte na configuração. Mas se não conseguir configurar o app desktop basta usar a versão web.

Abrir as conversas do WhatsApp no desktop é muito mais rápido do que abrir no navegador.

Você pode baixar para seu computador (Windows e Mac apenas) diretamente do site oficial do WhatsApp.

Se tudo estiver configurado corretamente você conseguirá abrir este link no WhatsApp desktop. 

[Clique aqui para testar](whatsapp://send?phone=5555555555555&text=Fernando!).

Caso não abra, você deve verificar suas configurações de aplicativo. infelizmente não consigo ajudar nessa parte.

Depois, ative a opção de usar desktop app nas configurações do plugin.

### Tentando ajudar

Como disse acima, isso é uma configuração do seu computador - não do plugin. No entanto, irei tentar ajudar aqui, mas não posso garantir que isso funcionará.

Se você usa Mac isso funcionará automaticamente.

Se você usa Windows, baixe o WhatsApp do site oficial. **Não baixe da loja do Windows**.

Coloque isso aqui no seu arquivo:

```php
Windows Registry Editor Version 5.00 [HKEY_CLASSES_ROOT\whatsapp] "URL Protocol"="" [HKEY_CLASSES_ROOT\http\DefaultIcon] @="C:\\Users\\NOME_USUARIO\\AppData\\Local\\WhatsApp\\WhatsApp.exe,0" [HKEY_CLASSES_ROOT\whatsapp\shell] @="open" [HKEY_CLASSES_ROOT\whatsapp\shell\open] [HKEY_CLASSES_ROOT\whatsapp\shell\open\command] @="\"C:\\Users\\NOME_USUARIO\\AppData\\Local\\WhatsApp\\WhatsApp.exe\" \"%1\""
```

Veja que em 2 locais está escrito NOME\_USUARIO**. Você precisa** modificar isso pelo nome do seu usuário no computador.

Feito isso, salve na área de trabalho o arquivo com o nome **whatsapp.reg**

Vá até sua Área de Trabalho e abra esse arquivo - siga os passos na tela.

Se você configurou corretamente, os links devem começar a abrir pelo aplicativo.

**Reiterando que isso é problema na configuração do computador e não ofereço suporte a isso, apenas ao que está relacionado ao meu plugin**.  

### O plugin não abre o WhatsApp

Desculpe ser repetitivo... mas o plugin apenas envia um sinal e seu computador deve estar configurado para abrir os links do WhatsApp.

Em alguns computadores isso parece já vir configurado, ou versões. Eu realmente não tenho como testar isso. Para verificar se é algo isolado no plugin ou qualquer link de WhatsApp basta clicar em qualquer link similar e ver se funciona.

Recebi essa informação de um cliente há algum tempo que pode ajudar, **experimente por sua conta e risco** (embora não tenha risco algum... no máximo não vai funcionar):  

> _O bug é na nova versão do WhatsApp para Windows, versão 0.4.1299. A versão que funciona é 0.4.930. Você pode disponibilizar um link dentro da documentação pros usuários ficarem cientes. 1) Entre no Painel de Controle do Windows 2) Clique em Desinstalar Programas 3) Desinsale o WhatsApp versão 0.4.1299 4) Baixe essa versão do WhatsApp (https://my.pcloud.com/publink/show?code=XZQW0nkZFvwejbmgl2fpSvqTQu0L8uzOPW7V) 5) Instale no computador para usar a versão 0.4.930 que funciona Sempre que voltar a dar problema significa que o aplicativo atualizou automaticamente, então você precisa refazer esses passos. Para usuários de Mac não há mudanças, funciona normalmente._

>   

___

Keywords: