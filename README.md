# 📦 MictlanTeam Library - Librería KiCad

Librería completa de componentes electrónicos para KiCad, optimizada para facilitar el diseño de circuitos y PCBs.

## 📋 Contenido

Esta librería incluye:

- ⚡ **Símbolos esquemáticos** (`.kicad_sym`)
- 👣 **Footprints/Huellas PCB** (`.pretty`)
- 🎨 **Modelos 3D** (`.3dshapes`)
- 🧩 **Design Blocks** (`.kicad_dblk`) - KiCad 9.0+

---

## 🚀 Instalación Rápida

### Requisitos
- **KiCad 8.0.4 o superior** (recomendado KiCad 9.0)
- **Sistema operativo:** Windows, Linux o macOS

---

## 📥 Paso 1: Descargar/Clonar la Librería

### Opción A: Clonar con Git (Recomendado)
```bash
cd C:\Users\[TuUsuario]\Documents\KiCad\
git clone https://github.com/MictlanTeam/MictlanTeam-Library.git
```

### Opción B: Descarga Manual
1. Descargar ZIP desde: [GitHub - MictlanTeam-Library](https://github.com/MictlanTeam/MictlanTeam-Library)
2. Extraer en: `C:\Users\[TuUsuario]\Documents\KiCad\MictlanTeam-Library`

---

## ⚙️ Paso 2: Configurar Variables de Entorno en KiCad

### 2.1 Abrir configuración de rutas
1. Abrir **KiCad**
2. Ir a **Preferencias → Configurar rutas...**

### 2.2 Agregar variable MICTLAN_LIBRARY
Hacer clic en el botón **[+]** y agregar:

| Nombre | Ruta |
|--------|------|
| `MICTLAN_LIBRARY` | `C:\Users\[TuUsuario]\Documents\KiCad\MictlanTeam-Library` |

**Ejemplo en Windows:**
```
MICTLAN_LIBRARY = C:\Users\Samuel\Documents\KiCad\MictlanTeam-Library
```

**Ejemplo en Linux:**
```
MICTLAN_LIBRARY = /home/usuario/KiCad/MictlanTeam-Library
```

**Ejemplo en macOS:**
```
MICTLAN_LIBRARY = /Users/usuario/KiCad/MictlanTeam-Library
```

### 2.3 Guardar y cerrar
Hacer clic en **"Aceptar"**

---

## 📚 Paso 3: Agregar Librerías de Símbolos

### 3.1 Abrir administrador de librerías
1. En KiCad, ir a **Preferencias → Gestionar bibliotecas de símbolos...**
2. Seleccionar pestaña **"Bibliotecas globales"**

### 3.2 Agregar librería de símbolos
Hacer clic en el botón **[+]** y agregar:

| Activo | Apodo | Ruta de la biblioteca |
|--------|-------|-----------------------|
| ✓ | `MictlanTeam` | `${MICTLAN_LIBRARY}/MictlanTeam.kicad_sym` |

### 3.3 Guardar
Hacer clic en **"Aceptar"**

---

## 👣 Paso 4: Agregar Librerías de Footprints/Huellas

### 4.1 Abrir administrador de librerías
1. En KiCad, ir a **Preferencias → Administrar bibliotecas de huellas...**
2. Seleccionar pestaña **"Bibliotecas globales"**

### 4.2 Agregar librería de footprints
Hacer clic en el botón **[+]** y agregar:

| Activo | Apodo | Ruta de la biblioteca |
|--------|-------|-----------------------|
| ✓ | `MictlanTeam` | `${MICTLAN_LIBRARY}/MictlanTeam.pretty` |

### 4.3 Guardar
Hacer clic en **"Aceptar"**

---

## 🧩 Paso 5: Agregar Librerías de Design Blocks (KiCad 9.0+)

### 5.1 Abrir administrador de Design Blocks
1. En KiCad, ir a **Preferencias → Manage Design Block Libraries...**
2. Seleccionar pestaña **"Bibliotecas globales"**

### 5.2 Agregar librería de Design Blocks
Hacer clic en el botón **[+]** y agregar:

| Activo | Apodo | Ruta de la biblioteca | Formato | Opciones | Descripción |
|--------|-------|-----------------------|---------|----------|-------------|
| ✓ | `MictlanTeam` | `${MICTLAN_LIBRARY}/MictlanTeam.kicad_dblk` | KiCad | | Bloques de diseño reutilizables |

### 5.3 Guardar
Hacer clic en **"Aceptar"**

> **Nota:** Design Blocks solo están disponibles en KiCad 9.0 y superior.

---

## ✅ Paso 6: Verificar la Instalación

### 6.1 Verificar símbolos
1. Abrir **Editor de Esquemáticos**
2. Hacer clic en **"Agregar símbolo"** (o tecla `A`)
3. Buscar: `MictlanTeam`
4. Deberías ver todos los símbolos disponibles

### 6.2 Verificar footprints
1. Abrir **Editor de PCB**
2. Hacer clic en **"Agregar huella"**
3. Buscar: `MictlanTeam`
4. Deberías ver todos los footprints disponibles

### 6.3 Verificar Design Blocks (KiCad 9.0+)
1. En el **Editor de Esquemáticos**, ir a **Ver → Paneles → Design Blocks**
2. Buscar: `MictlanTeam`
3. Deberías ver los bloques de diseño disponibles

---

## 🔧 Configuración Avanzada

### Usar librería en proyectos específicos (Local)

Si prefieres tener la librería solo en un proyecto específico:

1. Copiar la carpeta `MictlanTeam-Library` dentro de tu proyecto
2. En lugar de `${MICTLAN_LIBRARY}`, usar `${KIPRJMOD}/MictlanTeam-Library`

**Ventaja:** El proyecto es portable y auto-contenido
**Desventaja:** Ocupa más espacio (duplicación)

---

## 🎨 Estructura de la Librería

```
MictlanTeam-Library/
├── README.md                    ← Este archivo
├── LICENSE                      ← Licencia MIT
├── metadata.json                ← Metadata de la librería
├── repository.json              ← Info del repositorio
├── MictlanTeam.kicad_sym        ← Símbolos esquemáticos
├── MictlanTeam.pretty/          ← Footprints/Huellas
│   ├── componente1.kicad_mod
│   ├── componente2.kicad_mod
│   └── ...
├── MictlanTeam.3dshapes/        ← Modelos 3D
│   ├── modelo1.step
│   ├── modelo2.wrl
│   └── ...
└── MictlanTeam.kicad_dblk/      ← Design Blocks (KiCad 9+)
    ├── bloque1.kicad_dblk
    ├── bloque2.kicad_dblk
    └── ...
```

---

## 🆘 Solución de Problemas

### ❌ Problema: "No se encuentran los símbolos"

**Solución:**
1. Verificar que `${MICTLAN_LIBRARY}` esté configurada correctamente
2. En KiCad → Preferencias → Configurar rutas → Verificar ruta
3. Reiniciar KiCad

### ❌ Problema: "No se encuentran los footprints"

**Solución:**
1. Verificar que la librería `MictlanTeam.pretty` esté agregada
2. Preferencias → Administrar bibliotecas de huellas → Verificar entrada
3. Verificar que la ruta `${MICTLAN_LIBRARY}/MictlanTeam.pretty` existe

### ❌ Problema: "Modelos 3D no aparecen"

**Solución:**
1. Los modelos 3D se referencian automáticamente desde los footprints
2. Verificar que `${MICTLAN_LIBRARY}` esté correctamente configurada
3. Los modelos se cargan usando rutas como: `${MICTLAN_LIBRARY}/MictlanTeam.3dshapes/modelo.step`

### ❌ Problema: "No veo Design Blocks"

**Solución:**
1. Verificar que usas **KiCad 9.0 o superior**
2. Activar panel: Ver → Paneles → Design Blocks
3. Verificar que la librería esté agregada en "Manage Design Block Libraries"

---

## 🔄 Actualizar la Librería

### Si instalaste con Git:
```bash
cd C:\Users\[TuUsuario]\Documents\KiCad\MictlanTeam-Library
git pull
```

### Si descargaste ZIP:
1. Descargar nueva versión
2. Reemplazar archivos en la carpeta
3. Reiniciar KiCad

---

## 🌐 Variables de Entorno de KiCad

Esta librería utiliza las siguientes variables:

| Variable | Descripción | Ejemplo |
|----------|-------------|---------|
| `${MICTLAN_LIBRARY}` | Ruta a la librería MictlanTeam | `C:\Users\usuario\Documents\KiCad\MictlanTeam-Library` |
| `${KIPRJMOD}` | Ruta al proyecto actual (automática) | `C:\Users\usuario\Proyectos\MiProyecto` |

---

## 📖 Uso Básico

### Agregar un símbolo al esquemático:
1. Editor de Esquemáticos → Tecla `A`
2. Buscar componente por nombre
3. Seleccionar de librería `MictlanTeam`
4. Colocar en esquemático

### Agregar un footprint al PCB:
1. Editor de PCB → Click en "Agregar huella"
2. Buscar footprint por nombre
3. Seleccionar de librería `MictlanTeam`
4. Colocar en PCB

### Usar un Design Block (KiCad 9+):
1. Editor de Esquemáticos → Ver → Paneles → Design Blocks
2. Buscar bloque en librería `MictlanTeam`
3. Arrastrar al esquemático
4. Conectar entradas/salidas

---

## 🤝 Contribuir

Si deseas contribuir con nuevos componentes:

1. Fork el repositorio
2. Agregar componentes siguiendo la estructura
3. Crear Pull Request
4. Describir los componentes agregados

**Convenciones de nomenclatura:**
- Símbolos: Usar nombres descriptivos (ej: `LM358_OpAmp`)
- Footprints: Seguir nomenclatura IPC (ej: `SOT-23-5`)
- Modelos 3D: Mismo nombre que el footprint

---

## 📧 Soporte

- **Issues:** [GitHub Issues](https://github.com/MictlanTeam/MictlanTeam-Library/issues)
- **Email:** [tu-email@ejemplo.com]
- **Documentación completa:** [Wiki del proyecto]

---

## 📄 Licencia

Esta librería está licenciada bajo **MIT License**.

Ver archivo [LICENSE](LICENSE) para más detalles.

Copyright © 2025 Mictlán Team

---

## 🎯 Resumen de Instalación Rápida

```
1. Descargar librería → C:\Users\usuario\Documents\KiCad\MictlanTeam-Library
2. KiCad → Preferencias → Configurar rutas
   └─ Agregar: MICTLAN_LIBRARY = C:\Users\usuario\Documents\KiCad\MictlanTeam-Library
3. KiCad → Preferencias → Gestionar bibliotecas de símbolos
   └─ Agregar: MictlanTeam = ${MICTLAN_LIBRARY}/MictlanTeam.kicad_sym
4. KiCad → Preferencias → Administrar bibliotecas de huellas
   └─ Agregar: MictlanTeam = ${MICTLAN_LIBRARY}/MictlanTeam.pretty
5. KiCad 9+ → Preferencias → Manage Design Block Libraries
   └─ Agregar: MictlanTeam = ${MICTLAN_LIBRARY}/MictlanTeam.kicad_dblk
6. ¡Listo! Reiniciar KiCad y comenzar a diseñar
```

---

**Última actualización:** Octubre 2025
**Versión de KiCad compatible:** 8.0.4+ (Recomendado: 9.0+)

---

⭐ Si esta librería te resulta útil, no olvides dejar una estrella en GitHub!
