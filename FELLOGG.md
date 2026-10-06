# Fellogg

En rad per fel. Skriv medan du minns hur du gjorde.

| Nr | Vad stod i loggen? | Lokalt eller på GitHub? | Hur tog du reda på orsaken? | Hur löste du det? |
|----|--------------------|-------------------------|-----------------------------|-------------------|
| 1 | Invalid workflow file – YAML syntax error | GitHub | Jag såg felet i Actions och VS Code visade att raden med `uv sync --frozen` hade fel indrag | Jag flyttade raden så att den låg i samma kolumn som de andra stegen under `steps:` |
| 2 | Unable to find lockfile at `uv.lock`, but `--frozen` was provided | GitHub | Jag öppnade det röda steget `uv sync --frozen` i Actions och läste felmeddelandet | Jag tog bort `--frozen` så att kommandot blev `uv sync` |
| 3 | F401 `os` imported but unused | GitHub | Jag öppnade det röda Ruff-steget i Actions och såg att felet pekade på `src/miniforecast/baseline.py` rad 3 | Jag tog bort den oanvända raden `import os` |
| 4 | `tests/test_baseline.py` would be reformatted | GitHub | Jag öppnade det röda `ruff format --check`-steget och såg vilken fil som inte följde formatteringen | Jag körde `uv run ruff format src tests` så Ruff formaterade koden |




Fortsätt tabellen med fler rader vid behov.
