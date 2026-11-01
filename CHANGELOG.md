# Changelog

## 0.6.0 (2026-11-01)

- The plugin has its own repository (it was `adapters/astrbot/` in [memory-core](https://github.com/JikunLiu101/memory-core),
  whose history it keeps), so AstrBot's plugin market can install it. The library comes from PyPI as
  `memory-core-lib`.
- A public face for other plugins: `where`, `owner_spaces`, `snapshot`, `provider_id`, `persona`, `owner_console`
  (with the attributes `core`, `owner_ids`, `owner_title`); the rest may change between versions.
- Prompt caching: the system prompt is laid out by how often each part changes, and what is new among the
  abilities goes with the user's message (`<abilities_news>`), so the list only changes when an ability comes or
  goes.
- Market metadata: Chinese name 记忆核心, `astrbot_version`, `support_platforms`, tags.

Earlier versions: see memory-core's [CHANGELOG](https://github.com/JikunLiu101/memory-core/blob/main/CHANGELOG.md)
(0.1.0–0.5.0).
