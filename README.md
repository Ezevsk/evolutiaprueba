# Evolutia Prueba - Playwright Test Project

## Estructura del Proyecto
```
.
├── .github/
│   └── workflows/          # Configuración de GitHub Actions
├── src/
│   ├── locators/          # Selectores y localizadores
│   ├── pageObject/        # Page Objects
│   ├── test/             # Tests
│   ├── test-data/        # Datos para pruebas
│   └── utils/            # Utilidades
├── .env                  # Variables de entorno
├── .gitignore           # Archivos ignorados por git
├── package.json         # Configuración del proyecto
├── playwright.config.ts # Configuración de Playwright
└── README.md           
```

## Requisitos Previos
- Node.js (versión LTS)
- npm

## Instalación
1. Clonar el repositorio:
```bash
git clone https://github.com/Ezevsk/evolutiaprueba.git
```

2. Instalar dependencias:
```bash
npm install
```

3. Instalar navegadores de Playwright:
```bash
npx playwright install
```

## Scripts Disponibles

| Comando | Descripción |
|---------|-------------|
| `npm run test` | Ejecuta todas las pruebas en modo headless |
| `npm run test:headed` | Ejecuta las pruebas con el navegador visible |
| `npm run test:ui` | Abre el modo UI de Playwright |
| `npm run test:debug` | Ejecuta las pruebas en modo debug |

## Configuración
- El proyecto está configurado para ejecutar pruebas en Chromium por defecto
- Los reportes se generan en formato HTML
- Las pruebas se ejecutan en paralelo
- Configurado con GitHub Actions para CI/CD

## Estructura de los Tests
Los tests se encuentran en el directorio `src/test/` y siguen el patrón `.spec.ts`

## GitHub Actions
El proyecto incluye integración continua con GitHub Actions que:
- Se activa en push a main/master
- Se activa en pull requests a main/master
- Ejecuta las pruebas
- Guarda los reportes como artefactos

## Reportes con Allure

Para generar y ver reportes con Allure:

1. Ejecutar las pruebas:
```bash
npm run test
```

2. Generar el reporte:
```bash
npm run allure:generate
```

3. Abrir el reporte en el navegador:
```bash
npm run allure:open
```
