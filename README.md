<p align="center">
  <img src=".github/assets/banner.svg" alt="Raqib — Real-time AI Analytics Dashboard" width="100%">
</p>

# Raqib — Real-time AI Analytics Dashboard

FastAPI + WebSocket + JWT + Smart Runbooks. Production-ready.

<p align="center">
  <a href="https://github.com/tibatechapp-ship-it/raqib/actions/workflows/ci.yml"><img src="https://github.com/tibatechapp-ship-it/raqib/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://github.com/tibatechapp-ship-it/raqib/actions/workflows/integration.yml"><img src="https://github.com/tibatechapp-ship-it/raqib/actions/workflows/integration.yml/badge.svg" alt="Integration"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <a href="https://github.com/tibatechapp-ship-it/raqib/releases"><img src="https://img.shields.io/github/v/release/tibatechapp-ship-it/raqib" alt="Release"></a>
  <img src="https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white" alt="Python 3.11">
  <img src="https://img.shields.io/badge/FastAPI-0.111-009688?logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/lint-ruff%20pinned-FCC21B" alt="ruff pinned">
</p>

---

## ما هو Raqib؟

لوحة تحليلات فورية للأنظمة التشغيلية: تجمع المقاييس عبر **WebSocket**، تصنّف الحالات بالذكاء الاصطناعي، وتقترح **Runbooks ذكية** كإرشاد للقراءة — مع حد أمان صارم: **Raqib لا ينفّذ أوامر أبداً**. الـDeep Links تُحوّلك إلى منصة الأتمتة لديك (AWX / Rundeck / K8s) لتقرير أنت ماذا ينفّذ.

## الميزات

- 📊 **Real-time dashboard** — مقاييس حية عبر WebSocket بمصادقة JWT
- 📚 **Smart Runbooks** — إرشادات معالجة مقروءة فقط، مربوطة بالحالات
- 🔗 **Deep Links** — قفزات مدروسة إلى منصات الأتمتة بدل تنفيذ مباشر
- 🏗️ **ADR** — قرارات معمارية موثقة في `docs/ADR/`
- 🧪 **بوابات جودة صارمة** — ruff مثبّت الإصدار كـlint gate + pytest + bandit
- 🐳 **Docker** — بيئتا تطوير وإنتاج جاهزتان (`make docker-dev` / `make docker-prod`)

## Quick start (development)

```bash
./setup.sh
source .venv/bin/activate
alembic upgrade head
uvicorn app.main:app --reload --port 8080
```

Open http://localhost:8080

## Common commands

```bash
make help           # list all targets
make dev            # run with reload
make test           # pytest
make check          # lint + format + tests + bandit
make dod            # full Definition of Done
make docker-dev     # dev stack
make docker-prod    # prod stack
```

## Security boundary

Raqib never executes commands. Runbooks are read-only guidance.
Deep Links point to your automation platform (AWX/Rundeck/K8s).

Threat model + disclosure policy: [SECURITY.md](SECURITY.md).

## لقطات

| الواجهة | الميزة المعروضة |
|---|---|
| ![Raqib banner](.github/assets/banner.svg) | لوحة تحليلات فورية بـRunbooks ذكية |

<!-- 💡 لقطات حقيقية: أضف PNG من اللوحة الحية في .github/assets/ وأدرجها هنا -->

## Documentation

| الملف | المحتوى |
|---|---|
| [AGENT_BRIEF.md](AGENT_BRIEF.md) | phase-based execution contract |
| [SECURITY.md](SECURITY.md) | threat model + disclosure |
| [CONTRIBUTING.md](CONTRIBUTING.md) | dev workflow + quality gates |
| [CHANGELOG.md](CHANGELOG.md) | release history |
| docs/RUNBOOKS.md | how to add a runbook |
| docs/ADR/ | architecture decisions |

## Issues & PRs

لدينا قوالب جاهزة: [تقرير علة](.github/ISSUE_TEMPLATE/bug_report.yml) · [اقتراح ميزة](.github/ISSUE_TEMPLATE/feature_request.yml) · [قالب PR](.github/PULL_REQUEST_TEMPLATE.md).

## License

MIT
