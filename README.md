# Simulador do 2º turno 2026

Simulador interativo da eleição presidencial de 2026 (Lula × Flávio Bolsonaro). Para cada um dos 12 candidatos do 1º turno, e para quem não votou em ninguém, você escolhe quanto dos eleitores foi para Flávio, quanto foi para Lula e quanto deixou de votar. O placar do 2º turno é recalculado na hora e comparado com o resultado real.

É uma página única (`index.html`), sem build e sem dependências. Só as fontes vêm do Google Fonts; sem internet, a página usa fontes do sistema.

## Publicar no GitHub Pages

1. Crie um repositório e envie o `index.html` (e este README) para a raiz.
2. No repositório, vá em **Settings → Pages**.
3. Em **Source**, escolha **Deploy from a branch**, a branch `main` e a pasta `/ (root)`. Salve.
4. Em alguns minutos o site fica em `https://<seu-usuario>.github.io/<nome-do-repositorio>/`.

Para testar no computador, basta abrir o `index.html` no navegador.

## Dados

- **1º turno:** votos dos 12 candidatos, brancos, nulos e abstenção, da totalização do TSE com 100% das seções (via Estadão Conteúdo). "Não votou em ninguém" soma abstenção, brancos e nulos.
- **2º turno real:** Lula 64.256.232 votos e Flávio 59.826.041 (TSE, via Bloomberg Línea).
- **Botão "Pesquisa AtlasIntel":** pesquisa AtlasIntel/Bloomberg de 13 a 18/out/2026, 4.998 entrevistas, margem de erro de 1 ponto, registro TSE BR-02418/2026. Os percentuais foram conferidos em InfoMoney, IstoÉ Dinheiro e BPMoney.
  - Eleitores de Cury: 42,4% Flávio, 52,1% Lula.
  - Eleitores de Renan Santos: 33,5% Flávio, 31,9% Lula.
  - Eleitores de Caiado: 69,8% Flávio, 24,5% Lula.
  - A pesquisa não separa Zema nem os candidatos menores: todos estão no grupo "outros" (61,3% Flávio, 30,7% Lula), e o simulador aplica esse valor a cada um deles.
  - A margem de 1 ponto vale para a amostra inteira, não para esses subgrupos, que são bem menores.

Os dados ficam no objeto `D`, no início do `<script>` do `index.html`. Para conferir os números oficiais: https://resultados.tse.jus.br

Os cenários são hipóteses: o voto é secreto e ninguém sabe exatamente para onde cada eleitor foi.
