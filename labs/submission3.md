# Lab 3 Submission
**Platform: GitHub Actions**

## Task 1 — First GitHub Actions Workflow (6 pts)

### Workflow file location:
`.github/workflows/learn-github-actions.yml`

### Key concepts learned:
- **Jobs**: набор шагов, которые выполняются на одном runner'е
- **Steps**: отдельные команды или действия внутри job'а
- **Runners**: виртуальные машины, на которых выполняются workflow'ы (ubuntu-latest, windows-latest, macos-latest)
- **Triggers**: события, которые запускают workflow (push, workflow_dispatch, pull_request и др.)

### What triggered the workflow:
Workflow запустился автоматически после push в ветки main или feature/lab3.

### Link to successful run:
[ВСТАВИТЬ ССЫЛКУ НА RUN В ACTIONS TAB]

### Analysis of workflow execution process:
При push в репозиторий GitHub автоматически запускает workflow. Runner (ubuntu-latest) скачивает код, выполняет каждый шаг по очереди. Если какой-то шаг падает (exit code не 0), workflow останавливается и помечается как failed.

## Task 2 — Manual Trigger + System Information (4 pts)

### Changes made to workflow file:
Добавлен `workflow_dispatch:` под секцией `on:`. Это позволяет запускать workflow вручную из UI GitHub.

### How to trigger manually:
1. Зайти в Actions → Выбрать workflow "Learn GitHub Actions"
2. Нажать "Run workflow" → Выбрать ветку → Нажать "Run workflow"

### Gathered system information:
[ВСТАВИТЬ ВЫВОД ИЗ STEP "Gather system information"]

### Comparison of manual vs automatic triggers:
При ручном запуске (`workflow_dispatch`) вы контролируете процесс, но нужно не забыть его активировать, а при автоматическом (`push`) он срабатывает при каждом пуше, но может запускаться слишком часто.
### Analysis of runner environment:
GitHub Actions runner на ubuntu-latest предоставляет: 2-core CPU, 7GB RAM, 14GB SSD. Включает предустановленные инструменты: Git, Docker, Node.js, Python и др.
