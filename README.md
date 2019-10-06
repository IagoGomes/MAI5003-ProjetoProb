# Projeto de Probabilidade e Estatística - Mecai 2019

Baseado no projeto: [Predicting Hospital Readmission for Patients with Diabetes Using Scikit-Learn](https://towardsdatascience.com/predicting-hospital-readmission-for-patients-with-diabetes-using-scikit-learn-a2e359b15f0) utilizando o [github deles](https://github.com/andrewwlong/diabetes_readmission)

A base de dados utilizadas pode ser encontrada em [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008). 

Este projeto foi criado com base no ambiente conda environment.yml. 

## Descrição 

Foram criados dois jupyter notebooks sendo um para a preparação do DataFrame (`data_prep.jpynb`) e outro para validação, aplicação de modelos e análises (`validation_train.jpynb`).

O `data_prep.jpynb` importa o csv `diabetic_data.csv`, que é a base obtida do [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008), e faz a formatação para a aplicação nos modelos de machine learning. Então, exporta os dados 'formatados' no arquivo `diabetic_data_df.csv` bem como as colunas a serem utilizadas pelos modelos no `col2use.csv`. 

O `validation_train.jpynb` importa o DataFrame já trabalhado pelo `data_prep.jpynb`, faz a validação, normaliza os dados, aplica nos modelos e possui funções de calculo de threshold ótimo, gráficos e report (matriz de confusão e classification report do SKLearn).

**Atenção**
Como o tamanho do `diabetic_data_df.csv` excede os 25mb permitidos pelo github, para rodar o `validation_train.jpynb` é necessário rodar o `data_prep.jpynb` primeiro, pois este gera o `diabetic_data_df.csv`.