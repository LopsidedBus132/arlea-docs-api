# Endpoints — Colorimetría

---

## POST /colorimetria/analizar  
**Descripción:** Genera opciones preliminares de colorimetría antes de la confirmación final.

### Request
```json
{
  "usuario_id": "uuid",
  "imagen": "<base64>"
}
```
### Response
```json

{
  "opciones": {
    "color_piel": ["Beige Melocotón", "Arena Suave"],
    "color_pelo": ["Castaño Rojizo", "Castaño Oscuro"],
    "color_ojos": ["Avellana", "Marrón Suave"],
    "color_cejas": ["Café Medio", "Café Oscuro"],
    "estacion": ["Otoño", "Otoño Suave"],
    "sub_estacion": ["Suave", "Profunda"],
    "paletas": [
      { "hex": ["#D8B8A8", "#C0A090"] },
      { "hex": ["#E4C7B8", "#74503C"] }
    ]
  }
}
```
## POST /colorimetria/guarda
**Descripción**: Almacena la colorimetría final del usuario.

### Request
```json

{
  "usuario_id": "uuid-del-usuario",
  "color_piel": "Beige Melocotón",
  "color_pelo": "Castaño Rojizo",
  "color_ojos": "Avellana",
  "color_cejas": "Café Oscuro",
  "estacion": "Otoño",
  "sub_estacion": "Suave",
  "imagen_persona": "https://ruta/imagen.jpg",
  "colores": {
    "piel": ["#D8B8A8"],
    "pelo": ["#8C5A3C"],
    "ojos": ["#6C4F3D"]
  }
}
```
### Response
```json
{
  "message": "Colorimetría confirmada",
  "colorimetria": {
    "id_colorimetria": "uuid-generado",
    "usuario_id": "uuid-del-usuario",
    "color_piel": "Beige Melocotón",
    "color_pelo": "Castaño Rojizo",
    "color_ojos": "Avellana",
    "color_cejas": "Café Oscuro",
    "estacion": "Otoño",
    "sub_estacion": "Suave",
    "imagen_persona": "https://ruta/imagen.jpg",
    "colores": {
      "piel": ["#D8B8A8"],
      "pelo": ["#8C5A3C"],
      "ojos": ["#6C4F3D"]
    },
    "timestamp": "2025-11-25T12:34:00.000Z"
  }
}
```