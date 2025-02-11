# API PIX 📜

Com API você pode integrar o PIX ao seu sistema.
Obs: Os valores devem ser tratados como Float

## URL BASE

 `https://api.binbank.com.br`

## Rotas 


 `post` **/login**
<br>
body:
```
{	
	"user":		string,
	"password":	string
}
```

Response:
```
{
	"status": 	  string,
  	"x-access-token": string,
  	"personData": {
	  "user": 	string,
	  "email": 	string,
    	  "id_logins": 	number,
    	  "role":	string,
    	  "valor": 	number,
    	  "cpfCnpj": 	string,
    	  "nome": 	string
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
	"x-access-token": "token recebido pela rota /login",
}
```
<br>
<br>
<br>

 `post` **/dashboard/cliente**
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

 `post` **/pix/transfer**


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
	"key": 	    string,
  	"amount":   number
}
```

<br>
<br>
<br>

## CASHIN
<br>

 `post` **/pix/cobrar**


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
	"amount": number
}
```

<br>
<br>
<br>



