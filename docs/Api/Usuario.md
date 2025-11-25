# Usuario

## GET /usuario/me

### Response
```json
{
  "id_usuario": "uuid",
  "nombre": "Alex Santana",
  "genero": "Masculino",
  "pais": "Chile",
  "fecha_nacimiento": "2001-10-15"
}
```
## PATCH /usuario/me
### Request
```json
{
  "nombre": "Alex Actualizado",
  "genero": "Masculino",
  "pais": "Chile",
  "fecha_nacimiento": "2001-10-15"
}
```
### Response
```json
{
  "message": "Usuario actualizado",
  "usuario": {
    "id_usuario": "uuid",
    "nombre": "Alex Actualizado",
    "genero": "Masculino",
    "pais": "Chile",
    "fecha_nacimiento": "2001-10-15"
  }
}
```