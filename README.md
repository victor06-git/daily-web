# Ritual diario

Web estática (un solo `index.html`, sin dependencias ni build) con tu rutina diaria:

- Checklist de 7 hábitos con racha y mapa anual estilo GitHub
- Noticias más votadas de la semana en Hacker News (en directo, con filtros IA / Datos / Startups / Open source) y fuentes recomendadas
- Meditación guiada con temporizador y 3 técnicas de respiración
- Lección diaria (IA, Big Data, Cloud, startups, hackathons) con mini reto y diario
- Frase en inglés del día, generador de ideas de startup y enlaces a hackathons
- Recordatorio diario en tu calendario (.ics) y avisos del navegador
- Exportar / importar el progreso (se guarda en `localStorage`)

Para cambiar tu nombre, edita `const NAME = "Victor";` en el `<script>`.

## Deploy en Vercel

**Opción 1 — Desde GitHub (recomendada)**

```bash
cd ritual-diario
git init && git add . && git commit -m "Ritual diario"
gh repo create ritual-diario --public --source=. --push   # o créalo en github.com
```

Luego en [vercel.com/new](https://vercel.com/new) → *Import* el repo → Framework Preset: **Other** → *Deploy*. No hace falta build command ni output directory. Cada `git push` vuelve a desplegar.

**Opción 2 — Vercel CLI**

```bash
npm i -g vercel
cd ritual-diario
vercel          # primera vez: preview
vercel --prod   # producción
```

## Notas

- El progreso vive en el navegador donde lo uses: si cambias de móvil a portátil, usa *Exportar* / *Importar*.
- Los avisos del navegador solo saltan con la web abierta; para un aviso fiable cada día, usa *Añadir a mi calendario*.
