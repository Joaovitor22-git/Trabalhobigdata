Trabalho Prático Individual — Tópicos de Big Data em Python
Nome: João Vitor Figueira
Matrícula: 202408150768

Objetivo
Construir um pequeno pipeline de dados sobre vendas de varejo (vendas_bigdata_2026.csv): inspeção, limpeza e validação com Pandas, análise exploratória com gráficos, agregações com PySpark e Spark SQL, além de questões conceituais sobre HDFS e uma auditoria de Machine Learning.

Tecnologias utilizadas
Python 3, Pandas, Matplotlib, PySpark (Spark SQL), scikit-learn, Jupyter Notebook.

Como executar
pip install pandas matplotlib pyspark scikit-learn jupyter
jupyter nbconvert --to notebook --execute --inplace trabalho_bigdata.ipynb
Requer Java (JDK 8+) instalado para o PySpark. O notebook lê dados/vendas_bigdata_2026.csv e gera os arquivos em resultado/.

Estrutura
├── trabalho_bigdata.ipynb
├── README.md
├── dados/vendas_bigdata_2026.csv
└── resultado/
    ├── resumo_regioes.csv
    └── vendas_tratadas.csv
Principais conclusões
Dos 1.200 registros, 1.173 foram mantidos após remover duplicatas, quantidades/preços inválidos e valores incoerentes.
Faturamento total ≈ R$ 535 mil; Sudeste lidera (~41%).
Site é o canal de maior faturamento; Pix é a forma de pagamento mais usada.
Top produtos: Cadeira, Mesa, Aspirador, SSD 1TB e Joystick.
Faturamento mensal oscila entre ~R$ 40 mil e ~R$ 67 mil (novembro tem só 1 dia de dados).
O código original de ML tinha data leakage (scaler ajustado antes do split); corrigido com Pipeline.
