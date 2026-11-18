# Amaral de Almeida — Odontologia Estética

Landing page da clínica do **Dr. Matheus Amaral de Almeida** (CRO/SP 165256): odontologia estética e harmonização orofacial, com a campanha de Black Friday.

Site estático (HTML + CSS), sem build e sem dependências.

**Prévia:** https://matdev96.github.io/drMatheusAmaral/

## Estrutura

```
index.html            Página principal
404.html              Página de erro (noindex)
assets/css/style.css  Estilos
assets/img/           Imagens (WebP) + og-image.jpg (compartilhamento)
assets/icons/         Favicon e ícones de app
favicon.ico
robots.txt            Regras para buscadores
sitemap.xml           Mapa do site
llms.txt              Resumo do site para IAs (ChatGPT, Claude, Perplexity…)
site.webmanifest      Manifesto (ícones, cor do tema)
vercel.json           Cabeçalhos de cache e segurança (se publicar na Vercel)
.nojekyll             Necessário para o GitHub Pages servir os arquivos como estão
```

## SEO já aplicado

- `<title>` e meta description, `canonical`, `robots`, `lang="pt-BR"`
- Open Graph + Twitter Card com imagem 1200×630 (prévia no WhatsApp)
- Dados estruturados (JSON-LD): `Dentist`, `Person` (com CRO) e `WebSite`
- Um único `h1`, hierarquia de títulos, `alt` em todas as imagens, link "pular para o conteúdo"
- Imagens em WebP com `width`/`height`, `loading="lazy"` e pré-carregamento da foto principal
- Fontes com `preconnect` e `display=swap`
- Links do WhatsApp com mensagem pronta por serviço (`?text=`)

## Pendências de conteúdo

- `[DATA DE ENCERRAMENTO]` da promoção (index.html)
- `[RUA, NÚMERO]` (index.html e llms.txt). Quando tiver, completar `streetAddress` e `postalCode` no JSON-LD
- Fotos dos casos reais (ver abaixo)
- Apresentação do Dr. Matheus na seção "Sobre"

## Casos reais (antes e depois)

As fotos ficam em `assets/img/casos/`, no formato `caso-N-antes.webp` e `caso-N-depois.webp` (proporção 4:3, cerca de 800×600). Hoje são imagens provisórias: basta substituir os arquivos mantendo os nomes, e ajustar título, descrição e `alt` de cada caso no `index.html`.

Antes de publicar cada caso (Resolução CFO 196/2019):
- termo de consentimento (TCLE) assinado pelo paciente;
- só o diagnóstico (antes) e o resultado final (depois), sem etapas do procedimento;
- sem instrumentais, equipamentos ou materiais visíveis (ex.: afastador labial);
- sem promessa de resultado.

## Trocar para o domínio definitivo

Hoje a URL oficial é `https://matdev96.github.io/drMatheusAmaral`. Quando o cliente tiver domínio, substitua esse endereço em
`index.html`, `sitemap.xml`, `robots.txt` e `llms.txt`, e o caminho `/drMatheusAmaral/` em `404.html` por `/`.
Depois, cadastre o site no Google Search Console e envie o `sitemap.xml`.

## Atenção — publicidade odontológica

O Código de Ética Odontológica (CFO) proíbe anúncios com preços e modalidades de pagamento. Confirme com o cliente antes de divulgar a versão com valores.
