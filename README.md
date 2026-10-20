# 🏠 Buzgenda - Sistema Integral de Organización del Hogar

> **PWA (Progressive Web App) Mobile-First** lista para desplegar en **GitHub Pages** e instalar como aplicación nativa en tu teléfono móvil (iOS / Android), exactamente con la misma arquitectura que **BuzFinance**.

---

## 📱 Cómo Subirlo a GitHub y Usarlo en tu Móvil (Paso a Paso)

### Paso 1: Crear el repositorio en GitHub
1. Entra en tu cuenta de [GitHub](https://github.com/) y pulsa sobre el botón verde **«New»** (Nuevo repositorio).
2. Asigna un nombre al repositorio, por ejemplo: `Buzgenda` o `buzgenda-pwa`.
3. Selecciona **Public** (Público) para que GitHub Pages sea gratuito.
4. **No** es necesario marcar "Add a README" ni .gitignore. Pulsa **«Create repository»**.

---

### Paso 2: Subir los archivos del proyecto
Puedes subir los archivos directamente desde el navegador web sin necesidad de tener Git instalado:

1. En la página del repositorio recién creado, haz clic en el enlace azul: **«uploading an existing file»** (o ve a *Add file* > *Upload files*).
2. Selecciona y arrastra **todos los archivos** de tu carpeta `c:\Users\Buceta\Downloads\Buzgenda`:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `icon-192.png`
   - `icon-512.png`
   - `icon-512-maskable.png`
   - `README.md`
3. En la parte inferior, escribe un mensaje de commit (por ejemplo: `Versión inicial Buzgenda PWA`) y pulsa **«Commit changes»**.

---

### Paso 3: Activar GitHub Pages (Hosting Web Gratuito)
1. En tu repositorio de GitHub, entra en la pestaña **«Settings»** (Configuración) en la barra superior.
2. En el menú lateral izquierdo, haz clic en **«Pages»**.
3. En el apartado **Build and deployment**:
   - **Source**: Selecciona `Deploy from a branch`.
   - **Branch**: Elige `main` (o `master`) y la carpeta `/(root)`.
4. Pulsa el botón **«Save»** (Guardar).
5. Espera unos 60 segundos y refresca la página. Aparecerá un aviso verde con tu enlace público:
   ```text
   Your site is live at https://TU-USUARIO.github.io/Buzgenda/
   ```

---

### Paso 4: Instalar en tu Móvil como App Nativa (Igual que BuzFinance)

Abre el enlace generado en el navegador de tu teléfono móvil:

- **En iPhone (Safari)**:
  1. Abre el enlace en Safari.
  2. Pulsa el botón de **Compartir** (icono de cuadrado con flecha hacia arriba).
  3. Desplaza hacia abajo y selecciona **«Añadir a pantalla de inicio»** (o *Add to Home Screen*).
  4. Confirma el nombre "Buzgenda" y pulsa **Añadir**.

- **En Android (Google Chrome)**:
  1. Abre el enlace en Chrome.
  2. Pulsa el menú de tres puntos (arriba a la derecha).
  3. Selecciona **«Instalar aplicación»** o **«Añadir a pantalla de inicio»**.
  4. Confirma la instalación.

> 🎉 **¡Listo!** La app tendrá su propio icono esmeralda con el logo del hogar en tu pantalla de inicio, se abrirá a pantalla completa (sin barras de navegador), funcionará **100% offline** (incluso en modo avión) y guardará tus datos de forma privada en el almacenamiento local de tu teléfono (`localStorage`).

---

## 📂 Estructura del Proyecto

```text
Buzgenda/
├── index.html            # Aplicación completa (HTML5 semántico, CSS responsivo y JS reactivo)
├── manifest.json         # Especificación PWA (colores, orientación portrait, iconos)
├── service-worker.js     # Cacheo offline con estrategia Network-first
├── icon-192.png          # Icono 192x192 para pantallas estándar y móviles
├── icon-512.png          # Icono 512x512 de alta resolución
├── icon-512-maskable.png # Icono 512x512 adaptativo con padding seguro para Android/iOS
└── README.md             # Guía de despliegue y arquitectura
```

---

## 🧠 Características Principales

1. **📦 Inventario del Hogar (El núcleo)**:
   - Registro de productos: Nombre, Categoría, Ubicación (Nevera, Despensa, etc.), Cantidad, Unidad, Estado (Disponible, Agotándose, Agotado) y Umbral de alerta mínima.
   - Buscador en tiempo real y filtros combinados por Ubicación, Categoría y Estado.
   - Steppers rápidos `[-]` y `[+]` en cada tarjeta para ajuste de stock con una mano.
   - Botón directo para pasar a la compra si falta stock.

2. **🛒 Lista de la Compra (Inteligente y Antiduplicados)**:
   - **Sistema Antiduplicados en tiempo real**: Avisa inmediatamente mientras escribes si el producto ya existe en alguna ubicación de tu casa con su cantidad actual.
   - **Sincronización Automática al Comprar**: Al marcar un producto como comprado, se suma automáticamente al stock en el inventario.
   - **Botón «+ Añadir Agotados»**: Añade con 1 toque todos los productos que están agotados en el inventario.

3. **📅 Agenda / Lista de Tareas**:
   - Gestión de tareas del hogar con título, notas, fecha de vencimiento y prioridad (Alta, Media, Baja).
   - Filtros: Todas, Pendientes, Para Hoy, Vencidas y Completadas.

4. **✨ UX/UI & Privacidad**:
   - Modo Oscuro suave y Modo Claro alternables con 1 clic.
   - Barra de navegación inferior móvil estilo iOS/Android.
   - Cero servidores externos: Privacidad total con datos guardados localmente.
   - Herramienta para descargar copia de seguridad en `.json` y restaurarla cuando quieras.
