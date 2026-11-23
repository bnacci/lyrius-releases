# Coleção oficial do Lyrius

Temas completos em `themes/*.lyst`; wallpapers originais em `wallpapers/`;
miniaturas leves em `previews/`; configurações iniciais em `sources/`.
O app consulta `catalog.json` ao clicar em **Buscar novidades**. O site
consulta a mesma coleção, com cache de uma hora. Depois de aprovado e
mesclado um PR, o conteúdo aparece sem publicar outra versão do app.

## Criar ou atualizar um tema

1. No Lyrius, crie o tema, teste claro/escuro e a leitura no telão e exporte
   pelo menu **Exportar como .lyst**. Inclua fundo, variantes e apenas fontes
   cuja licença permita redistribuição. Aumente a versão em atualizações.
2. Faça um fork de `bnacci/lyrius-releases` e clone seu fork.
3. No código-fonte do app, registre o pacote no checkout da coleção:

   ```sh
   flutter test --concurrency=2 tool/content/register_theme_test.dart --dart-define=PACKAGE=/caminho/tema.lyst --dart-define=SLUG=meu-tema --dart-define=NAME_EN="My theme" --dart-define=PREVIEW=/caminho/miniatura.jpg --dart-define=CONTENT_ROOT=/caminho/lyrius-releases/content
   ```

   Use o mesmo slug nas atualizações. O comando verifica o pacote completo,
   preserva autor/licença/fontes/variantes, estabelece o ID oficial e atualiza
   tamanho e SHA-256. Após alterar o manifesto a assinatura anterior não é
   reutilizada. O canal oficial vem do catálogo revisado neste repositório;
   não representa assinatura verificada do Marketplace.
4. Acrescente o JSON de configuração em `sources/` se também desejar permitir
   revisão do desenho em texto. O `.lyst` é o conteúdo instalado pelo app.
5. Abra um PR com o `.lyst`, miniatura, fonte editável e `catalog.json`.
   Descreva mudanças visuais, autoria e direitos de redistribuição.

Mantenha as versões anteriores dos arquivos para que um download em andamento
continue válido. Não altere o conteúdo de um arquivo já publicado; aumente a
versão e crie outro nome. O app não faz downgrade automático. Cópias pessoais
não são sobrescritas; atualizações de temas offline preservam os IDs usados
por músicas antigas. Remover a atualização restaura a versão offline.

## Wallpapers

Renomeie com slug descritivo, coloque o original em `wallpapers/` e uma prévia
até 640×360 em `previews/`. Cadastre `kind: wallpaper`, ID
`org.lyrius.wallpaper.<slug>`, nomes `pt`/`en`, versão SemVer, caminhos relativos,
`size` em bytes, `sha256` hexadecimal e `bundled: false` em `catalog.json`.
Não há código executável nos temas. Pacotes têm limite de 64 MB no catálogo.
Os dois wallpapers offline ficam no instalador; as outras imagens são baixadas
apenas quando solicitadas. Catálogo e miniaturas são públicos.

## Revisar o PR

- Confira leitura, alinhamento, acentos e contraste da letra em fundos claros.
- Confira autoria/licenças e não inclua fontes proprietárias.
- Confira hash, tamanho, nomes seguros e versão; abra o pacote no app.
- Teste a instalação, a atualização e uma cópia editada pelo usuário.
- Não use `pull_request_target` para executar código de contribuições.

O fluxo editorial é independente dos binários e releases do aplicativo.
