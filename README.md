# Solución prueba ingreso SoloTodo
## Parte 1: Desarrollo de API usando Python y Django

## Instalación

Acorde a la indicación dada el proyecto se instala de la siguiente forma:

- Crear un ambiente virtual vacío ubicado en la carpeta raíz del proyecto
  
  ```
  // MacOs
  python3 -m venv mi_env
  source mi_env/bin/activate
  ```
  ```
  // Windows
  python -m venv mi_env
  mi_env\Scripts\activate.bat
  ```
- Instalar dependencias del proyecto
  ```
  pip install -r requirements.txt
  ```
- Correr las migraciones del proyecto
  ```
  python manage.py migrate
  ```
- Crear un superuser
  ```
  python manage.py createsuperuser
  ```
- Correr la aplicación
  ```
  python manage.py runserver
  ```

## Uso

Hay 3 endpoints disponibles

GET  /posts

Devuelve todos los posts existentes

**Respuesta**
```
[
    {
        "id": 1,
        "title": "Primer post",
        "content": "Bienvenidos al blog de SoloTodo",
        "author": "Tomás Díaz Toro",
        "created_at": "2024-06-27T12:00:00.000000Z"
    },
    ...
]
```

GET  /posts/:id

Devuelve un post específico

**Respuesta**
```
{
    "id": 1,
    "title": "Primer post",
    "content": "Bienvenidos al blog de SoloTodo",
    "author": "Tomás Díaz Toro",
    "created_at": "2024-06-27T12:00:00.000000Z"
}
```

POST /posts

Crea un nuevo post

**Parámetros**
|Name|Required|Type|                                                                                                                                                      
| :----------|:--------|:-------|
|`title` | required | string  |
|`content` | required | string  | 
|`author` | required | string  | 

**Respuesta**
```
{
    "id": 2,
    "title": "Segundo post",
    "content": "Bienvenidos otra vez al blog de SoloTodo",
    "author": "Tomás Díaz Toro",
    "created_at": "2024-06-28T12:00:00.000000Z"
}
```
