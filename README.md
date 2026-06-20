# immesionweek-design-ai

Guia da viagem **Design & AI Immersion Week** — San Francisco, 22 a 26 de junho de 2026.
Página única, estática e autossuficiente (fontes Itaú e logos ICTi/Hub embutidas no `index.html`).

- **Site no ar:** https://immesionweek-design-ai.vercel.app
- **Repositório:** https://github.com/mms-ops/immesionweek-design-ai
- **Vercel:** projeto `immesionweek-design-ai` (já conectado a este repo via integração GitHub).

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | O site (tudo embutido: fontes, logos, conteúdo). |
| `immersion-week.pdf` | O PDF que o botão **"Baixar este conteúdo em PDF"** entrega. |
| `vercel.json` | Config mínima da Vercel. |

## Como atualizar (IMPORTANTE)

> ⚠️ **Sempre suba os DOIS arquivos juntos no mesmo commit: `index.html` e `immersion-week.pdf`.**
> O PDF é gerado a partir do mesmo conteúdo do site. Se você atualizar só o HTML, o PDF de
> download fica desatualizado. O botão de download usa `immersion-week.pdf?v=AAAAMMDDHHMM`
> (carimbo de versão que muda a cada publicação) para o navegador nunca servir um PDF em cache.

Qualquer **push/commit na branch `main`** dispara o redeploy automático na Vercel (mesma URL).

### Opção A — pela web (sem terminal)
1. Abra `https://github.com/mms-ops/immesionweek-design-ai/upload/main`
2. Arraste **`index.html`** e **`immersion-week.pdf`** (versões novas).
3. Clique em **Commit changes** (direto na `main`). O Vercel republica sozinho.

### Opção B — pelo terminal
```bash
git add index.html immersion-week.pdf
git commit -m "atualiza guia"
git push
```

## Sincronização da agenda (Tupii)

A tarefa agendada "sync-agenda-sf" checa a agenda oficial (planotupii.online/itau-design)
algumas vezes ao dia e avisa mudanças. Quando algo mudar, regenere `index.html` + `immersion-week.pdf`
e publique pelos passos acima.
