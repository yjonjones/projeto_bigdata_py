# Trabalho Prático Individual — Tópicos de Big Data em Python

**Nome:** Jonathan Monteiro Henriques
**Matrícula:** 202202160539

## Objetivo
Construir um pequeno pipeline de dados sobre `vendas_bigdata_2026.csv`: inspecionar e limpar os dados com Pandas, analisar o faturamento, reproduzir a análise regional com PySpark e Spark SQL, e responder às questões teóricas (HDFS e auditoria de ML).

## Tecnologias utilizadas
Python 3, Pandas, Matplotlib, PySpark (modo local), Spark SQL, scikit-learn, Jupyter.

## Como executar
```bash
pip install pandas matplotlib pyspark scikit-learn jupyter

jupyter nbconvert --to notebook --execute --inplace trabalho_bigdata.ipynb
```
Execute dentro desta pasta (o CSV `vendas_bigdata_2026.csv` deve estar ao lado do notebook). O notebook roda de cima para baixo e gera `resultado/resumo_regioes.csv` e `resultado/vendas_tratadas.csv`.

## Principais conclusões
- Foram removidas 8 duplicatas e 10 registros com quantidade/preço inválidos; 5 datas inválidas viraram `NaT` e os valores incoerentes (9 após remover os inválidos) foram recalculados pela regra de negócio.
- Faturamento tratado: ~R$ 538,8 mil em 1.182 pedidos.
- Sudeste lidera (~R$ 224 mil, mais de 40% do total); Site é o canal que mais fatura; Pix é a forma de pagamento mais usada.
- Cadeira e Mesa são os produtos de maior faturamento.
- Novembro/2026 tem dados só do dia 1, então a queda no último mês é artefato da cobertura dos dados.
