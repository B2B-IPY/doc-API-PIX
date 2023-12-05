# API PIX 📜

Com API você pode integrar o PIX ao seu sistema.

## URL BASE

 `https://pix.b2btecnologia.io`

## Rotas 


 `post` **/login**
<br>
body:
```
{
	"user_login":"gstv",
	"password_login":"Gustavo123"
}
```

<br>
<br>
<br>

 `get` **/balance**
<br>
Verifica o saldo disponivel em conta

Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```
<br>
<br>
<br>

## CASHOUT
<br>

 `post` **/create-cashout**


Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>

Body:
```
{
	"value": 1,
	"pixKey": "39857534000174",
	"creditorDocument": "39857534000174",
	"description": "withdraw",
	"url_notify": "https://webhook.site/61e7v93f-c2a4-4f8f-aa25-25466cdb8a14",
	"order_id": "adcadzf-amsn3kna-30nmssa"
}
```

<br>
<br>
<br>





 `get` **/search-cashout/:order-id**

Exemplo: /search-cashout/adcadzf-amsn3kna-30nmssa

Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>
<br>
<br>





 `get` **/search-cashout/e2e/:e2e**

Exemplo: /search-cashout/e2e/E0825353920231204193933984d6b8e6

Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>
<br>
<br>





 `get` **/search-cashout/txid/:txid**

Exemplo: /search-cashout/txid/5804250afc642ef8736f708f169c016u0


Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>
<br>
<br>





 `get` **/payment-voucher/:order_id**

Exemplo: /payment-voucher/adcadzf-amsn3kna-30nmssa


Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>
<br>
<br>

## CASHIN
<br>

 `post` **/create-cashin**


Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>

Body:
```
{
	"value": 100,
	"expiration_time": 86400,
	"url_notify": "https://webhook.site/61e7d93f-c2a4-4f8f-aa25-25466cdb8a14",
	"order_id": "cz3878af-v805-47vc-b419-va19773f1vka"
}
```

<br>
<br>
<br>





 `get` **/search-cashin/:order_id**

Exemplo: /search-cashin/cz3878af-v805-47vc-b419-5a19773f1vka

Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>
<br>
<br>





 `get` **/search-cashin/e2e/:e2e**

Exemplo: /search-cashin/e2e/E0825353920231204193933984d6b8e6

Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>
<br>
<br>





 `get` **/search-cashin/txid/:txid**

Exemplo: /search-cashin/txid/5804250afc642ef8736f708f169c016u0


Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
}
```

<br>
<br>
<br>



