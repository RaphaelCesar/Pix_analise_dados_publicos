# PIX no Brasil: Crescimento, Comportamento e Concentração Geográfica

Análise exploratória do crescimento do PIX no Brasil (nov/2020 a jun/2026), usando dados públicos do Banco Central. O projeto investiga quatro frentes: evolução do volume transacionado, mudança no perfil de uso (ticket médio, pessoa física vs. jurídica), o impacto de mudanças regulatórias nos indicadores de fraude, e a distribuição geográfica do PIX pelo território nacional.

## Perguntas de negócio

1. Como evoluiu o volume e a quantidade de transações PIX desde o lançamento?
2. O PIX mudou de perfil de uso ao longo do tempo (grandes transferências vs. uso cotidiano)?
3. Pessoa física ou pessoa jurídica lidera o crescimento do PIX?
4. O aumento nos indicadores de fraude reflete mais golpes ou mudança na forma de medir?
5. O PIX está concentrado geograficamente, ou distribuído de forma equilibrada pelo país?

## Principais achados

- O volume mensal de PIX saltou de praticamente zero (nov/2020) para mais de R$ 3 trilhões/mês (2026).
- O ticket médio caiu de ~R$ 870 para uma estabilização em torno de R$ 400–450, indicando transição de "grandes transferências pontuais" para "uso cotidiano".
- O volume pago por pessoa jurídica ultrapassou o de pessoa física por volta de 2023 e a diferença só cresce.
- O salto nas contestações de fraude a partir de out/2025 coincide com a obrigatoriedade do botão de contestação digital (Resolução BCB nº 493/2025) — reflete facilidade de reportar, não necessariamente mais fraude real.
- Em **valor financeiro**, o Sudeste concentra cada vez mais o PIX (50% → 55% do total nacional, 2021–2026). Mas em **número de transações**, o Brasil está se desconcentrando: Nordeste e Norte ganharam participação relevante (Nordeste: 20% → 27%) — evidência de adoção popular crescente fora do eixo Sul-Sudeste.

## Fontes de dados

Todos os dados são públicos, coletados via API oficial do Banco Central (Olinda — Dados Abertos do Pix):

- `EstatisticasTransacoesPix` — volume e quantidade de transações mensais, segmentadas por PF/PJ, região, idade, natureza e finalidade.
- `EstatisticasFraudesPix` — contestações, devoluções e indicadores do Mecanismo Especial de Devolução (MED).
- `TransacoesPixPorMunicipio` — transações por município e UF.

Base URL: `https://olinda.bcb.gov.br/olinda/servico/Pix_DadosAbertos/versao/v1/odata`

## Ferramentas

- Python (pandas, requests, matplotlib, plotly)
- Google Colab
- API pública do Banco Central do Brasil (Olinda)

## Estrutura do repositório

```
├── notebooks/
│   └── Projeto_Pix.ipynb      # notebook principal com toda a análise
├── README.md
└── requirements.txt
```

## Como reproduzir

1. Clone o repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/pix-analise-dados-publicos.git
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Abra `notebooks/Projeto_Pix.ipynb` no Jupyter ou Google Colab e execute as células em ordem. Não é necessária nenhuma chave de API — os dados são públicos e a coleta é feita em tempo real.

## Autor

Raphael — em transição de carreira para análise de dados, com background em Engenharia Mecânica e experiência prática em gestão de dados de vendas e estoque no varejo alimentício.

[LinkedIn](#) · [Outros projetos no GitHub](#)
