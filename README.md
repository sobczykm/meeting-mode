# meeting-mode

Jeden skrót przed spotkaniem / live demo: czysty, „bezpieczny” ekran. Drugi raz przywraca stan sprzed.

## Status

**pomysł** — nic nie zaimplementowane.

## MVP

- Ukrycie ikon na pulpicie (`defaults write com.apple.finder CreateDesktop -bool false` + restart Findera, albo okno-zasłona nad pulpitem).
- Włączenie Focus „Nie przeszkadzać” (Shortcuts: `shortcuts run "…"` — skróty tworzone raz przez użytkownika).
- Ukrycie / zamknięcie wybranych aplikacji (Slack, Messenger, poczta) — lista w ustawieniach.
- Opcjonalnie: neutralna tapeta, ukrycie paska menu, wybór mikrofonu.
- Zapamiętanie stanu i pełne przywrócenie po wyłączeniu.

## Notatki techniczne

- Focus nie ma publicznego API → przez aplikację Skróty (`/usr/bin/shortcuts`).
- Zamykanie aplikacji: `NSRunningApplication.terminate()`; ukrywanie: `.hide()`.

## Decyzje / TODO

- [ ] ukrywać czy zamykać aplikacje (domyślnie ukrywać)
- [ ] integracja z meeting-timer (start trybu = start timera)?
