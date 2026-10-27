# Simulador do 2º turno 2026

Simulador interativo da eleição presidencial de 2026 (Lula × Flávio Bolsonaro). Para cada candidato do 1º turno você escolhe quanto dos eleitores dele foi para Flávio, quanto foi para Lula e quanto deixou de votar. O placar do 2º turno é recalculado na hora, para o Brasil e para cada estado, e comparado com o resultado real.

É uma página única (`index.html`), sem build e sem dependências. Só as fontes vêm do Google Fonts; sem internet, a página usa fontes do sistema.

## Publicar no GitHub Pages

1. Crie um repositório e envie o `index.html` (e este README) para a raiz.
2. No repositório, vá em **Settings → Pages**.
3. Em **Source**, escolha **Deploy from a branch**, a branch `main` e a pasta `/ (root)`. Salve.
4. Em alguns minutos o site fica em `https://<seu-usuario>.github.io/<nome-do-repositorio>/`.

Para testar no computador, basta abrir o `index.html` no navegador.

## Dados

- Votos do 1º e do 2º turno por estado, compilados de veículos que reproduzem a totalização do TSE: Estadão Conteúdo, Bloomberg Línea, Lado a Lado, Radar da Eleição e Metrópoles. Brancos, nulos e "demais candidatos" de RS, RO, RR, SC, SE e TO no 1º turno foram estimados pela diferença com o total nacional.
- "Não votou no 1º turno" soma abstenção, brancos e nulos.
- O botão **Pesquisa AtlasIntel** usa a pesquisa AtlasIntel/Bloomberg de 13 a 18/out/2026 para os eleitores de Cury, Renan Santos, Caiado e Zema.
- Por estado, o simulador aplica os mesmos percentuais em todo lugar.

Os dados ficam no objeto `D`, no início do `<script>` do `index.html`. Para conferir os números oficiais: https://resultados.tse.jus.br

Os cenários são hipóteses: o voto é secreto e ninguém sabe exatamente para onde cada eleitor foi.
