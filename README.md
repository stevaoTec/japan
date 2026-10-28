# YŪGEN — Japão além do óbvio

Site estático e responsivo sobre histórias, tradições, costumes, cidades, pessoas, sabores, natureza, animes e mangás do Japão.

Inclui 11 páginas, 52 descobertas, fotografias com créditos, busca geral, leitor de conteúdo, caderno de favoritos, tanzaku e uma abertura ilustrada com transição circular.

## Publicar na Vercel

1. Na Vercel, escolha **Add New → Project** e importe o repositório **stevaoTec/japan**.
2. Use a branch **main** e mantenha **Root Directory** na raiz do repositório (`./`).
3. O arquivo `vercel.json` já configura:
   - **Framework Preset:** Other.
   - **Build Command:** nenhum; deixe vazio se a interface pedir uma substituição.
   - **Output Directory:** `dist`.
4. Clique em **Deploy**.

Não são necessários banco de dados, variáveis de ambiente, instalação de pacotes ou etapa de compilação. Os arquivos de `dist/` já são o site final. Mantenha as URLs `.html`; não adicione um redirecionamento global de SPA para `index.html`, pois o projeto tem páginas próprias.

Configuração oficial: https://vercel.com/docs/project-configuration/vercel-json

## Executar localmente

Com Python instalado, rode na raiz do repositório:

```bash
python -m http.server 8000 --directory dist
```

Abra http://localhost:8000. Use um servidor HTTP, em vez de abrir o HTML como `file://`, para que a leitura dos créditos e a navegação funcionem normalmente.

## Estrutura

- `dist/index.html`: início e atlas.
- `dist/tradicoes.html`: tradições e rituais.
- `dist/historia.html`: marcos históricos, folclore e diversidade cultural.
- `dist/costumes.html`: costumes por situação.
- `dist/pessoas.html`: perfis de criadores e cientistas.
- `dist/lugares.html`: cidades e comparação de perspectivas.
- `dist/anime-manga.html`: seleção de obras e laboratório de ritmo visual.
- `dist/sabores.html`: cultura alimentar e cardápio interativo.
- `dist/natureza.html`: paisagens, festivais e tanzaku.
- `dist/caderno.html`: favoritos e anotações locais.
- `dist/creditos.html`: proveniência das imagens.
- `dist/atlas-data.js` e `dist/atlas-data.json`: conteúdo do atlas; mantenha as duas versões sincronizadas ao editar.
- `dist/entrance.js` e `dist/entrance.css`: abertura do site.
- `dist/assets/`: imagens, favicon e ilustrações.

## Créditos e privacidade

As fotografias mantêm as autorias e as licenças documentadas em `dist/photo-credits.json` e na página de créditos. Preserve essas informações ao republicar. As ilustrações de ambientação são identificadas na página de créditos.

O caderno, os selos e o desejo usam o armazenamento local do navegador. Não são enviados a um servidor e não migram automaticamente entre domínios; a versão na Vercel terá seu próprio armazenamento. Google Fonts é usado para carregar as fontes, com alternativas locais de sistema.

Este repositório contém os arquivos necessários para hospedagem independente. Não depende da hospedagem anterior e não inclui credenciais ou configurações internas do ambiente de criação.
