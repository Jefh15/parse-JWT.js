# parse-JWT.js
Parse - JWT - Obtener Payload y fecha de creación y expiración

```
function parseJwt (token) {
    var base64Url = token.split('.')[1];
    var base64 = base64Url.replace('-', '+').replace('_', '/');
    return JSON.parse(window.atob(base64));
};
```

# USO EN CONSOLA DE EXPLORADOR:

```
let token = 'eyJhbGciOiJIUzI1NiIsInR5cCI6I.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6Ikplc3VzIEZvbnNlY2EiLCJpYXQiOjE1MTYyMzkwMjIsIl9pZCI6ImFiYyIsImVkYWQiOiIxOTgiLCJjYXJkLW51bWJlciI6IjEzMjEtMzIxNi02NTQ.-p2iSrC7w5144S_MIQ2m1KuV0eFy_2yK19kgcEX'

parseJwt(token)
```

# Para ejecutarla:
![image](https://user-images.githubusercontent.com/31804499/110858010-2ea5b000-827f-11eb-8325-9a383a24b054.png)

# Para definir el token
![image](https://user-images.githubusercontent.com/31804499/110858211-6ad91080-827f-11eb-82da-2b4ace310a93.png)

# Para ejecutar con el token
![image](https://user-images.githubusercontent.com/31804499/110858398-a5db4400-827f-11eb-9781-bb568c04325b.png)

# Como resultado nos arroja:
![image](https://user-images.githubusercontent.com/31804499/110858504-c60b0300-827f-11eb-9190-581019a00a4c.png)




# Con esta pagina vemos el HEADER, PAYLOAD, VERIFY SIGNATURE, para hacer el ejemplo:

https://jwt.io/

# IMAGEN # 1
En esta imagen tenemos la informacion del token
![image](https://user-images.githubusercontent.com/31804499/110856931-df12b480-827d-11eb-91ac-1c9687a4d342.png)

# IMAGEN # 2
En esta imagen es como se veria el token, lo cual vamos a copiarlo para poder descubrir que tiene dicho token en ese dominio.
![image](https://user-images.githubusercontent.com/31804499/110857681-c787fb80-827e-11eb-884f-5d8e8f0648db.png)

