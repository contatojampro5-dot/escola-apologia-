# Firmes · Escola Apologia

App de estudos para jovens cristãos (15 a 25 anos), com dois cursos:

- **Apologia** (Cristianismo): teologia e defesa da fé, do Evangelho à apologética avançada, com C. S. Lewis e outros.
  Mestres: Pedro, Paulo, Lucas e Daniel.
- **Contracorrente** (Política): ideias da direita, história da esquerda, Constituição, história do Brasil, STF e
  como se posicionar. Personagens: Samuel, Elias, Ester, Neemias, José, Moisés, Débora e Salomão.

Tem trilha com "Você está aqui", lições em stories com minijogos, figurinhas, cards de revisão, treino de debate,
trilha de livros (com leitura guiada de *O mínimo que você precisa saber para não ser um idiota*), a aba Tempo
(presidentes, quem é quem, STF) e dois testes na tela inicial: "Onde você se encaixa hoje?" e
"Com qual tradição cristã você mais se parece?".

## Abrir

- **No celular:** https://contatojampro5-dot.github.io/escola-apologia-/
- No iPhone: abra no Safari → Compartilhar → **Adicionar à Tela de Início** para virar um "app".
- **Versão no Claude** (debate com IA dentro do app, usando a conta Claude de cada um):
  https://claude.ai/artifact/PwjVHwgECTfGKc5svL1dq2
- O progresso fica salvo no aparelho.

## IA nos debates

- No link do GitHub, sem configuração, o debate abre no ChatGPT gratuito já com o personagem e as regras.
- Para a IA funcionar **dentro do site**, de graça: siga [`servidor-ia/GUIA.md`](servidor-ia/GUIA.md)
  (Gemini + Cloudflare Worker) e mande o endereço do Worker para o Zeus colocar no app.

## Arquivos

- `index.html`: o app inteiro, numa página só.
- `manifest.webmanifest`, `*.png`: ícones e dados para "Adicionar à Tela de Início".
- `servidor-ia/`: o intermediário da IA gratuita (`worker.js`) e o passo a passo (`GUIA.md`).
- `.nojekyll`: faz o GitHub Pages servir os arquivos como estão.

## Versões

- **v2.4.1**: leitura guiada com os nomes originais dos temas do livro (181 artigos).
- **v2.4**: leitura guiada de *O mínimo* (artigos originais no site do autor, com marcação de lidos).
- **v2.3**: testes na tela inicial (espectro político e tradição cristã).
- **v2.2**: IA própria grátis no site (Gemini via Cloudflare Worker).
- **v2.1**: debate no ChatGPT gratuito.
- **v2.0**: Firmes: Apologia + Contracorrente juntos, personagens e stories na Política.
- **v1**: Escola Apologia (primeira versão).
