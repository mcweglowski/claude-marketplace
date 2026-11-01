# claude-marketplace

Marketplace `mawg-marketplace` z pluginami Claude Code Marcina Węglowskiego. To repozytorium zawiera tylko katalog (`.claude-plugin/marketplace.json`); każdy plugin ma własne repozytorium.

| Plugin | Repozytorium | Opis |
| --- | --- | --- |
| `statusbar` | [mcweglowski/claude-statusbar-mawg](https://github.com/mcweglowski/claude-statusbar-mawg) | konfigurowalny status bar z widżetami i układami |
| `session-gauge` | [mcweglowski/claude-session-gauge](https://github.com/mcweglowski/claude-session-gauge) | pasek nad promptem: kontekst, limity, koszt, cache i handoff |

## Instalacja

W sesji Claude Code w terminalu:

```
/plugin marketplace add mcweglowski/claude-marketplace
/plugin install session-gauge@mawg-marketplace
/plugin install statusbar@mawg-marketplace
```

Z powłoki:

```bash
claude plugin marketplace add mcweglowski/claude-marketplace
claude plugin install session-gauge@mawg-marketplace
```

Po zmianach w katalogu: `claude plugin marketplace update mawg-marketplace`.

W aplikacji desktopowej: + obok pola promptu, Plugins, Add marketplace z `mcweglowski/claude-marketplace`, potem Add plugin.

Plugin z prywatnego repozytorium zainstalują tylko osoby z dostępem do niego na GitHubie i skonfigurowanym dostępem git do github.com.

## Dodanie pluginu

Dopisz wpis do `plugins` w `.claude-plugin/marketplace.json`:

```json
{
  "name": "nazwa-pluginu",
  "description": "Co robi",
  "source": { "source": "github", "repo": "mcweglowski/repozytorium-pluginu" }
}
```

`name` musi się zgadzać z `name` w `.claude-plugin/plugin.json` pluginu. Sprawdź katalog poleceniem `claude plugin validate .claude-plugin/marketplace.json`.
