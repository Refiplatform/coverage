# 🧪 Coverage Template Workflow — Refiplatform

Plantilla central para ejecutar **tests y gate de calidad** en todos los repositorios de **Refiplatform**.

---

## 🚀 ¿Qué hace?

- Ejecuta los tests de Jest con cobertura (`npm test -- --coverage`)
- Sube el reporte de cobertura como artefacto
- Implementa un **Quality Gate**: si los tests fallan, bloquea el deploy

---

## 🧩 Cómo usarlo en tus repositorios

En cualquier repositorio de Refiplatform, crea el archivo:

`.github/workflows/coverage.yml`

con este contenido:

```yaml
name: Reutilizar workflow de cobertura

on:
  push:
    branches: [main]

jobs:
  coverage:
    uses: Refiplatform/coverage-template/.github/workflows/coverage.yml@main

