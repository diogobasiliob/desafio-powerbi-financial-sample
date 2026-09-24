# Relatório de Vendas e Lucratividade — Financial Sample

Desafio de projeto do módulo de Power BI da [DIO](https://www.dio.me/). A proposta era
replicar duas páginas construídas durante o curso e criar uma terceira de forma autônoma,
exercitando a construção de visuais, o uso de dicas de ferramenta e a publicação do relatório.

O arquivo `.pbix` neste repositório contém o relatório completo, com as três páginas.

---

## A base de dados

`Financial Sample.xlsx` — amostra financeira da Microsoft, também usada nos materiais do curso.

| | |
|---|---|
| Linhas | 700 |
| Período | setembro/2013 a dezembro/2014 |
| Países | 5 (Canadá, França, Alemanha, México, EUA) |
| Segmentos | 5 (Government, Small Business, Channel Partners, Midmarket, Enterprise) |
| Produtos | 6 |

Uma particularidade do arquivo original: a coluna de vendas se chama `" Sales"`, **com um
espaço no início do nome**. Por isso ela aparece no topo da lista de campos do Power BI, fora
da ordem alfabética. Não é erro de digitação — é assim na fonte.

---

## As três páginas

### Página 1 — Produtos e Segmentos

| Visual | Campos |
|---|---|
| Pizza | `Product` × Soma de ` Sales` |
| Área | `Product` × Soma de `Sale Price` |
| Colunas agrupadas | Eixo: hierarquia `Date` (Ano › Mês) · Valor: Soma de ` Sales` · Legenda: `Segment` |
| Segmentação de dados | Hierarquia `Date` (Ano › Mês) |

### Página 2 — Países e Lucro

| Visual | Campos |
|---|---|
| Cartão | Soma de ` Sales` |
| Cartão | Soma de `Units Sold` |
| Pizza | `Country` × Soma de `Profit` |
| Colunas agrupadas | Eixo: hierarquia `Date` (Ano › Mês) · Valor: Soma de `Profit` |
| Colunas agrupadas | Eixo: `Country` · Valor: Soma de ` Sales` |

### Página 3 — Distribuição Geográfica

Página de criação autoral, com os três visuais pedidos no desafio.

| Visual | Campos |
|---|---|
| Mapa — Volume de vendas por país | Local: `Country` · Tamanho: Soma de ` Sales` · **Dica de ferramenta:** Soma de `Units Sold` |
| Mapa — Lucro por país | Local: `Country` · Tamanho: Soma de `Profit` |
| Pizza — Participação no lucro por segmento | Legenda: `Segment` · Valor: Soma de `Profit` |

Os títulos dos visuais foram reescritos em todo o relatório. O padrão automático do Power BI
descreve o cálculo (*Soma de Profit por Country*); os títulos deste relatório descrevem a
informação (*Lucro por país*).

---

## Números do relatório

| Indicador | Valor |
|---|---|
| Sales | US$ 118.726.350,26 |
| Gross Sales | US$ 127.931.598,50 |
| Descontos concedidos | US$ 9.205.248,24 |
| COGS | US$ 101.832.648,00 |
| Profit | US$ 16.893.702,26 |
| Margem líquida | 14,23% |
| Unidades vendidas | 1.125.806 |

---

## Achados da análise

**O lucro não segue a receita.** Os Estados Unidos lideram em vendas, com US$ 25,03 milhões
e 21,1% do total, mas ficam em quarto lugar em lucro, com 17,7%. A França vende menos —
US$ 24,35 milhões — e lucra mais, 22,4%. É esse descolamento que justifica a página 3 ter
**dois** mapas em vez de um: sozinho, o mapa de vendas esconde onde a empresa ganha dinheiro.

| País | Sales | % das vendas | Profit | % do lucro |
|---|---|---|---|---|
| Estados Unidos | 25,03 mi | 21,1% | 3,00 mi | 17,7% |
| Canadá | 24,89 mi | 21,0% | 3,53 mi | 20,9% |
| França | 24,35 mi | 20,5% | 3,78 mi | 22,4% |
| Alemanha | 23,51 mi | 19,8% | 3,68 mi | 21,8% |
| México | 20,95 mi | 17,6% | 2,91 mi | 17,2% |

**Um segmento destrói valor.** *Enterprise* fechou o período com prejuízo de US$ 614.545,62 —
margem de −3,1% sobre US$ 19,61 milhões vendidos. É o segundo maior em receita e o único
negativo em lucro.

**A concentração é extrema.** *Government* responde por 67,4% de todo o lucro, com margem de
21,7%. *Channel Partners* tem a melhor margem da base, 73,1%, mas sobre uma receita pequena
de US$ 1,80 milhão — é o segmento com maior potencial de escala.

| Segmento | Sales | Profit | % do lucro | Margem |
|---|---|---|---|---|
| Government | 52,50 mi | 11,39 mi | 67,4% | 21,7% |
| Small Business | 42,43 mi | 4,14 mi | 24,5% | 9,8% |
| Channel Partners | 1,80 mi | 1,32 mi | 7,8% | 73,1% |
| Midmarket | 2,38 mi | 0,66 mi | 3,9% | 27,7% |
| Enterprise | 19,61 mi | −0,61 mi | −3,6% | −3,1% |

---

## Nota técnica: o gráfico de pizza e o valor negativo

Gráficos de pizza não representam valores negativos. Como o segmento *Enterprise* tem lucro
negativo, o Power BI omite essa fatia da pizza de lucro por segmento — e recalcula os
percentuais sobre a soma dos segmentos positivos, US$ 17,51 milhões, em vez do lucro real da
empresa, US$ 16,89 milhões.

O efeito é visível no relatório: *Government* aparece com **65,04%** do lucro, quando sua
participação verdadeira é **67,4%**.

O visual foi mantido porque o desafio o especifica. Em um relatório de produção, a escolha
correta seria um gráfico de barras ou de colunas, que acomoda o valor negativo e preserva a
leitura correta. Registro a limitação aqui porque escolher a forma errada sabendo o motivo é
diferente de escolher por acidente.

---

## Como abrir

Baixe o arquivo `.pbix` e abra no [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
O modelo de dados já vem carregado — não é necessário reconectar a fonte.

## Tecnologias

Power BI Desktop · Power Query · Microsoft Excel

## Referência

Material original do curso: [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst)

## Autor

Diogo — Bootcamp Power BI + IA · DIO
