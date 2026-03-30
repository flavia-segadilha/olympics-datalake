# Exercício Olympics Data Lake

## Fontes de Dados

Os dados utilizados neste projeto foram obtidos a partir das seguintes fontes públicas:
* [Base dos Dados – Histórico das Olimpíadas ](https://www.kaggle.com/datasets/piterfm/paris-2024-olympic-summer-games)(`raw/athlete_event_result.csv`, `raw/athlete_bio.csv` e `raw/country.csv`)
* [Paris 2024 Olympic Summer Games Dataset ](https://basedosdados.org/dataset/62f8cb83-ac37-48be-874b-b94dd92d3e2b)(`raw/athletes.csv`, `raw/medals.csv` e `raw/nocs.csv`)

---

## Estrutura

```
olympics-datalake/
│
├── README.md             <- Estamos aqui
├── metadata_schema.json
├── pipeline.ipynb
├── raw/
│   ├── athlete_bio.csv
│   ├── athlete_event_result.csv
│   ├── country.csv
│   ├── athletes.csv
│   ├── medals.csv
│   └── nocs.csv
├── bronze/
│   ├── historico.csv
│   ├── paris.csv
│   ├── olimpiadas.csv
│   ├── *.parquet
│   └── *.json (metadados)
├── gold/
│   └── analise_medalhas/
│       ├── medalha.csv
│       ├── medalha_top10.csv
│       ├── medalha_plot.png
│       ├── medalha.json
│       └── medalha.parquet
│   └── analise_modalidades/
│       ├── modalidades.csv
│       ├── modalidades.json
│       └── modalidades.parquet
│   └── analise_genero/
│       ├── genero.csv
│       ├── genero.json
│       └── genero.parquet
```

---

## Metadados

Cada dataset possui um arquivo de metadados no formato JSON contendo:

* Nome do dataset
* Fonte dos dados
* Descrição
* Data de criação
* Colunas
* Quantidade de linhas

Exemplo:

```json
{
    "nome_dataset": "historico",
    "fonte": "dados historicos",
    "descricao": "Dataset de historico",
    "data_coleta": "2026-03-29",
    "campos": [
        "sex",
        "country",
        "sport",
        "medal"
    ],
    "qtd_linhas": 44996,
    "observacoes": "Gerado automaticamente"
}
```

A sua estrutura base pode ser emcontrada em `metadata_schema.json`.
