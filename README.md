# Simulador de Investimentos em Fundos Imobiliários (FIIs)

O objetivo é fornecer uma ferramenta interativa e automatizada construída no Microsoft Excel para projeção de acúmulo patrimonial e geração de renda passiva com Fundos de Investimento Imobiliário.

---

## Visão Geral do Projeto

A ferramenta simula a mecânica dos juros compostos aplicada ao ecossistema de FIIs, permitindo ao investidor responder a perguntas estratégicas:
- Quanto terei acumulado após determinado período de aportes?
- Qual será meu fluxo de dividendos mensais (renda passiva)?
- Qual é o impacto financeiro real do reinvestimento dos proventos versus o resgate mensal?
- Quando atinjo o chamado "efeito bola de neve" (quando a renda mensal compra novas cotas sem necessidade de aporte externo)?

---

## Funcionalidades e Parâmetros

A planilha opera com entradas dinâmicas e fórmulas automatizadas:

### Parâmetros de Entrada (Inputs)
- **Investimento Inicial (R$):** Montante disponibilizado para a primeira compra de cotas.
- **Aporte Mensal Recorrente (R$):** Valor poupado e injetado mensalmente no portfólio.
- **Dividend Yield Médio Mensal (%):** Taxa média de retorno em proventos ao mês.
- **Preço Médio da Cota (R$):** Valor unitário de referência da cota para cálculo da quantidade de cotas.
- **Prazo da Simulação (Meses):** Horizonte temporal projetado.
- **Reinvestimento dos Proventos (Sim/Não):** Chave condicional para simulação com ou sem juros compostos ativos.

### Métricas de Saída (KPIs)
- **Total Investido do Bolso:** Capital direto aportado pelo investidor.
- **Patrimônio Acumulado Final:** Montante global ao término do período.
- **Total em Dividendos Recebidos:** Proventos brutos gerados pelos ativos.
- **Renda Passiva Projetada:** Fluxo financeiro mensal gerado ao fim da simulação.
- **Quantidade de Cotas Acumuladas:** Volume de cotas em carteira.

---

## Fórmulas e Lógica Aplicada

1. **Rendimento Mensal:**
   $$\text{Rendimento}_t = \text{Patrimônio Inicial}_t \times \text{DY Mensal}$$
2. **Reinvestimento Condicional:**
   Utilização da função lógica `=SE(Reinvestir="SIM"; Rendimento; 0)`.
3. **Cálculo de Cotas:**
   Utilização da função `=INT(Patrimônio / Preço Médio da Cota)` para contabilizar apenas lotes inteiros de cotas.
4. **Resumo Dinâmico via Busca:**
   Emprego da função `=PROCV()` para recuperar os valores do último mês selecionado pelo usuário no painel de controle.

<img width="2752" height="1536" alt="logo" src="https://github.com/user-attachments/assets/5d12c6cd-47c4-4fec-804f-480134dea6aa" />



