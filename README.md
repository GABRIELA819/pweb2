# pweb2
1. La estructura del proyecto
2. El proyecto tiene tres partes principales: el archivo app.py que es el servidor, la
carpeta models con las clases de Python, y la carpeta templates con el HTML.
3. Las clases (models/producto.py)
Creé una clase abstracta llamada Producto que no se puede instanciar directamente.
Esto lo logré usando ABC y abstractmethod de Python. Esta clase obliga a que todas
sus subclases implementen el método mostrar_info().
De ella heredan dos clases:
ProductoDigital, que agrega el atributo tamanio_mb
ProductoFisico, que agrega el atributo peso_kg
Esto es herencia. Y cuando llamo mostrar_info() en cualquier producto, cada clase
responde de forma distinta según su tipo, eso es polimorfismo.
4. El servidor (app.py)
Usé Flask para crear el servidor. Tiene dos rutas:
 La ruta / que renderiza la página web con los productos
La ruta /api/productos que devuelve los productos en formato JSON
Para pasar los productos al HTML usé render_template, que es el sistema de
plantillas de Flask llamado Jinja2.
5. El HTML (templates/index.html)
6. El HTML usa Jinja2 para mostrar los productos dinámicamente con un {% for %}.
Dependiendo del tipo de producto muestra información distinta, como el tamaño en MB
para digitales o el peso en kg para físicos.
7. La documentación Swagger
8. Usé flask-restx para generar automáticamente la documentación de la API. Se
puede ver en /swagger e incluye los endpoints disponibles y qué datos devuelven.
