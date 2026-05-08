# pweb2

1. El proyecto tiene tres partes principales: 
├── app.py                  # Punto de entrada principal (el archivo app.py que es el servidor)
├── models/
│   └── producto.py         # Clases de Productos (carpeta models con las clases de Python)
└── templates/ 
    └── index.html          # Vista web principal (carpeta templates con el HTML)
└── venv                    # Entorno virtual 
El servidor (app.py)
Usé Flask para crear el servidor. 
Para pasar los productos al HTML usé render_template, que es el sistema de
plantillas de Flask llamado Jinja2.
La documentación Swagger está disponible en `/swagger`
 
METODO MANUAL:
- Agregar productos al carrito
- Eliminar productos del carrito
- Calcular el total de la compra
La app corre por defecto en `http://127.0.0.1:5000`
