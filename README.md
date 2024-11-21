

## Linguagem

```php
javascript
```

## Pré-requisitos

```php
Clonar o projecto
```


## Cadastro de usuário

```
curl --location 'https://go-wash-api.onrender.com/api/user' \
--header 'Content-Type: application/json' \
--header 'Cookie: gowash_session=0hGqRHf0q38ETNgEcJGce30LcPtuPKo48uKtb7Oj' \
--data-raw '{
    "name":"xxxxxxxxxxx",
    "email":"xxxxxxxxx@gmail.com",
    "user_type_id":1,
    "password": "123456",
    "cpf_cnpj": "62418247406",
    "terms": 1,
    "birthday":"2000-10-12"    
} '
```


## Login

```
curl --location 'https://go-wash-api.onrender.com/api/login' \
--header 'Content-Type: application/json' \
--header 'Cookie: gowash_session=0hGqRHf0q38ETNgEcJGce30LcPtuPKo48uKtb7Oj' \
--data-raw '{
"email": "xxxxxx@gmail.com",
"password":"123456",
"user_type_id":1
}'
```
##Resposta Login

```
{
    "data": {
        "errors": "Usuário não esta ativo"
    }
}
```
![alt text](https://github.com/carlosrmfernandes/project-dw/assets/22120478/49fcd1da-25d6-45d1-88c8-d1c37f245293)

```
{
    "data": {
        "errors": "Usuário não foi encontrado"
    }
}
```
![alt text](https://github.com/carlosrmfernandes/project-dw/assets/22120478/9571f618-7845-4d89-a6de-eaaa1b14140a)

```
{
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodtZWZjOWM5NTgyNjg3Lmhlcm9rdWFwcC5jb20vYXBpL2xvZ2luIiwiaWF0IjoxNzEyMDc4Mjg0LCJuYmYiOjE3MTIwNzgyODQsImp0aSI6ImRPajVkTng4WEgxdVJ5TVkiLCJzdWIiOiIxIiwicHJ2IjoiMjNiZDVjODk0OWY2MDBhZGIzOWU3MDFjNDAwODcyZGI3YTU5NzZmNyJ9.oBAOYBcADNUiwFKgM",
    "token_type": "bearer",
    "expires_in": null,
    "user": {
        "id": 1,
        "name": "xxxxxxxxxx",
        "is_active": true,
        "is_socialite": false,
        "terms": true,
        "cpf_cnpj": "xxxxxxxxxx",
        "email": "xxxxxxxxx@gmail.com",
        "user_type_id": 1,
        "birthday": "xxxx-xx-xx",
        "phone": "xxxxxxxxx",
        "avatar": null,
        "attachment": null,
        "document_status": null,
        "created_at": "2024-03-14T15:08:44.000000Z"
    }
}
```

## Listar todos endereço de um usuario

```
curl --location 'https://go-wash-api.onrender.com/api/auth/address' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vYXBpLWdvLXdhc2gtZWZjOWM5NTgyNjg3Lmhlcm9rdWFwcC5jb20vYXBpL2xvZ2luIiwiaWF0IjoxNzEwNDE3MjIyLCJuYmYiOjE3MTA0MTcyMjIsImp0aSI6InBsZll0aENEZ0U1NUNzMHEiLCJzdWIiOiIxIiwicHJ2IjoiMjNiZDVjODk0OWY2MDBhZGIzOWU3MDFjNDAwODcyZGI3YTU5NzZmNyJ9.z1pdEBkx8Hq01B7jNKa42NGxtFFHwb-7O_0y8krVWUY' \
--header 'Cookie: gowash_session=0hGqRHf0q38ETNgEcJGce30LcPtuPKo48uKtb7Oj' \
--data ''
```

## Cadastro de endereço

```
curl --location 'https://go-wash-api.onrender.com/api/auth/address' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vYXBpLWdvLXdhc2gtZWZjOWM5NTgyNjg3Lmhlcm9rdWFwcC5jb20vYXBpL2xvZ2luIiwiaWF0IjoxNzEwNDE3MjIyLCJuYmYiOjE3MTA0MTcyMjIsImp0aSI6InBsZll0aENEZ0U1NUNzMHEiLCJzdWIiOiIxIiwicHJ2IjoiMjNiZDVjODk0OWY2MDBhZGIzOWU3MDFjNDAwODcyZGI3YTU5NzZmNyJ9.z1pdEBkx8Hq01B7jNKa42NGxtFFHwb-7O_0y8krVWUY' \
--header 'Cookie: gowash_session=0hGqRHf0q38ETNgEcJGce30LcPtuPKo48uKtb7Oj' \
--data '{
    "title":"Minha Casa",
    "cep": "03730000",
    "address": "Rua Brazópolis Jardim Jaú (Zona Leste)",
    "number": "8A",
    "complement": ""
}'
```

## Atualizar endereço

```
curl --location 'https://go-wash-api.onrender.com/api/auth/address/4' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vYXBpLWdvLXdhc2gtZWZjOWM5NTgyNjg3Lmhlcm9rdWFwcC5jb20vYXBpL2xvZ2luIiwiaWF0IjoxNzEwNDE3MjIyLCJuYmYiOjE3MTA0MTcyMjIsImp0aSI6InBsZll0aENEZ0U1NUNzMHEiLCJzdWIiOiIxIiwicHJ2IjoiMjNiZDVjODk0OWY2MDBhZGIzOWU3MDFjNDAwODcyZGI3YTU5NzZmNyJ9.z1pdEBkx8Hq01B7jNKa42NGxtFFHwb-7O_0y8krVWUY' \
--header 'Cookie: gowash_session=0hGqRHf0q38ETNgEcJGce30LcPtuPKo48uKtb7Oj' \
--data '{
    "title":"Minha Casa ola",
    "cep": "03730000",
    "address": "Rua Brazópolis Jardim Jaú (Zona Leste)",
    "number": "8A",
    "complement": ""
}'
```

## Deletar um edereço

```
curl --location --request DELETE 'https://go-wash-api.onrender.com/api/auth/address/3' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOi8vYXBpLWdvLXdhc2gtZWZjOWM5NTgyNjg3Lmhlcm9rdWFwcC5jb20vYXBpL2xvZ2luIiwiaWF0IjoxNzEwNDE3MjIyLCJuYmYiOjE3MTA0MTcyMjIsImp0aSI6InBsZll0aENEZ0U1NUNzMHEiLCJzdWIiOiIxIiwicHJ2IjoiMjNiZDVjODk0OWY2MDBhZGIzOWU3MDFjNDAwODcyZGI3YTU5NzZmNyJ9.z1pdEBkx8Hq01B7jNKa42NGxtFFHwb-7O_0y8krVWUY' \
--header 'Cookie: gowash_session=0hGqRHf0q38ETNgEcJGce30LcPtuPKo48uKtb7Oj'
```


## Dúvida 

```
Prof.Esp: carlos.fernandes@faculdadeimpacta@gmail.com.br
```



