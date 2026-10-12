# Práctica 5 - API REST USUARIOS Y PRODUCTOS

Proyecto backend desarrollado con **Django REST Framework** y **PostgreSQL**, utilizando contenedores de **Docker** para la base de datos y documentado con **Swagger**.

---

## 🚀 Tecnologías y Herramientas Utilizadas
- **Python 3.8+ / Django 4.2**
- **Django REST Framework (DRF)**
- **PostgreSQL 15** (a través de Docker Compose)
- **drf-yasg** (para la generación de la interfaz de Swagger)
- **Linux Mint / Git / GitHub**

---

## 🛠️ Instrucciones de Configuración y Ejecución

Sigue estos pasos en tu terminal para poner a marchar el proyecto en tu equipo local:

### 1. Clonar el repositorio
```bash
git clone [https://github.com/TS-UAM26O-JMVH/p05_django.git](https://github.com/TS-UAM26O-JMVH/p05_django.git)
cd p05_django/proyectos_django/django4/proyecto_django/back_end_django
```

### 2. Levantar la base de datos con Docker compose
asegurate de tener DOcker activo y ejecuta el sigiente comando en la raiz donde se encuentra tu Docker-compose.yml
```bash
sudo docker compuse up -d
```
### 2.1 como detener la base de datos de Docker
Cuando termines de trabajar y desees apagar el contenedor de PostgreSQL de forma limpia, ejecuta el siguiente comando en la misma ruta donde se encuentra tu docker-compose.yml:
```bash
sudo docker compose down
```

### 3. Activar el entorno virtual
```bash
source venv/bin/activate
```

### 3.1 Cómo desactivar el entorno virtual
Para salir del entorno virtual y regresar a la terminal normal del sistema, simplemente ejecuta:
```bash
deactivate
```

### 4. Aplicar las migraciones de la Base de datos
```bash
python manage.py migrate
```

### 5. Iniciar el servidor de desarrollo
```bash
python manage.py runserver
```
### 5.1 Para detener el servidor de desarrollo de django
para detener el servidor en cualquier momento presiona en la terminal:
```
Ctrl +  C
```
---

## 🧪 Cómo Probar el Código y los Endpoints
Una vez que el servidor esté corriendo, puedes interactuar con la API de dos formas:

Interfaz gráfica de Swagger (Recomendado):
 Abre tu navegador web e ingresa a la siguiente URL para explorar y probar los métodos HTTP disponibles:
👉 http://127.0.0.1:8000/swagger/

Endpoints disponibles:

 Gestión de Usuarios:

    GET /api/usuarios/: Obtiene la lista completa de usuarios registrados.

    POST /api/usuarios/: Permite registrar un nuevo usuario en la base de datos.

 Gestión de Productos (Práctica 5):

    GET /api/products/: Obtiene la lista completa de productos activos.

    POST /api/products/: Crea un nuevo producto validando sus campos y estructura.

    GET /api/products/{id}/: Obtiene los detalles de un producto específico mediante su UUID.

    PUT /api/products/{id}/: Actualiza de forma completa un producto.

    PATCH /api/products/{id}/: Actualiza de forma parcial un producto.

    DELETE /api/products/{id}/: Realiza un borrado lógico del producto.

---

## 👨‍💻 Autor

Desarrollado por Juan Valentin.


