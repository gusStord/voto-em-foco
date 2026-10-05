# Voto em Foco
Página acadêmica sobre eleições para Programação Web I.

## Executar
Abra `dist/index.html` para ler e usar o quiz. Para gravar áudio, use HTTPS ou um servidor local: `python -m http.server 8000 --directory dist` e abra http://localhost:8000. Autorize o microfone. Não é necessário npm.

## Quatro bibliotecas externas
- Darkmode.js 1.5.7: modo escuro; `new Darkmode()`, `toggle()` e `isActivated()`.
- AlertifyJS 1.13.1: diálogos de feedback do quiz; `alertify.alert()`.
- RecordRTC 5.6.2: gravação de áudio; `startRecording()`, `stopRecording()`, `getBlob()`.

Arquivos distribuídos localmente em dist/vendor, sem dependência de CDN para executar. Origem: pacotes oficiais via jsDelivr. Preservados os avisos incluídos nos arquivos. APIs nativas como getUserMedia, Blob e dialog não são contadas como bibliotecas.

## Correspondência com os documentos
- Tema livre: eleições (pedido do usuário).
- Uma página Web: index.html, com navegação por âncoras.
- 4 bibliotecas de funcionalidades diferentes: aparência, diálogos e áudio, todas citadas no PDF.
- Apresentação em slides: botão Abrir apresentação, 8 slides no navegador, navegação por botões ou setas.
- Explicar o que são, para que servem e como usar: seção O projeto, slides e comentários em app.js.
- Inclusão externa no HTML: scripts defer carregados antes de app.js, CSS do AlertifyJS no head.

## Operação e privacidade
Quiz educativo: nenhuma votação real ou coleta de preferências políticas. Áudio só permanece na memória da página; download manual para guardar. O microfone é encerrado ao parar, ao erro ou ao sair. Limite de 120 segundos. Nova gravação substitui a anterior. Nenhum cadastro, upload ou banco de dados.

## Fontes
Os links do TSE e das documentações oficiais estão na página. O site não oferece notícias nem resultados eleitorais ao vivo. Os exemplos tratam de conceitos eleitorais e são apartidários.

## Apresentação sugerida
1. Apresente o tema e a estrutura HTML/CSS/JS.
2. Alterne o modo escuro.
3. Responda as três questões, demonstrando feedback de acerto e erro.
4. Grave uma anotação, ouça, baixe e exclua.
5. Abra os slides e explique cada trecho de código.

## Limitações
Modo escuro e bibliotecas não garantem conformidade integral de acessibilidade. O projeto inclui semântica HTML, foco visível, navegação por teclado, mensagens textuais e redução de movimento. A gravação depende de permissões, microfone e suporte do navegador. WebMCP é opcional e detectado por disponibilidade; não participa dos requisitos acadêmicos.

## GSAP e tipografia
GSAP 3.13.0, com plugin ScrollTrigger da mesma biblioteca: entrada sequenciada da abertura, revelação dos cards e do gravador ao rolar. gsap.matchMedia respeita prefers-reduced-motion e reverte as animações ao mudar a preferência. Nenhum movimento contínuo ou bloqueio da rolagem.
Manrope variável nos títulos, servida localmente; Arial para texto. Arquivos Manrope via @fontsource-variable/manrope 5.2.6.
A inclusão do GSAP é um pedido posterior do usuário e torna o total quatro bibliotecas JavaScript. ScrollTrigger é plugin do GSAP.
