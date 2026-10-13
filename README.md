# Dashboard de Assinaturas

Dashboard de vendas feito dentro do Excel, a partir de uma base de 295 assinaturas iniciadas em 2024. Tudo é calculado por fórmulas: se a base mudar, o dashboard acompanha.

## Como usar

No painel escuro à esquerda ficam os botões de navegação. Cada um leva a um painel, lado a lado na mesma aba:

1. **Visão geral:** todas as assinaturas juntas.
2. **Monthly:** só as assinaturas de cobrança mensal.
3. **Quarterly:** só as de cobrança trimestral.
4. **Annual:** só as de cobrança anual.

Os quatro painéis têm o mesmo formato, então dá para comparar um com o outro. O período analisado aparece no topo de cada um: de 01/01/2024 até 16/12/2024, que é a data da última assinatura na base.

## O que cada painel mostra

- **Cartões de KPI:** assinantes ativos, MRR, ARR, ARPU e % de assinantes com renovação automática.
- **3 perguntas de negócio (OKRs):**
  1. Qual plano concentra mais receita recorrente?
  2. Que parte do MRR é recorrente de fato, ou seja, vem de quem renova sozinho?
  3. O MRR está crescendo mês a mês?
- **Tabelas:** KPIs separados entre renovável e não renovável, comparação por plano (Core, Standard, Ultimate) e comparação por tipo (Monthly, Quarterly, Annual).
- **Gráficos:** dois de barras horizontais (MRR por plano e por tipo, com renovável ao lado de não renovável) e um de linha com o MRR no fim de cada mês.
- **Série mensal e resumo trimestral e anual:** o mesmo MRR em tabela, mês a mês, e fechado por trimestre e pelo ano.

## Como os números são calculados

- **Assinatura ativa:** começou até a data de corte e, ou renova sozinha, ou o ciclo dela ainda não acabou. Quem não renova automaticamente "sai" do MRR quando o ciclo termina.
- **MRR (receita mensal recorrente):** o valor total da assinatura (plano + add-ons − cupom) dividido pelos meses do ciclo. Uma assinatura anual de R$ 12 vale R$ 1 por mês, por exemplo.
- **ARR:** MRR × 12.
- **ARPU:** MRR ÷ assinantes ativos.
- **MRR renovável × não renovável:** o MRR das assinaturas com renovação automática comparado ao das que não têm.

## Observações

- A base só tem data de início, não de cancelamento. Por isso não existe CHURN real: o que sai do MRR são as assinaturas sem renovação automática que chegaram ao fim do ciclo.
- O último mês (dezembro) é parcial: vai só até a data de referência, 16/12/2024.
- Como a base cobre só 2024, o resumo anual tem uma linha única. A comparação entre anos só aparece quando houver mais anos na base.
- A série mensal mostra 12 meses a partir do primeiro mês da base.

## Cores

Paleta usada: `#98967C`, `#7C7A62`, `#605F47`, `#43432D`, `#272712`, mais um tom claro de fundo derivado dela.
