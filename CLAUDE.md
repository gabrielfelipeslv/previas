# Prévias de site (previa.gabrielfelipe.tech)

Repositório das prévias que o Gabriel mostra para empresas de Uberaba (MG) que não têm site ou têm um site antigo.
Ele pede pelo Telegram, muitas vezes na rua, na frente do dono da empresa: "Prévia, faz um site para a Padaria
São José, rua tal, Instagram @..." A prévia precisa ficar pronta rápido, bonita no celular e com cara de site de
verdade daquela empresa. Cada prévia é uma pasta na raiz: `<nome-da-pasta>/index.html`.

Publicado pelo GitHub Pages em https://previa.gabrielfelipe.tech/<nome-da-pasta>/ . Quem publica é o atalho do
Hub (commit e push só da pasta da prévia). Você nunca roda git.

## Como fazer

1. **Entenda o pedido.** Nome da empresa, ramo, bairro/endereço, Instagram ou site atual, telefone/WhatsApp e o que
   o Gabriel disser sobre ela. Se faltar algo, pesquise (WebSearch/WebFetch): site atual, Instagram, Google, listas
   públicas. Use só informação pública da EMPRESA. Não invente: o que não achar fica genérico ("Seg a sáb, consulte
   horários") e você diz no relatório o que faltou.
2. **Nome da pasta:** o nome da empresa em minúsculas, sem acento, com hífen (`padaria-sao-jose`). Se já existir uma
   pasta com esse nome de outra empresa, acrescente o bairro (`padaria-sao-jose-centro`). Pedido de ajuste na mesma
   empresa: edite a pasta dela.
3. **Monte a página** (um `index.html` só, com CSS dentro; imagens opcionais na mesma pasta):
   - Celular primeiro (é lá que o dono vai abrir). Rápida, sem framework, sem build.
   - Seções de site de pequena empresa: topo com nome e chamada clara; o que a empresa faz/serviços ou produtos;
     diferenciais; como chegar (endereço e link "Abrir no mapa" do Google Maps pela busca do endereço); horário;
     botão grande de WhatsApp (`https://wa.me/55DDDNUMERO?text=...`) quando houver o número; rodapé.
   - Visual com cara do ramo (cores, tipografia do Google Fonts, ícones em SVG ou emoji). Bonito de verdade: é isso
     que vende. Nada de cara de modelo genérico.
   - Imagens: não copie foto do Instagram, do Google ou de outro site (direito autoral). Use composição com CSS,
     gradientes, formas, ícones e emojis; se precisar de foto, deixe um bloco elegante "Sua foto aqui".
   - Textos curtos, em português do Brasil, com acentuação correta, no tom do ramo. Sem depoimento, nota, número de
     clientes ou prêmio inventado.
   - Obrigatório no `<head>`: `<meta name="robots" content="noindex, nofollow">` (a prévia não pode aparecer no Google)
     e `<meta name="viewport" content="width=device-width, initial-scale=1">`.
   - Obrigatório no fim da página, discreto: "Prévia criada por Gabriel Felipe (gabrielfelipe.tech), sem vínculo com
     <empresa>. Informações públicas, sujeitas a confirmação." com link para https://gabrielfelipe.tech .
   - Sem formulário que envie dados, sem script de rastreio, sem chamada a API.
4. **Publique:** `node <atalho de publicar> <nome-da-pasta>`. Ele recusa página sem noindex ou sem o aviso de prévia,
   arquivo grande (máx. 3 MB cada, 8 MB no total) e nome inválido: corrija e publique de novo.
5. **Teste:** depois de 1 a 2 minutos, `node <atalho de testar> /<nome-da-pasta>/` deve dar 200.
6. **Relatório:** o link, o que você pôs na página, o que não achou e precisa ser confirmado com o dono.

## Nunca

- Mexer em pasta de outra prévia, no `index.html`, `CNAME`, `robots.txt` ou `.nojekyll` da raiz.
- Usar logotipo, marca ou foto de terceiros; fingir ser a empresa (o aviso de prévia é obrigatório).
- Colocar dado pessoal de alguém (CPF, telefone pessoal de funcionário): só o contato público da empresa.
- Contatar a empresa: quem fala com o dono é o Gabriel.
