# Prompt Generator Rules

Offizielle Ruleset-Quelle für den privaten Prompt Generator.

Dieses Repository enthält **nur Daten-/Promptregeln**, keinen ausführbaren Code.

## Aktuelle Version

`2026.08.2`

Der Prompt Generator liest `latest.json`, prüft Versionsnummer und SHA256 des
Ruleset-Pakets und installiert nur kompatible JSON-Regelpakete.

## Struktur

- `latest.json` – Online-Update-Manifest
- `releases/<version>/manifest.json` – internes Ruleset-Manifest
- `releases/<version>/core.json` – allgemeine Promptregeln
- `releases/<version>/targets.json` – Zielsystem- und Arbeitsmodusregeln
- `releases/<version>/prompt-ruleset-<version>.zip` – installierbares Paket

## Sicherheitsmodell

Das NAS akzeptiert keine `.py`, `.js`, Shell-Skripte oder andere ausführbare Dateien
als Ruleset-Update. SHA256-Prüfsummen, App-Kompatibilität und Adapter-Schema werden
vor Aktivierung geprüft; ein Rollback-Punkt wird automatisch erzeugt.
