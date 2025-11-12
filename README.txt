
CON_News_v6.0_UNIFICADO_INTEL
============================
Pronto para GitHub Pages.

Resumo:
- index.html: painel (login adm/adm).
- assets/app_v6.js: busca unificada (client-side via rss2json), classificação automática (Acidente, Roubo, Furto, Interdição, Porto, Sindicato, Internacional, Outros), mapas e export.
- data/mock_data.json: dados de teste caso feeds falhem.
- map.html: mapa em tela cheia que carrega do cache localStorage.

Notas importantes:
- Browser-side RSS requests may be limited. The script uses https://api.rss2json.com to convert RSS to JSON (helps with CORS) but has rate limits. For stable production, deploy a Cloudflare Worker proxy and update rss2jsonFetch to call your worker.
- CSV export includes UTF-8 BOM so Excel usually opens correctly. If accents appear incorrectly, open via Excel Data -> From Text/CSV and choose UTF-8.
- To publish: push repository to GitHub and enable Pages (branch main). After publishing, open the site and click Atualizar to fetch live feeds.

Login: adm / adm
