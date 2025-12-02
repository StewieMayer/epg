# Clon de Guía de Programación (EPG) de Claro Video

## 1. Descripción del Proyecto

Este proyecto tiene como objetivo desarrollar un clon funcional de la Guía de Programación Electrónica (EPG) de Claro Video. La aplicación consumirá la APIRest pública de Claro para obtener los datos de programación y los renderizará en una interfaz limpia, performante y moderna, siguiendo las mejores prácticas de desarrollo de software.

### Objetivos Principales

- **Interfaz de Usuario (UI):** Replicar la apariencia y funcionalidad del EPG de Claro Video, ofreciendo una experiencia de usuario fluida e intuitiva.
- **Rendimiento:** Asegurar un desplazamiento (scroll) y una navegación eficientes, incluso con grandes cantidades de datos, mediante técnicas de virtualización/windowing.
- **Calidad de Código:** Mantener un código limpio, escalable y bien documentado, aplicando un esquema de CI/CD desde el inicio para garantizar la integridad en cada cambio.
- **Testing:** Implementar una estrategia de pruebas unitarias y de integración para asegurar la fiabilidad de los componentes.

---

## 2. Prompt para el Asistente (Gemini)

> **Tu Rol:** Eres mi asistente de programación y copiloto. Tu misión es guiarme y asistirme en la construcción de este proyecto paso a paso, siguiendo el checklist de abajo.
>
> **Tu Tarea Principal:** Cuando yo te indique que he completado un paso, debes verificar mi trabajo. Si es correcto, actualiza el checklist en este mismo archivo `README.md` marcando la casilla correspondiente (`- [ ]` -> `- [x]`). Si hay errores o algo que mejorar, debes indicármelo.
>
> **Especificaciones del Proyecto:**
>
> - **Framework/Librerías:** React, React DOM, RTK, useImmer, HeadlessUI.
> - **Lenguaje:** TypeScript.
> - **Bundler/Compiler:** Webpack con Babel.
> - **Estilos:** Tailwind CSS con PostCSS y CSS Modules.
> - **Calidad de Código (CI):** Husky para pre-commits, ESLint para análisis estático y Prettier para formateo.
> - **Testing:** Jest y React Testing Library (RTL).
> - **Flujo de Trabajo (CD):** GitHub Actions para automatizar la verificación de PRs (lint, test, build).

---

## 3. Checklist del Proyecto

### Fase 0: Configuración e Inicialización

- [x] 1. Inicializar el proyecto con `npm init -y` y crear un archivo `.gitignore` inicial.
- [x] 2. Instalar y configurar **ESLint** para TypeScript y React.
- [x] 3. Instalar y configurar **Prettier** para un formato de código consistente.
- [x] 4. Instalar y configurar **Husky** y **lint-staged** para ejecutar ESLint y Prettier en un hook `pre-commit`.
- [x] 5. Realizar el primer commit: "feat(setup): initialize project and configure CI basics".

### Fase 1: Dependencias y Configuración del Build System

- [ ] 6. Instalar dependencias de **React** y **TypeScript** (`react`, `react-dom`, `typescript`, `@types/react`, `@types/react-dom`).
- [ ] 7. Instalar dependencias de **Webpack** (`webpack`, `webpack-cli`, `webpack-dev-server`, `html-webpack-plugin`).
- [ ] 8. Instalar **Babel** y sus presets (`@babel/core`, `babel-loader`, `@babel/preset-env`, `@babel/preset-react`, `@babel/preset-typescript`).
- [ ] 9. Crear un archivo `babel.config.js` básico.
- [ ] 10. Crear un archivo `tsconfig.json` inicial con `npx tsc --init`.
- [ ] 11. Crear un archivo `webpack.config.js` básico que pueda compilar un "Hola Mundo" en TypeScript/React.

### Fase 2: Estructura del Proyecto y Estilos

- [ ] 12. Crear la estructura de directorios: `public/index.html` y `src/index.tsx`.
- [ ] 13. Crear el componente `App.tsx` con un "Hola Mundo" y renderizarlo en `index.tsx`.
- [ ] 14. Añadir scripts `start` y `build` al `package.json` y verificar que la aplicación se ejecuta.
- [ ] 15. Instalar y configurar **Tailwind CSS** (`tailwindcss`, `postcss`, `postcss-loader`, `css-loader`, `style-loader`).
- [ ] 16. Crear archivos `tailwind.config.js` y `postcss.config.js`.

### Fase 3: Funcionalidad Principal y Testing

- [ ] 17. Configurar **Jest** y **React Testing Library** para que funcionen con TypeScript, Babel y Webpack.
- [ ] 18. Crear el primer test para el componente `App.tsx` y un script `test` en `package.json`.
- [ ] 19. Crear la estructura de componentes para el EPG (ej. `EpgGuide`, `ChannelRow`, `ProgramItem`).
- [ ] 20. Implementar el servicio de fetching de datos (API de Claro).
- [ ] 21. Integrar Redux Toolkit (RTK) para el manejo del estado de la aplicación.

### Fase 4: CI/CD y Despliegue

- [ ] 22. Crear un workflow de **GitHub Actions** (`.github/workflows/ci.yml`) que instale dependencias, ejecute el linter, los tests y el build en cada Pull Request.
- [ ] 23. (Opcional) Configurar el despliegue contínuo (CD) a una plataforma como Vercel o Netlify.
