# 🏠 Buzgenda - Sistema Integral de Organización del Hogar

> **PWA (Progressive Web App) Mobile-First** lista para desplegar en **GitHub Pages** e instalar como aplicación nativa en tu teléfono móvil (iOS / Android), con la misma arquitectura que **BuzFinance** y potenciada con metodologías **Superpowers**.



### Paso 4: Instalar en tu Móvil como App Nativa 

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

---

## ⚡ Nuevas Capacidades y Mejoras Integradas

### 1. 🧠 Motor Antiduplicados 2.0 (Fuzzy Matching Heurístico)
- **Tolerancia a Plurales y Singulares**: Reconoce automáticamente que *"Tomates"* coincide al 98% con *"Tomates de ensalada"* o *"Tomate"*.
- **Tolerancia a Erratas (Levenshtein)**: Si tecleas *"Deterjente"*, detecta una coincidencia del 90% con *"Detergente lavadora"*.
- **Alerta Enriquecida con Grado de Similitud**: Informa del porcentaje exacto de coincidencia, la ubicación donde está y su estado actual.

### 2. ⏱️ Control de Fechas de Caducidad
- **Campo de Caducidad Opcional**: Registra fecha de caducidad o consumo preferente en cualquier producto del inventario.
- **Semáforo Visual**:
  - 🟢 *Caduca en X días* (más de 3 días)
  - 🟡 *¡Caduca en X días / hoy!* (3 días o menos)
  - 🔴 *Caducado hace X días*
- **Filtro Rápido**: Chip `⏱️ Caducan Pronto / Caducados` para auditar la despensa en 1 segundo.

### 3. 📍 Ubicaciones y Categorías Dinámicas
- Crea tus propios espacios en casa (*Arcón congelador*, *Bodega*, *Garaje*, *Buhardilla*) y tus propias categorías (*Mascotas*, *Bebé*, *Papelería*) desde la propia app con guardado permanente.

### 4. 📳 UX Móvil: Haptics y Deshacer (Undo)
- **Vibración Háptica**: Feedback táctil nativo al sumar/restar stock, marcar items o completar tareas.
- **Sistema de Deshacer (Undo)**: Al eliminar cualquier elemento, un Toast interactivo ofrece 5 segundos para restaurarlo de inmediato con un toque.

### 5. 🧪 Suite de Diagnóstico y Pruebas Unitarias (Superpowers TDD)
- Accesible desde el botón de Ajustes/Gestión de Datos: ejecuta en milisegundos una batería de pruebas automatizadas que valida la algoritmia de similitud, la lógica de caducidades y la integridad del stock.
