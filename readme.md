# API PIX 📜

Com API você pode integrar o PIX ao seu sistema.


## URL BASE

 `https://api.binbank.com.br`

## Rotas 


 `post` **/login**
<br>
body:
```
{
	"user":"Seu_usuario",
	"password":"Sua_senha"
}
```

Response:
```
{

  "status": "isLogged",
  "x-access-token": "x-access-token",
  "personData": {
    "user": "seu_usuario",
    "email": "seu_email",
    "id_logins": 1,
    "role": "sua_role",
    "valor": 0,
    "cpfCnpj": "seu_documento",
    "nome": "seu_nome"
  }

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

 `post` **/dashboard**
<br>
Verifica todos os dados da conta

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
	"order_id": "adcadzfamsn3kna30nmssa"
}
```

<br>
<br>
<br>



 `get` **/search-cashout**


Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
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
	"order_id": "cz3878afv80547vcb419va19773f1vka"
}
```

<br>
<br>
<br>


 `get` **/search-cashin**


Headers:
```
{
	"x-access-token":"token recebido pela rota /login",
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



