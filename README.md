# Espaço YO — site de demonstração

Projeto HTML/CSS/JavaScript estático, pronto para publicar no **Render Static Site**.

## Conteúdo deste pacote

- `public/index.html`: site completo, com cinco imagens ilustrativas incorporadas para evitar espaços vazios.
- `public/favicon.svg`: ícone visual "YO" provisório.
- `public/robots.txt`: solicita que buscadores não indexem a demonstração.
- `render.yaml`: configuração opcional para implantação pelo Render Blueprint.

## Publicar no Render (pelo painel)

1. Descompacte o arquivo ZIP.
2. Crie um **repositório novo** no GitHub, por exemplo `espaco-yo-demo`, e envie **o conteúdo da pasta `espaco_yo_render`** para a raiz do repositório (o `render.yaml` e a pasta `public` devem ficar na raiz).
3. No painel do Render, selecione **New > Static Site** e conecte o repositório.
4. Use estes campos:
   - **Build Command:** `echo "Site estatico: nenhuma compilacao necessaria"`
   - **Publish Directory:** `public`
   - **Root Directory:** deixe em branco (se os arquivos estiverem na raiz).
5. Crie o Static Site e, após o deploy terminar, abra o endereço `*.onrender.com` atribuído pelo Render.

### Alternativa: Blueprint

No Render, selecione **New > Blueprint**, escolha o mesmo repositório e deixe o Render ler o `render.yaml`. O arquivo configura o site estático e os cabeçalhos de não indexação.

## Testar antes de publicar

Abra `public/index.html` no navegador, ou execute `python -m http.server 8000 -d public` dentro da pasta do projeto e acesse `http://localhost:8000`.

## Importante: conteúdo e autorização

- Esta versão **é uma demonstração não oficial**. O rodapé informa esse caráter.
- As cinco fotos de reserva são **ilustrativas** e não representam trabalhos reais do Espaço YO. O JavaScript tenta carregar imagens públicas do Booksy; se isso falhar, mantém as imagens ilustrativas.
- A exibição pública e o uso definitivo de marca, fotos e eventuais depoimentos devem ser aprovados pela proprietária. Para o site oficial, use arquivos originais autorizados, preferencialmente hospedados no próprio projeto.
- **Agendar** e **Reservar** continuam abrindo a página geral do Espaço YO no Booksy. Nenhum serviço fica selecionado automaticamente nesta versão.
- Textos, valores de serviços, equipe e dados do negócio devem ser confirmados antes de usar como site oficial.
- O site **não exige banco de dados**, serviço web Python ou Node. Fontes do Google e tentativas de fotos do Booksy dependem de internet; as imagens de reserva ficam dentro do HTML.
- A indicação `noindex` ajuda a evitar indexação, mas **não torna o site privado**. Quem tiver a URL poderá acessá-lo.
- A autoria/assinatura comercial da **sua empresa** pode ser incluída depois que você fornecer o nome e logotipo. Nenhum nome de empresa foi inventado.

## Atualizar o site

Edite `public/index.html`, envie a alteração ao GitHub e o Render poderá publicar automaticamente a nova versão. Para publicar oficialmente, substitua os materiais provisórios e revise a identidade visual conforme a aprovação da proprietária.

## Fontes de configuração

Render Static Sites: https://render.com/docs/static-sites
Render Blueprints: https://render.com/docs/blueprint-spec
