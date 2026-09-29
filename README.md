# Meu Festival do Rio 2026 🎬

Planejador de sessões do Festival do Rio, feito com **HTML, CSS e JavaScript puro** para demonstrar desenvolvimento front-end e tratamento de dados.

**Fonte dos dados:** [programação oficial de todas as sessões](https://www.festivaldorio.com.br/br/programacao/todas-as-sessoes), consultada em **28/09/2026**. A página oficial indicava **931 sessões entre 1 e 14 de outubro de 2026**. O projeto é independente e não tem vínculo com a organização. Confira eventuais mudanças, ingressos e condições de acesso no site oficial antes de ir ao cinema.

## Funcionalidades

- Catálogo com título, gênero, mostra, data, horário, duração, sala e link para o filme na fonte oficial.
- Busca por título ou cinema; filtros por dia, gênero, favoritos e agenda.
- Favoritos e agenda guardados no navegador com `localStorage`.
- Aviso de conflito entre sessões sobrepostas, considerando a duração do filme.
- Importação opcional de CSV e exportação da agenda em `.ics`.
- Interface responsiva, sem cadastro, servidor, dependências ou API.

## Como executar

Abra [index.html](index.html) diretamente em um navegador moderno. A programação oficial consultada está incorporada ao arquivo, então ele funciona mesmo sem servidor. Para publicar pelo GitHub Pages, configure **Settings → Pages → Deploy from a branch → main → / (root)**. O endereço final será mostrado no painel Pages.

Na aba **Importar programação**, você pode baixar o modelo CSV, editar as linhas e carregar outra programação. Cada linha equivale a uma sessão; uma nova importação substitui os dados atuais e limpa agenda e favoritos. Use o botão **Restaurar programação oficial** para voltar à cópia consultada em 28/09/2026.

Cabeçalho CSV: `titulo,direcao,genero,data,hora,duracao,cinema,sinopse`. Direção e sinopse podem ficar vazias. Data deve ser `AAAA-MM-DD`, hora `HH:MM` e duração um número inteiro de minutos.

## Habilidades demonstradas

HTML semântico, CSS com Flexbox e Grid, manipulação do DOM, eventos, filtros, validação de CSV, cálculo de sobreposição de horários, persistência com `localStorage` e geração de arquivos de calendário.

## Limitações

Os horários são uma **cópia consultada em 28/09/2026**, sem atualização automática. A listagem oficial usada não fornecia direção nem sinopse para cada sessão, por isso esses campos não são inventados. As escolhas ficam somente no navegador e não são sincronizadas entre aparelhos.

Ao atualizar da primeira versão oficial, as sessões e favoritos que continuam na programação são preservados no navegador. Sessões retiradas pelo Festival deixam a agenda.
