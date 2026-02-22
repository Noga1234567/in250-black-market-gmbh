# Branch-Strategie – Black Market Software GmbH

## Gewählte Strategie: GitHub Flow

GitHub Flow ist eine einfache, schlanke Branching-Strategie, die sich besonders
für kleinere Teams eignet.

## Branch-Übersicht

| Branch | Zweck |
|---|---|
| `main` | Stabiler, produktionsreifer Code – direkte Pushes verboten |
| `feat/<name>` | Neue Features und Funktionen |
| `fix/<name>` | Bugfixes |
| `docs/<name>` | Dokumentationsänderungen |

## Regeln

- Direkte Pushes auf `main` sind **verboten**
- Jede Änderung erfolgt über einen **Feature-Branch**
- Jeder Feature-Branch wird über einen **Pull Request** in `main` gemerged
- Ein Pull Request benötigt mindestens **1 Approval** bevor er gemerged werden darf
- Branch-Namen folgen dem Schema: `feat/`, `fix/`, `docs/`
- Commit-Nachrichten folgen den [Conventional Commits](https://www.conventionalcommits.org/de/v1.0.0/)

## Workflow

1. `git checkout main`
2. `git pull origin main`
3. `git checkout -b feat/<name>`
4. Änderungen vornehmen und committen
5. `git push origin feat/<name>`
6. Pull Request auf GitHub erstellen
7. Code Review & Approval
8. Merge in `main`

## Vorteile

- Einfach und verständlich für alle Teammitglieder
- Klare Trennung zwischen stabilem Code und laufender Entwicklung
- Nachvollziehbare Git-History durch Conventional Commits
- Schutz des `main` Branches vor ungewollten Änderungen