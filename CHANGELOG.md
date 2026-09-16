# Changelog

## 1.0.5 — 2026-09-16

- Made an agent-controlled real browser the mandatory first recovery route for
  CodeWeavers 403, robots, timeout, empty-result, and no-match failures.
- Added an explicit pause for CAPTCHA, login, or other human verification;
  those gates are neither a search miss nor compatibility evidence.
- Moved exact-page search behind the browser attempt instead of allowing it to
  replace that attempt.

## 1.0.4 — 2026-09-16

- Added a structured `query_log` to collector and recovery results: stages,
  elapsed time, source outcome, retrieval gate, and recovery handoff.
- Made ordinary compatibility checks verdict-first. Tutorial and community
  walkthrough discovery now run only when the user asks for play instructions,
  a workaround, or provides a tutorial link.
- Tightened recovery to one authorized retry and one exact CodeWeavers recovery
  pass; repeated DNS failures, archive hunting, and title-guess loops stop.
