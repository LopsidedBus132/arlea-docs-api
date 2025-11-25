# Autenticación (AUTH)

## POST /auth/register

### Request
```json
{
  "email": "usuario@example.com",
  "password": "12345678",
  "nombre": "Alex Santana",
  "genero": "Masculino",
  "pais": "Chile",
  "fecha_nacimiento": "2001-10-15"
}
```

## Response
```json
{
  "message": "Usuario registrado correctamente",
  "id_usuario": "uuid",
  "email": "usuario@example.com",
  "token": "<jwt_token>"
}
```
## POST /auth/login
### Request
```json
{
  "email": "usuario@example.com",
  "password": "12345678"
}
```

### Response
```json
{
  "message": "Login exitoso",
  "token": "<jwt_token>",
  "id_usuario": "uuid"
}
```