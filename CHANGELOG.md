# Changelog

## Unreleased

- **Missed diaries are caught up.** It only ever looked at yesterday, so after AstrBot had been off for two days
  the last day she talked was never written. Now the finished days of the last `diary_catch_up_days` (7) are
  written oldest first, each from that day's experiences and the day before's diary only, and the self-image is
  rewritten once, after the last, so nothing that came later gets in. A late one is written as such ("现在是 X，
  你在补写 Y 那天的日记：程序被关了"), marked in `diary/<date>.md`, and she keeps a thought in the owner's private
  chat that she caught up on it. A day she was not running at all is no longer written up as "nobody came".
- Needs memory-core-lib with `mark_awake`, `missed_days` and `why_late` (the next release after 0.6.0).

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
