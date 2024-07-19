# GitHub Flow

> Esta estrategia es muy utilizada especialmente en proyectos de código abierto

GitHub Flow es un flujo de trabajo sencillo y efectivo para gestionar proyectos de software utilizando GitHub. Se basa en las siguientes etapas clave:

### 1. **Creación de una rama**
   - **Objetivo**: Trabajar en una nueva característica o solución a un problema sin afectar la rama principal (`main`).
   - **Acción**: Crear una nueva rama descriptiva basada en la rama `main`.
     ```sh
     git checkout -b nombre-rama
     ```

### 2. **Realizar commits**
   - **Objetivo**: Hacer cambios en el código de forma incremental y documentar el progreso.
   - **Acción**: Hacer commits a la nueva rama con mensajes claros y descriptivos.
     ```sh
     git add archivo-modificado
     git commit -m "Mensaje descriptivo del cambio"
     ```

### 3. **Abrir un Pull Request (PR)**
   - **Objetivo**: Proponer la integración de los cambios realizados en la nueva rama a la rama `main`.
   - **Acción**: Abrir un PR en GitHub, comparando la nueva rama con `main`, y describir los cambios y la motivación detrás de ellos.
     ```sh
     git push origin nombre-rama
     ```
     Luego, en GitHub, ir a la página de Pull Requests y crear uno nuevo.

### 4. **Revisión del Pull Request**
   - **Objetivo**: Asegurar la calidad del código mediante la revisión por otros desarrolladores.
   - **Acción**: Revisar el código, dejar comentarios, sugerencias y aprobar o solicitar cambios en el PR.

### 5. **Merge del Pull Request**
   - **Objetivo**: Integrar los cambios revisados y aprobados en la rama `main`.
   - **Acción**: Hacer merge del PR una vez que ha sido aprobado.
     ```sh
     git checkout main
     git pull origin main
     git merge nombre-rama
     ```
     En GitHub, usar el botón "Merge pull request".

### 6. **Despliegue**
   - **Objetivo**: Poner los cambios en producción de manera segura y controlada.
   - **Acción**: Desplegar desde la rama `main` a producción. Este proceso puede variar dependiendo del entorno y las herramientas de despliegue utilizadas.

### Beneficios del GitHub Flow
- **Simplicidad**: Es fácil de entender y aplicar, adecuado para proyectos de cualquier tamaño.
- **Colaboración**: Facilita la colaboración entre desarrolladores a través de revisiones de código y PRs.
- **Control de Calidad**: La revisión de PRs ayuda a mantener la calidad del código.
- **Despliegue Continuo**: Compatible con prácticas de integración y despliegue continuo (CI/CD).

### Ejemplo de Ciclo Completo

1. **Crear rama**: `git checkout -b feature/nueva-funcionalidad`
2. **Realizar cambios y commits**:
   ```sh
   git add .
   git commit -m "Añadida nueva funcionalidad"
   ```
3. **Push y PR**:
   ```sh
   git push origin feature/nueva-funcionalidad
   ```
   Luego abrir un PR en GitHub.
4. **Revisión**: Colegas revisan el PR y dejan comentarios.
5. **Merge**: Una vez aprobado, hacer merge del PR.
6. **Despliegue**: Desplegar la rama `main` actualizada a producción.

Este flujo de trabajo fomenta un desarrollo ágil y colaborativo, manteniendo un alto estándar de calidad en el código.
