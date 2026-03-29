# 📱 QR Redirect App

Aplicación web simple que permite **redirigir usuarios mediante códigos QR dinámicos** usando un parámetro en la URL y un backend en Google Apps Script.

---

## 🚀 Descripción

Este proyecto consiste en una página HTML que:

1. Lee un parámetro `k` desde la URL
2. Consulta un servicio externo (Google Apps Script)
3. Obtiene una URL asociada a ese parámetro
4. Redirige automáticamente al usuario

👉 Ideal para generar **códigos QR dinámicos**, donde el destino puede cambiar sin modificar el QR.

---

## 🧠 ¿Cómo funciona?

El flujo es el siguiente:

```
Usuario escanea QR
        ↓
Se abre la URL con parámetro ?k=valor
        ↓
La app consulta el backend (Google Script)
        ↓
Recibe una URL de destino
        ↓
Redirige automáticamente
```

---

## 🔗 Ejemplo de uso

```
https://tu-dominio.com?k=123
```

El valor `123` se envía al backend, que responde con algo como:

```
https://google.com
```

👉 El usuario será redirigido automáticamente a esa URL.

---

## 🛠️ Tecnologías utilizadas

* HTML5
* CSS3 (animaciones de carga)
* JavaScript (Fetch API)
* Google Apps Script (backend)

---

## 📂 Estructura del proyecto

```
qr/
│── index.html   # Archivo principal
```

---

## ⚙️ Configuración

### 1. Backend (Google Apps Script)

Debes tener un endpoint como este:

```
https://script.google.com/macros/s/TU_SCRIPT_ID/exec
```

Este debe recibir el parámetro `k` y devolver una URL válida.

Ejemplo de respuesta:

```
https://miweb.com
```

---

### 2. Configurar la URL base

En el código, modifica esta línea:

```javascript
const AS_URL_BASE = "TU_URL_DE_GOOGLE_SCRIPT";
```

---

## 🎨 Características

* 🔄 Redirección automática
* ⏳ Indicador de carga animado
* 🌐 Soporte para parámetros dinámicos
* 📱 Compatible con móviles (ideal para QR)

---

## 📸 Uso con códigos QR

Puedes generar un QR que apunte a:

```
https://tu-dominio.com?k=producto1
```

Luego, desde el backend decides a dónde redirigir:

* Promociones
* Productos
* Formularios
* Redes sociales

---

## ⚠️ Consideraciones

* El backend debe responder rápidamente
* Validar los valores de `k`
* Evitar redirecciones maliciosas
* Manejar errores si no hay respuesta

---

## 🧪 Mejoras futuras

* Interfaz para administrar links
* Base de datos (Sheets o Firebase)
* Estadísticas de escaneos
* Personalización de QR

---

## 📄 Licencia

Este proyecto es de uso libre para fines educativos y personales.

---

## 👨‍💻 Autor

Desarrollado por **elmerpabel**

