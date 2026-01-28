# Login en Amazon 

 

## Descripción

  

El sistema de autenticación permite a los usuarios iniciar sesión usando **correo electrónico y contraseña**

  

---

  

## Escenario

  

1. El usuario ingresa su correo electrónico y contraseña

2. La aplicación envía las credenciales al sistema

3. Se  validan las credenciales

4. Se redirige al inicio de la pagina  /home
  

## Request

  

```json

{

"email": "userejemplo@gmail.com",

"password": "Contraseña123!!"

}

```

  

### Validaciones

- Email con formato válido
- Contraseña correcta 
- Cuenta registrada

  
  

## Response

  

```json

{

"accessToken": "eyJraWQiOiJLT1E...",

"idToken": "eyJhbGciOiJSUzI1NiIs...",

"refreshToken": "eyJjdHkiOiJKV1QiLCJlbmMiOiJBMjU2R0NNIn0..."

}

```


## Manejo de Errores
* Se limita el numero de intentos consecutivos
* No especifica el campo incorrecto
* Se dirige a  **"Registrarse"** después de ingresar un correo no vinculado a una cuenta


| Escenario | Resultado Esperado |Pasos de ejecución | Resultado Real |
|----------|----------|----------|--------|
| Login exitoso con usuario valido    | Redirigir a home   |   |    Aprobado    | 
| Intento de login con correo invalido   | Alerta "  La dirección de correo electrónico no es válida"   |    | Aprobado       |
| Intento de login sin contraseña    | Alerta "Ingrese su contraseña"   |    | Aprobado      | 