# brunnofalcao.com.br

Site estático, sem build. Deploy direto na Vercel (projeto link-bio-b2n).

- `/`            → site oficial (index.html)
- `/bio`         → link da bio do Instagram (bio/index.html)
- `/assets/`     → wordmark e logo B2N

## Bio · ajustes rápidos (bio/index.html, bloco CONFIG no fim do arquivo)
- `estadoEvento`: 'inscricoes' | 'esgotado' | 'encerrado'
- `mostrarContagem`: true/false (contagem "Faltam X dias")
- `mostrarAulas`: true/false (esconde a seção Aulas)

## Pendências
- Trocar a foto de palco (hero) nas duas páginas pela definitiva no Cloudinary
- Colar Meta Pixel / GA4 no comentário no fim de cada página
