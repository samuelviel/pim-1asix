# Projecte Intermodular · 1r ASIX

Materials públics del mòdul de **Projecte Intermodular** del primer curs del CFGS
d'Administració de Sistemes Informàtics en Xarxa.

El lloc es genera amb [MkDocs](https://www.mkdocs.org/) i el tema
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), i es publica
automàticament a GitHub Pages.

---

## Posada en marxa

### 1 · Crea el repositori a GitHub

Crea un repositori **públic** anomenat `pim-1asix` i puja este contingut:

```bash
git init
git add .
git commit -m "Materials del mòdul de Projecte Intermodular 1r ASIX"
git branch -M main
git remote add origin https://github.com/EL-TEU-USUARI/pim-1asix.git
git push -u origin main
```

### 2 · Canvia les tres referències al teu usuari

Al fitxer `mkdocs.yml`, substituïx `usuari-github` pel teu nom d'usuari de GitHub:

```yaml
site_url: https://EL-TEU-USUARI.github.io/pim-1asix/
repo_url: https://github.com/EL-TEU-USUARI/pim-1asix
```

I també a l'apartat `extra.social`, al final del fitxer.

### 3 · Activa GitHub Pages

A la pàgina del repositori: **Settings → Pages → Build and deployment → Source:
GitHub Actions**.

A partir d'ací, cada `git push` a `main` torna a publicar el lloc automàticament.
El trobaràs a `https://EL-TEU-USUARI.github.io/pim-1asix/`.

---

## Treballar-hi en local

```bash
pip install -r requirements.txt
mkdocs serve
```

Obri <http://127.0.0.1:8000>. El lloc es recarrega sol cada vegada que guardes un fitxer.

Per a comprovar que tot compila abans de pujar-ho:

```bash
mkdocs build --strict
```

---

## Estructura

```
.
├── mkdocs.yml                 Configuració del lloc i navegació
├── requirements.txt
├── .github/workflows/         Publicació automàtica a GitHub Pages
└── docs/
    ├── index.md               Portada
    ├── modul/                 Presentació, RA, metodologia, avaluació, calendari
    ├── projecte/              Elecció del repte, quadern de seguiment, lliurables
    ├── up1/ … up7/            Les set unitats de programació
    ├── recursos/              Eines, plantilles i preguntes freqüents
    └── stylesheets/
```

Cada unitat és un únic fitxer `index.md` que conté els continguts didàctics, l'activitat
avaluable i la seua rúbrica.

---

## Com editar el contingut

| Vull… | Fitxer |
|---|---|
| Canviar dates de lliurament | `docs/modul/calendari.md` |
| Canviar pesos o criteris d'avaluació | `docs/modul/avaluacio.md` |
| Modificar una activitat o la seua rúbrica | `docs/up<N>/index.md` |
| Afegir o llevar una plantilla | `docs/recursos/plantilles.md` |
| Canviar el menú de navegació | Secció `nav:` de `mkdocs.yml` |
| Canviar colors | `theme.palette` a `mkdocs.yml` i `docs/stylesheets/extra.css` |

Les etiquetes de colors dels resultats d'aprenentatge s'escriuen així:

```html
<span class="ra ra1">RA1</span>
```

---

## Pendent de personalitzar

Abans de publicar-ho a l'alumnat, revisa:

- [ ] L'usuari de GitHub a `mkdocs.yml` (tres llocs)
- [ ] Les **dates concretes** de lliurament a `docs/modul/calendari.md`
- [ ] El nom del centre i el professorat a `docs/index.md` i `docs/modul/index.md`
- [ ] La **fitxa de cas tancat** que s'esmenta a `docs/projecte/index.md` i a la FAQ,
      per si vols preparar-ne una per a qui no trobe organització
- [ ] Un `favicon.png` a `docs/assets/` si en vols un de propi

---

## Llicència

Materials publicats sota llicència
[Creative Commons BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.ca):
es poden reutilitzar i adaptar citant l'autoria i mantenint la mateixa llicència.
