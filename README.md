# Laravel-Autenticacion

Ejemplo de explicación del flujo y funcionamiento para tu tarea de autenticación en Laravel
1. Creación de la base de datos y tabla Users
Se creó una base de datos llamada autenticacion.

Se definió la tabla users con campos básicos: id, name, email, password, created_at, updated_at.

La contraseña se almacena cifrada usando bcrypt para garantizar la seguridad.

2. Registro de usuario
El formulario de registro solicita email y password.

El email se valida para que tenga formato correcto y no esté repetido en la base.

La contraseña se cifra automáticamente antes de guardarse en la tabla users.

Cuando el usuario se registra, sus datos se almacenan en la tabla users.

3. Login / autenticación
El formulario de login solicita email y password.

Se valida que el email exista en la base.

Se compara la contraseña cifrada almacenada con la ingresada usando bcrypt.

Si las credenciales son correctas, el usuario inicia sesión.

En caso de error, se muestra un mensaje claro (ejemplo: "Email no registrado" o "Contraseña incorrecta").

4. Mantener la sesión activa
Laravel utiliza sesiones para mantener autenticado al usuario.

Se protege la ruta /dashboard para que solo usuarios autenticados puedan acceder.

Si un usuario no autenticado intenta entrar a /dashboard, se le redirige al login.

5. Flujo general en la aplicación
Usuario nuevo accede a /register, completa formulario y crea cuenta.

Usuario existente accede a /login, ingresa sus credenciales y si son válidas, accede a /dashboard.

En /dashboard se muestra contenido protegido, visible solo para usuarios autenticados.

Usuario puede cerrar sesión y terminar la sesión actual.

6. Uso de herramientas y tecnologías
Se usó Laravel con PHP para la lógica del backend.

La base de datos es MySQL.

Las contraseñas se cifran con bcrypt (integrado en Laravel).

Validaciones de formulario para email y contraseña están implementadas.

Código fuente disponible en GitHub (proporcionar enlace).

Script SQL exportado desde MySQL Workbench para crear base y tabla.
