# IntelliGrid AI — Energy Operations Dashboard Prototype

[![Forks](https://img.shields.io/github/forks/MokuLakshithReddy/intelligrid-control?style=flat-square)](https://github.com/MokuLakshithReddy/intelligrid-control/forks) [![Open Issues](https://img.shields.io/github/issues/MokuLakshithReddy/intelligrid-control?style=flat-square)](https://github.com/MokuLakshithReddy/intelligrid-control/issues)


A React and TypeScript dashboard prototype for exploring an industrial energy-management workflow. It brings energy-source status, demand and cost indicators, forecasts, scenario controls, carbon views, and an assistant-style interface into one navigable UI.

[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=111)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![TanStack Start](https://img.shields.io/badge/Framework-TanStack%20Start-FF4154)](https://tanstack.com/start)
[![Stars](https://img.shields.io/github/stars/MokuLakshithReddy/intelligrid-control?style=flat-square)](https://github.com/MokuLakshithReddy/intelligrid-control/stargazers)
[![Last commit](https://img.shields.io/github/last-commit/MokuLakshithReddy/intelligrid-control?style=flat-square)](https://github.com/MokuLakshithReddy/intelligrid-control/commits/main)

## What is included

The route structure exposes dashboard views for:

- Energy overview and source mix
- Live-style energy flow
- Demand and generation forecasts
- Digital-twin and scenario pages
- Carbon and executive views
- Copilot-style explanations and recommendations
- Reports and settings

The energy snapshot model currently generates **deterministic synthetic/demo telemetry** in the browser and refreshes it on a timer. Values such as demand, source output, renewable share, savings, and system health are illustrative UI data—not readings from a connected industrial plant, production SCADA system, or verified utility meter. The assistant and recommendation surfaces should also be treated as prototype UI unless separately connected to a validated model and real data source.

## Dashboard workflow

~~~mermaid
flowchart TD
    A["Open energy dashboard"] --> B["Demo telemetry generator"]
    B --> C["Energy-source snapshot"]
    C --> D["Dashboard and source mix"]
    C --> E["Energy-flow view"]
    C --> F["Forecast and scenario views"]
    D --> G["Copilot / recommendation UI"]
    E --> G
    F --> G
    G --> H["Reports and decision context"]
~~~

## Tech stack

| Layer | Technology |
|---|---|
| UI | React 19, TypeScript |
| App framework | TanStack Start / Vite |
| Styling | Tailwind CSS 4 |
| Charts and visualizations | Recharts |
| UI composition | Radix UI primitives and Lucide icons |
| Motion | Framer Motion |

## Run locally

Requirements: Node.js version supported by the installed Vite/TanStack toolchain and npm.

~~~bash
npm install
npm run dev
~~~

Create a production build with:

~~~bash
npm run build
~~~

## Evidence and current limitations

- The repository includes the dashboard and route modules listed above.
- The checked-in energy snapshot generator is synthetic; it is useful for UI demonstration, not operational monitoring.
- No independently validated forecasting accuracy, optimization benchmark, SCADA integration test, or measured cost/carbon savings result is published in this repository.
- No automated test script is currently defined in package.json.

## Why it matters

Industrial energy systems need a shared view of supply, demand, cost, storage, and emissions. This prototype explores how those concepts can be presented together so an operator can inspect the energy picture before any production integrations are attempted.
