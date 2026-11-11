# devops-ci-app

Учебное Flask-приложение для практической работы № 10.

CI: Pylint → pytest → Docker build → smoke-test → GHCR.

Публикация образа выполняется только из `main`. В Pull Request выполняются
проверки без push.

- health endpoint: `/health`;
- сведения о службе: `/`;
- образ: `ghcr.io/mikle-kekich/devops-ci-app`;
- основной workflow: `.github/workflows/ci.yml`.

Зависимости приложения находятся в `app/requirements.txt`, инструменты
разработки — в `requirements-dev.txt`. В производственный образ входят
только зависимости приложения.
