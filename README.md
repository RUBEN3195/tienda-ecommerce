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



git push -u origin docs/add-installation-commands

# 5. Crear Pull Request con GitHub CLI (si tienes gh instalado y autenticado)
gh pr create --title "docs: agregar comandos de instalación" --body "Agrega instrucciones para clonar y crear repo con gh CLI" --base main --head docs/add-installation-commands
