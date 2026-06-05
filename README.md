# PROJETO-AVALIATIVO-P2-Nathalia

# P2 - Classificação de Doença Hepática

Projeto acadêmico da disciplina de Inteligência Artificial, usando o dataset **Indian Liver Patient Records** para classificar pacientes com ou sem indicativo de doença hepática.

## Estrutura

```text
p2/
├── app.py
├── requirements.txt
├── README.md
├── data/
│   └── dataset_tratado.csv
├── model/
│   ├── modelo_final.joblib
│   ├── scaler.joblib
│   └── metadata.json
├── notebooks/
│   └── notebook_atualizado.ipynb
└── reports/
    └── relatorio_atualizado.pdf
```

## O que foi mantido

- Dataset original utilizado no trabalho anterior.
- Análise exploratória com distribuições, outliers, correlação e análise por gênero.
- Separação em treino, validação e teste.
- Classificadores: Regressão Logística, Random Forest e Gradient Boosting.
- Avaliação com Stratified K-Fold.
- Métricas: acurácia, precisão, recall, F1-score e AUC-ROC.
- Matrizes de confusão e curvas ROC.

## Arquivos necessários para o Streamlit

Como esta versão não usa `Pipeline`, o app precisa de dois arquivos principais:

- `model/modelo_final.joblib`: classificador treinado.
- `model/scaler.joblib`: normalizador usado antes do treinamento.

Também são gerados:

- `model/metadata.json`: informações sobre o modelo, variáveis e métricas.
- `data/dataset_tratado.csv`: dataset tratado usado no projeto.

## Como gerar os arquivos do modelo

1. Abra `notebooks/notebook_atualizado.ipynb`.
2. Execute todas as células em ordem.
3. A última célula gera automaticamente:

```text
model/modelo_final.joblib
model/scaler.joblib
model/metadata.json
data/dataset_tratado.csv
```

## Como rodar localmente

Instale as dependências:

```bash
pip install -r requirements.txt
```

Execute o app:

```bash
streamlit run app.py
```

## Como publicar no GitHub

1. Crie um repositório público no GitHub.
2. Envie esta pasta inteira para o repositório.
3. Confira se estão presentes:
   - `app.py`
   - `requirements.txt`
   - `README.md`
   - `notebooks/notebook_atualizado.ipynb`
   - `model/modelo_final.joblib`
   - `model/scaler.joblib`
   - `data/dataset_tratado.csv`
   - `reports/relatorio_atualizado.pdf`

## Como publicar no Streamlit Community Cloud

1. Acesse https://share.streamlit.io/.
2. Conecte sua conta do GitHub.
3. Selecione o repositório público do projeto.
4. Em **Main file path**, coloque:

```text
app.py
```

5. Faça o deploy.
6. Copie o link gerado e coloque no relatório ou no README.

## Observação

Este app é apenas uma demonstração acadêmica. Ele não deve ser usado como ferramenta de diagnóstico médico real.
