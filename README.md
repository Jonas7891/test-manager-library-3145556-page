# test-manager-library-3145556-page

> **Prueba técnica · Ficha ADSO 3145556**: sitio público estático de presentación de *Manager Library* (T-23).

## Reglas que cumple

| Regla | Cómo |
|---|---|
| No habla con la API | HTML y CSS puros: no hay JavaScript ni `fetch` |
| No expone datos personales | Ningún dato de socios ni de bibliotecarios (`data-model.md` §7) |
| Se ve bien en móvil y escritorio | Rejilla `auto-fit` y tipografía con `clamp()`; probado a 375 px y a 1280 px |

## Cómo se abre

- Local: abrir `index.html` en el navegador, sin servidor y sin la API.
- Publicación: GitHub Pages → *Settings → Pages → Deploy from a branch → `main` / root*.

## Evidencia (T-23)

```bash
grep -c "fetch\|<script" index.html   # 0: no llama a la API
```
