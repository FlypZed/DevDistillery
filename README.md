# DevDistillery

## Descripción del Proyecto

DevDistillery es un proyecto académico desarrollado para la materia **Arquitecturas de Software (ARSW)** en la **Escuela de Ingenieros Julio Garavito**. Su objetivo es generar un entorno colaborativo para la creación y gestión de proyectos de software, integrando funcionalidades inspiradas en herramientas como **Miro, Trello y Live Share**.

### Propósito del Proyecto

Al integrar estas funcionalidades en un solo entorno, **DevDistillery** permitirá a equipos de desarrollo y planificación trabajar de manera más fluida, sin necesidad de cambiar de aplicación constantemente. Esto mejora la productividad, reduce la fricción en el flujo de trabajo y hace que la colaboración en tiempo real sea más eficiente.

## Estructura del Repositorio

El proyecto está estructurado en un repositorio principal con dos submódulos:

- **DevDistillery** (repositorio principal): [DevDistillery](https://github.com/FlypZed/DevDistillery.git)
- **DevDistillery-Backend** (submódulo para la parte backend): [DevDistillery-Backend](https://github.com/FlypZed/DevDistillery-Backend.git)
- **DevDistillery-Frontend** (submódulo para la parte frontend): [DevDistillery-Frontend](https://github.com/FlypZed/DevDistillery-Frontend.git)

## Clonación del Proyecto

Para clonar el proyecto con los submódulos incluidos:

```sh
git clone --recurse-submodules https://github.com/FlypZed/DevDistillery.git
```

Si ya clonaste el repositorio sin los submódulos, inicialízalos manualmente:

```sh
git submodule update --init --recursive
```

## Flujo de Trabajo en Git

Utilizaremos **Git Flow** de manera simplificada:

- `main`: Contiene la última versión estable.
- `develop`: Rama principal de desarrollo.
- `feature/*`: Para nuevas funcionalidades.
- `bugfix/*`: Para corregir errores en `develop`.
- `hotfix/*`: Para corregir errores críticos en `main`.

### Creación de una nueva funcionalidad

```sh
git checkout develop
git pull origin develop
git checkout -b feature/nueva-funcionalidad
```

### Fusión de una funcionalidad

```sh
git checkout develop
git pull origin develop
git merge --no-ff feature/nueva-funcionalidad
git push origin develop
git branch -d feature/nueva-funcionalidad
```

### Creación de una corrección de bug

```sh
git checkout develop
git pull origin develop
git checkout -b bugfix/error-en-x
```

## Convenciones para Commits

Usaremos el siguiente formato de commit para mantener un historial limpio y organizado:

### Estructura

```
[tipo]<id>: descripcion breve
```

### Tipos de commit

- `feat`: Nueva funcionalidad
- `fix`: Corrección de errores
- `docs`: Cambios en documentación
- `style`: Cambios de formato (sin afectar lógica)
- `refactor`: Refactorización de código
- `test`: Agregar pruebas
- `chore`: Mantenimiento o cambios menores

### Ejemplo de commit

```sh
git commit -m "[feat]123: Agregar autenticación con JWT"
```

## Actualización de Submódulos

Si el backend o frontend se actualiza, en el repositorio principal ejecuta:

```sh
git submodule update --remote --merge
git add backend frontend
git commit -m "[chore]456: Actualizar submódulos"
git push origin main
```

## Revisión de Código

Todo cambio debe pasar por una **Pull Request (PR)** en GitHub antes de fusionarse. Cada PR debe:

1. Tener un título descriptivo.
2. Explicar los cambios realizados.
3. Estar asignada a al menos un revisor.

## Para más información

Para conocer más detalles sobre el proyecto, consulta la siguiente presentación:
[DevDistillery - Presentación](https://docs.google.com/presentation/d/1Y0IjhDgLzDcFet2pHk4yCFrvMbrLyaW-XSnxp1Ju6fY/edit?usp=sharing)

---
