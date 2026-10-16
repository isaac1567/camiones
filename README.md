# Control de camiones

Aplicación web para que dueños de camiones lleven sus viajes, pagos, turnos, mantenimiento y deudas de choferes.

- Abrir: https://isaac1567.github.io/camiones/
- Cada persona crea su cuenta (Google o correo y contraseña) y solo ve sus propios datos.
- Funciona en el teléfono sin señal y se puede instalar como app ("Agregar a pantalla de inicio").

## Cómo está hecha

- Página única (`index.html`) publicada con GitHub Pages.
- Cuentas y base de datos: Firebase (Authentication + Cloud Firestore), plan gratis.
- `firebase-config.js`: configuración pública del proyecto. No es una contraseña; lo que protege los datos son las reglas.
- `firestore.rules`: cada usuario solo puede leer y escribir dentro de `users/{su uid}/`.
