# Passos Mágicos — MLOps na Databricks

Projeto do Datathon da Fase 5 (Pós Tech — AI Scientist). O objetivo é construir e implantar na Databricks um pipeline de Machine Learning reproduzível, com base nos dados da Associação Passos Mágicos, que apoie a identificação de estudantes que talvez precisem de acompanhamento adicional.

> As previsões são **sinais de apoio à investigação pedagógica**, nunca rótulos definitivos nem substitutos da avaliação humana.

**Ciclo completo:** dados → features → treino → avaliação → registro → deploy → inferência → monitoramento

## Estrutura do repositório

```
├── README.md
├── notebooks/
│   ├── 01_data_quality_and_features.py   # Bronze/Silver/Gold + validações
│   ├── 02_train_and_evaluate.py          # Baseline, candidatos, MLflow
│   └── 03_register_and_inference.py      # Quality gate, registro, deploy, inferência
├── src/
│   ├── data.py
│   ├── features.py
│   ├── train.py
│   └── predict.py
├── tests/
│   └── test_input_validation.py
├── docs/
│   ├── architecture.md
│   ├── model_card.md
│   └── monitoring_plan.md
├── data/raw/                              # Dados locais (ignorados pelo git)
└── requirements.txt
```

## Como executar

> A preencher conforme o projeto avançar.

1. Clonar o repositório no Databricks via **Workspace → Git folders**.
2. Fazer o upload da base de dados para um Volume do Unity Catalog.
3. Executar os notebooks em ordem: `01` → `02` → `03`.

Testes locais:

```bash
pip install -r requirements.txt
pytest tests/
```

## Dados e privacidade

A base original contém informações de estudantes e **não é versionada** neste repositório (veja `.gitignore`). Também não devem ser commitados tokens, senhas ou credenciais: use os Databricks Secrets.

## Limitações do ambiente

> A preencher: recursos disponíveis no Databricks Free Edition (Unity Catalog, Model Serving, Jobs).

## Equipe

> A preencher.
