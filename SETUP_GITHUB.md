# 🚀 Guía de Setup del Repositorio GitHub

## Opción 1: Crear desde GitHub.com (Recomendado)

### Paso 1: Crear el Repositorio en GitHub

1. Ve a [github.com](https://github.com) y haz login
2. Click en el botón **"+"** → **"New repository"**
3. Configuración:
   - **Repository name:** `PowerBI-COIIG-2026`
   - **Description:** `Curso Power BI - Colegio de Ingenieros de Galicia - Abril 2026`
   - **Visibility:** ✅ Public
   - **Initialize repository:**
     - ❌ NO marcar "Add a README file" (ya lo tenemos)
     - ❌ NO añadir .gitignore (ya lo tenemos)
     - ❌ NO añadir license
4. Click en **"Create repository"**

### Paso 2: Preparar la Estructura Local

Crea esta estructura de carpetas en tu ordenador:

```
PowerBI-COIIG-2026/
├── Dataset/
│   └── (aquí pones Contoso_Sales.xlsx)
├── Recursos/
│   ├── Fondos/
│   └── (aquí los temas y plantillas)
├── Sesion1/
├── Sesion2/
├── Sesion3/
├── Sesion4/
├── README.md (el que te he creado)
└── .gitignore (el que te he creado)
```

### Paso 3: Subir al Repositorio

#### Opción A: Usando GitHub Desktop (MÁS FÁCIL)

1. Descarga [GitHub Desktop](https://desktop.github.com/)
2. Abre GitHub Desktop
3. Click en **"File"** → **"Add Local Repository"**
4. Selecciona la carpeta `PowerBI-COIIG-2026`
5. Si dice "not a git repository", click en **"create a repository"**
6. Añade todos los archivos (aparecerán en la izquierda)
7. Escribe un mensaje: `📦 Configuración inicial del curso`
8. Click en **"Commit to main"**
9. Click en **"Publish repository"**
10. Selecciona tu cuenta de GitHub
11. ✅ Desmarca "Keep this code private"
12. Click en **"Publish repository"**

#### Opción B: Usando Git por Terminal

```bash
# 1. Navega a la carpeta del proyecto
cd /ruta/a/PowerBI-COIIG-2026

# 2. Inicializa git
git init

# 3. Añade todos los archivos
git add .

# 4. Haz el primer commit
git commit -m "📦 Configuración inicial del curso"

# 5. Conecta con GitHub (sustituye TU_USUARIO)
git remote add origin https://github.com/JuanNaya/PowerBI-COIIG-2026.git

# 6. Cambia a la rama main
git branch -M main

# 7. Sube los archivos
git push -u origin main
```

---

## Opción 2: Usar GitHub Web Interface (Para archivos pequeños)

1. Crea el repositorio vacío en GitHub (Paso 1 de arriba)
2. Click en **"uploading an existing file"**
3. Arrastra y suelta los archivos
4. Añade mensaje: `📦 Configuración inicial del curso`
5. Click en **"Commit changes"**

**⚠️ Limitación:** Solo sirve para archivos pequeños (<25MB)

---

## 📝 Añadir Archivos Después de Cada Sesión

### Usando GitHub Desktop:

1. Añade los archivos .pbix a la carpeta correspondiente (Sesion1, Sesion2...)
2. Abre GitHub Desktop
3. Verás los archivos nuevos en la izquierda
4. Escribe un mensaje: `📊 Archivos Sesión 1 añadidos`
5. Click en **"Commit to main"**
6. Click en **"Push origin"**

### Usando Git por Terminal:

```bash
# 1. Añade los archivos nuevos
git add Sesion1/

# 2. Commit
git commit -m "📊 Archivos Sesión 1 añadidos"

# 3. Sube a GitHub
git push
```

---

## 🔗 Verificar que Funciona el Link de Descarga

Una vez subido el archivo `Contoso_Sales.xlsx` a la carpeta `Dataset/`, el link será:

```
https://github.com/JuanNaya/PowerBI-COIIG-2026/raw/main/Dataset/Contoso_Sales.xlsx
```

**Prueba el link** en un navegador incógnito para verificar que descarga correctamente.

---

## 📦 Archivos a Subir ANTES del Curso

**Prioridad Alta:**
- ✅ README.md
- ✅ .gitignore
- ✅ Dataset/Contoso_Sales.xlsx
- ✅ Recursos/Tema_PowerBI.json (cuando lo tengamos)
- ✅ Recursos/Plantilla_Presentacion.pptx (cuando lo tengamos)

**Durante el curso:**
- 📊 Sesion1/Contoso_Sesion1.pbix
- 📊 Sesion2/Contoso_Sesion2.pbix
- 📊 Sesion3/Contoso_Sesion3.pbix
- 📊 Sesion4/Contoso_Sesion4_Final.pbix

---

## 🆘 Solución de Problemas

### "File too large" (archivo muy grande)

Los archivos .pbix pueden ser grandes. Si supera 100MB:

**Solución:** Usar [Git LFS](https://git-lfs.github.com/)

```bash
# Instalar Git LFS
git lfs install

# Configurar .pbix para LFS
git lfs track "*.pbix"

# Añadir y commit
git add .gitattributes
git commit -m "🔧 Configurar Git LFS para archivos .pbix"
git push
```

### "Permission denied" al hacer push

Necesitas autenticación. Usa **GitHub Desktop** o configura un [Personal Access Token](https://github.com/settings/tokens).

---

## ✅ Checklist Final

- [ ] Repositorio creado en GitHub
- [ ] README.md subido
- [ ] .gitignore subido
- [ ] Estructura de carpetas creada
- [ ] Dataset de Contoso subido
- [ ] Link de descarga probado y funciona
- [ ] Presentación HTML actualizada con el link correcto

---

**¿Necesitas ayuda?**  
📧 juannaya@naban.es
