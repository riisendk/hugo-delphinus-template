# Hugo Delphinus Template

En Hugo template baseret på AU Delphinus Designsystem.

## Kom i gang

1. Installer Hugo (https://gohugo.io/installation/)
2. Kør udviklerserver:
   ```bash
   hugo server -D
   ```
3. Åbn http://localhost:1313 i din browser

## Struktur

```
hugo-delphinus-template/
├── archetypes/          # Templates til nyt indhold
├── content/             # Sideindhold (Markdown)
├── layouts/
│   ├── _default/        # Basis layouts
│   ├── partials/        # Genbrugelige komponenter
│   └── shortcodes/      # Hugo shortcodes
└── static/
    ├── css/style.css    # Delphinus CSS
    ├── js/app.js        # Delphinus JavaScript
    └── assets/          # Logoer og ikoner
```

## Konfiguration

Rediger `hugo.toml` for at ændre:
- Site titel og beskrivelse
- Navigation menu
- Sprog (da/en)

## Tilgængelige Shortcodes

### Button
```markdown
{{</* button url="/link" text="Klik her" */>}}
{{</* button url="/link" text="Sekundær" type="dimmed" */>}}
```

### Callout
```markdown
{{</* callout type="info" */>}}Information her{{</* /callout */>}}
{{</* callout type="warning" */>}}Advarsel{{</* /callout */>}}
{{</* callout type="error" */>}}Fejl{{</* /callout */>}}
{{</* callout type="success" */>}}Succes{{</* /callout */>}}
```

### Grid Layout
```markdown
{{</* row */>}}
  {{</* col size="6" */>}}Venstre kolonne{{</* /col */>}}
  {{</* col size="6" */>}}Højre kolonne{{</* /col */>}}
{{</* /row */>}}
```

## Delphinus CSS Klasser

Se memory-filen `au-delphinus-designsystem.md` for fuld reference, eller besøg https://delphinus.au.dk

### Ofte brugte klasser

| Klasse | Brug |
|--------|------|
| `.button` | Primær knap |
| `.button--dimmed` | Sekundær knap |
| `.text--stamp` | Kategori-label |
| `.text--intro` | Introduktionstekst |
| `.content-container` | Indholdscontainer |
| `.theme--dark` | Mørkt tema |
| `.theme--normal` | Lyst tema |

## Opret nyt indhold

```bash
hugo new nyheder/min-nyhed.md
```

## Build til produktion

```bash
hugo --minify
```

Output gemmes i `public/` mappen.
