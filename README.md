# brunnofalcao.com.br · B2N

Site estático, sem build. Deploy pelo GitHub (brunnofalcao/link-bio-b2n, branch main) → Vercel.

    index.html        site oficial · /
    bio/index.html    link da bio · /bio
    assets/b2n/       logos B2N (7 nav e rodapé da bio · 8 rodapé do site · 10 topo da bio · símbolo NN no herói)
    assets/           favicons, apple-touch-icon, og.jpg (1200×630)
    vercel.json       URLs limpas, /bio/ → /bio, cache dos assets
    robots.txt · sitemap.xml

## Ajustes sem mexer no layout (bloco CONFIG no fim de cada arquivo)

Site (index.html)
- eventBanner   true/false · faixa do Health Influence Day no topo
- heroCta       'mentorias' | 'palestras' · ordem dos botões do herói
- depoimentos   true quando os 3 depoimentos reais estiverem preenchidos
- fotos         hero · sobre · palco (URL; '' esconde sobre e palco)
- formEndpoint  FormSubmit → contato@scienceplay.com. Se falhar, abre o WhatsApp da equipe com os dados
- whatsapp      número da equipe, só dígitos com DDI

Bio (bio/index.html)
- estadoEvento  'inscricoes' | 'esgotado' (lista de espera) | 'encerrado' (some o bloco)
- mostrarContagem, mostrarAulas

## Rastreamento
Cole GTM (ou Pixel + GA4) no comentário do <head> das duas páginas.
Todo CTA tem data-track; o clique dispara BioClick / SiteClick no Pixel e bio_click / site_click no GA4.
Envio do formulário dispara Lead (Pixel) e generate_lead (GA4).

## Fotos (assets/fotos/ · ver LEIA-ME.txt na pasta)
- brunno-hero.jpg   herói do site e da bio · 4:5 · 1600x2000
- brunno-sobre.jpg  Sobre · 3:2 · 1600x1066
- brunno-palco.jpg  Palestras · 21:9 · 2400x1030
Enquanto o arquivo não existir, o espaço fica preto.

## Pendências
- Subir as 3 fotos
- Ativar o FormSubmit: o 1º envio do formulário manda um e-mail de ativação para contato@scienceplay.com (clicar no link). Até lá o envio cai no WhatsApp.
- Mais depoimentos: modelo comentado no HTML, seção Depoimentos
- Após 04/11: estadoEvento 'encerrado' na bio e eventBanner false no site
