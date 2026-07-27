## Instalación y configuración local

**Clonar el repositorio y preparar el entorno (git + GitHub CLI):**

```bash
# Crear carpeta local y repositorio git
mkdir tienda-ecommerce
cd tienda-ecommerce
git init
echo "# tienda-ecommerce" > README.md
git add README.md
git commit -m "Inicializar repo con README"

# Crear repo remoto con GitHub CLI (gh)
gh repo create RUBEN3195/tienda-ecommerce --public --source=. --remote=origin --push

**Nota:** pega el bloque completo incluyendo las tres comillas invertidas (```) que delimitan el bloque de código en Markdown.

---

### 2. Cómo pegarlo usando la interfaz web de GitHub (paso a paso)

#### Pasos
1. Abre el repositorio en GitHub: `https://github.com/RUBEN3195/tienda-ecommerce`.
2. Haz clic en el archivo **README.md** en la lista de archivos.
3. Haz clic en el botón **Edit** (ícono de lápiz) en la esquina superior derecha del archivo.
4. Sitúa el cursor en el lugar donde quieres insertar el bloque (por ejemplo, debajo de un título `## Instalación`).
5. Pega el contenido del bloque (ver sección anterior).
6. En la parte inferior de la página, en **Commit changes**:
   - Selecciona **Create a new branch for this commit and start a pull request**.
   - Escribe un nombre de rama, por ejemplo: `docs/add-installation-commands`.
   - En **Commit message** deja algo descriptivo: `docs: agregar comandos de instalación y gh`.
7. Haz clic en **Propose changes**. GitHub creará la rama y abrirá un Pull Request automáticamente.

#### Capturas de pantalla sugeridas (evidencia)
- **Antes de editar:** vista del README.md (archivo abierto).
- **Editor:** pantalla con el bloque pegado en el editor (muestra el contenido).
- **Commit:** sección **Commit changes** con la opción de crear rama seleccionada y el nombre de la rama.
- **PR creada:** página del Pull Request abierta tras proponer cambios.

---

### 3. Cómo pegarlo desde tu máquina local (git + GitHub CLI)

#### Comandos completos (ejecuta en tu terminal)
```bash
# 1. Clonar el repo (si aún no lo tienes)
git clone https://github.com/RUBEN3195/tienda-ecommerce.git
cd tienda-ecommerce

# 2. Crear y cambiar a una rama nueva para la edición del README
git checkout -b docs/add-installation-commands

# 3. Abrir README.md en tu editor favorito y pegar el bloque de Markdown
# (ejemplo con nano)
nano README.md
# pega el bloque, guarda y cierra

# 4. Añadir, commitear y subir la rama
git add README.md
git commit -m "docs: agregar comandos de instalación y gh"
git push -u origin docs/add-installation-commands

# 5. Crear Pull Request con GitHub CLI (si tienes gh instalado y autenticado)
gh pr create --title "docs: agregar comandos de instalación" --body "Agrega instrucciones para clonar y crear repo con gh CLI" --base main --head docs/add-installation-commands
