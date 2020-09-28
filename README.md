# backtests-ibov-cbs-repo
*Backtests - Compra/Venda Ibovespa após circuit breakers.*

---
## Backtests de Compra Após Circuit Breakers:

Comparação de três estratégias:
1. Compra sempre a mesma quantia (corrigida pelo IPCA) do Ibovespa no primeiro dia útil de todos os meses. 
2. Compra sempre a mesma quantia (corrigida pelo IPCA) do CDI no primeiro útil do mês e investir no Ibovespa a quantia acumulada no CDI no dia seguinte a circuit breakers.
3. Compra sempre a mesma quantia (corrigida pelo IPCA) do CDI no primeiro útil do mês e investir no Ibovespa a quantia acumulada no CDI 21 dias úteis após circuit breakers.

## Backtests de Venda Após Circuit Breakers:

1. Venda no preço de fechamento dos dias com circuit breakers. Ficar de fora por um mês esperando uma recuperação, deixando o dinheiro no CDI nesse período. Recomprar o índice um mês (21 dias úteis) depois.
5. Mesmo da estratégia 1, mas considerando impostos.

---

## Dados retirados de:

Dados de 01/07/1994 até 31/07/2020.

Ibovespa:
 - 1994 até 2000: [BC](https://www3.bcb.gov.br/sgspub/localizarseries/localizarSeries.do?method=prepararTelaLocalizarSeries)
 - Após 2000: [Investing.com](https://br.investing.com/indices/bovespa)
 
CDI: [BC](https://www3.bcb.gov.br/sgspub/localizarseries/localizarSeries.do?method=prepararTelaLocalizarSeries)
 
IPCA: [BC](https://www3.bcb.gov.br/sgspub/localizarseries/localizarSeries.do?method=prepararTelaLocalizarSeries)


*Os dias com circuit breakers utilizados foram os seguintes:*

*05/09/1994*\**, 27/10/1997, 07/11/1997, 12/11/1997, 21/08/1998, 04/09/1998, 10/09/1998, 17/09/1998, 13/01/1999, 14/01/1999, 11/09/2001*\*\**, 29/09/2008, 06/10/2008, 10/10/2008, 15/10/2008, 22/10/2008, 18/05/2017, 09/03/2020, 11/03/2020, 12/03/2020, 16/03/2020, 18/03/2020.*

\**Não encontrei nenhuma informação sobre circuit breaker nesse dia, mas como fechou com uma queda superior à 10%, resolvi incluir no teste.*

\*\**Dia do atentado às torres gêmeas. Não houve o circuit breaker propriamente dito, mas houve grande queda e as negociações foram interrompidas.*
