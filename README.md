# Meu Roteiro de Cinema 🎬

Aplicação web de portfólio para descobrir sessões e montar uma agenda pessoal. Implementação própria em **HTML, CSS e JavaScript puro**, inspirada na ideia de um planejador de festivais.

> Os filmes e horários iniciais são **fictícios**. Este projeto é independente e não representa a programação oficial do Festival do Rio. Confirme sessões e ingressos nos canais oficiais.

## Funcionalidades

- Busca por título, direção e cinema; filtros por dia, gênero, favoritos e agenda.
- Favoritos e agenda salvos neste navegador com `localStorage`.
- Aviso quando duas sessões têm horários sobrepostos, considerando a duração dos filmes.
- Importação de programação em CSV e exportação da agenda em `.ics`.
- Interface responsiva, sem cadastro, servidor, dependências ou API.

## Como executar

Abra o arquivo [index.html](index.html) diretamente em um navegador moderno. Para publicar, configure **Settings → Pages → Deploy from a branch → main → / (root)** no GitHub. Após o deploy, use o endereço indicado no painel Pages.

Na aba **Importar programação**, clique em **Baixar modelo CSV**, preencha ou substitua as linhas e importe o arquivo. Cada linha equivale a uma sessão; um filme com várias sessões deve aparecer em várias linhas.

Cabeçalho obrigatório:

```csv
titulo,direcao,genero,data,hora,duracao,cinema,sinopse
```

Use data `AAAA-MM-DD`, hora `HH:MM` e duração inteira em minutos. Uma importação substitui os dados de exemplo e limpa agenda e favoritos anteriores. O CSV fica apenas no navegador.

## Habilidades demonstradas

HTML semântico, CSS com Flexbox e Grid, manipulação do DOM, eventos, filtros, validação de dados, cálculo de horários, `localStorage`, leitura de CSV e criação de arquivos para download.

## Limitações

Não há programação ao vivo nem consulta de ingressos. Os dados e escolhas ficam apenas no navegador usado; não há sincronização entre aparelhos.
