# FIRMES / ESCOLA APOLOGIA: guia para o Claude (leia antes de mexer)

App web de estudos para jovens cristãos brasileiros (15 a 25 anos). Dono: Theo (GitHub `contatojampro5-dot`), chama o
assistente de **"Zeus"**. Responda sempre em português, simples e direto. Theo é iniciante em GitHub: explicar passo a passo.
Theo gosta de autonomia: se ele não responder, decida e avise depois o que decidiu.

## Como o projeto é montado
- Página única `index.html` (HTML + CSS + JS puro, sem build), servida pelo GitHub Pages (`main`, raiz; `.nojekyll`).
- A mesma página também é publicada como artifact no Claude: https://claude.ai/artifact/PwjVHwgECTfGKc5svL1dq2
  (lá ela usa `window.claude` para IA (`sample`), banco (`db`) e usuário). Fora do Claude, tudo isso é opcional.
- Dois cursos no mesmo motor: `COURSES.fe` (dados em `FE`, marca "Apologia") e `COURSES.pol` (dados em `POL`,
  marca "Contracorrente"). `setCourse(id)` troca os dados; progresso separado (`apologia.v1` / `contraponto.v1`).
- Personagens e stories por curso: `FE/POL.MENTORS`, `MKEYS`, `FIGS`, `STORIES`, `RANKS`; arte SVG em `ARTMAP` (`personS`).
- Testes da tela inicial: `POLT` (eixos Economia/Costumes/Poder, 13 famílias) e `FET` (12 tradições). Cuidado com
  neutralidade: as opções devem ser ditas como quem as defende explicaria; teste com respostas aleatórias para ver viés.
  "Extrema" só com ruptura democrática ou Poder alto, igual para os dois lados.
- IA fora do Claude: `AI_URL` (vazio por enquanto) + `extAI()` imitam o `sample`; intermediário em `servidor-ia/worker.js`.
  Sem IA, o debate oferece o modo "No ChatGPT".
- Leitura guiada: `POL.LEIT.b25` (artigos do site olavodecarvalho.org). Theo pediu: **não alterar títulos nem conteúdo
  do Olavo** ("não estamos aqui para refazer o que Olavo falou").
- Fatos recentes (eleição 2026, STF, ministros) foram conferidos na web em out/2026; confira de novo antes de mudar.

## Testar
- Sintaxe: extrair o `<script>` e rodar `node --check`.
- Navegador: Playwright (Chromium já instalado), envolvendo a página num HTML simples; procurar `pageerror`.

## Regras
- Toda atualização: commit + push em `main`, com mensagem curta em português começando pela versão (ex.: `v2.5: ...`),
  e uma linha em "Versões" no `README.md`.
- Atualizar também o artifact do Claude com a mesma página.
