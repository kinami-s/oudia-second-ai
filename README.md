# Railway Diagram Studio AI

This repository provides the initial project skeleton for a railway timetable planning and optimization system based on the specification in the attached design document.

## Structure

```text
.
├── README.md
├── docs/
│   ├── architecture.md
│   ├── product-spec.md
│   └── roadmap.md
├── apps/
│   └── web/
│       ├── package.json
│       ├── vite.config.ts
│       ├── tsconfig.json
│       ├── index.html
│       └── src/
│           ├── main.tsx
│           ├── App.tsx
│           └── styles.css
├── core/
│   ├── __init__.py
│   ├── domain/
│   │   ├── __init__.py
│   │   ├── models.py
│   │   └── time.py
│   ├── validation/
│   │   ├── __init__.py
│   │   ├── engine.py
│   │   ├── rules.py
│   │   └── report.py
│   ├── optimization/
│   │   ├── __init__.py
│   │   ├── objectives.py
│   │   ├── candidates.py
│   │   └── optimizer.py
│   ├── ai/
│   │   ├── __init__.py
│   │   ├── interfaces.py
│   │   ├── parser.py
│   │   └── planner.py
│   └── io/
│       ├── __init__.py
│       ├── schema.py
│       └── json_store.py
├── tests/
│   ├── test_time.py
│   ├── test_validation.py
│   └── test_ai_contracts.py
├── .gitignore
├── pyproject.toml
└── package.json
```

## Minimal stack

- Web UI: TypeScript + React + Vite
- Core logic: Python
- Validation and optimization: deterministic engine with structured reports
- AI integration: typed interfaces and structured commands

## Getting started

### Python core

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pytest -q
```

### Web app

```bash
cd apps/web
npm install
npm run dev
```

## Notes

This is intentionally a design-first skeleton. The system is structured so that the domain model, validation engine, optimization layer, and AI interfaces can be developed independently while adhering to the specification.
