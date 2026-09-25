# Painel de Vendas Porsche

Dashboard interativo em HTML, feito a partir de uma base de **100 vendas de veículos Porsche** (EUA, 2024–2027). O arquivo roda sozinho no navegador, com os dados e as imagens embutidos e sem dependências para instalar.

**Ver online:** `https://gilberto-r.github.io/dashboard_porsche_sales/`

## Perguntas de negócio

1. **Quais os principais modelos vendidos por cidade?** Ranking dos 10 modelos mais vendidos e tabela com o modelo líder de cada cidade ou estado.
2. **Qual ano-modelo mais saiu em cada período?** Gráfico de barras por ano-modelo e matriz que cruza o ano da venda com o ano-modelo.
3. **O que é popular em cada praça?** Leituras automáticas que se recalculam conforme os filtros: linha líder, concentração geográfica, faixa de entrada, forma de pagamento e idade do carro.

## Filtros

Modelo (ou a linha inteira) · ano-modelo · cidade · forma de pagamento · período da venda · incluir ou não as vendas canceladas.

## Tratamento dos dados

Os dados de origem vieram "sujos" e foram padronizados antes da análise:

- **Datas:** 24 datas não existem no calendário (ex.: 30/02) e aparecem como "Sem data". Outras 23 são posteriores à data da análise e estão marcadas com `*`.
- **Preços e quilometragem:** eram texto livre (`$121k`, `68.900 dollars`, `KM 18,900`) e foram convertidos para número. Quilômetros foram passados para milhas.
- **Categorias:** modelo, cidade, estado, forma de pagamento e status de entrega foram padronizados.
- **Canceladas:** as 7 vendas canceladas ficam fora dos totais por padrão.

Com 79 cidades para 100 vendas, as leituras por cidade são indicativas. Para ver padrões, use a visão por estado.

## Stack

HTML, CSS e JavaScript puros, sem frameworks. Tipografia Archivo (Google Fonts).

## Créditos das imagens

As fotos dos veículos são de fontes de terceiros, em sua maioria do Porsche Newsroom (uso editorial). Este é um projeto de estudo e portfólio, sem vínculo com a Porsche AG.
