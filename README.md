# Projeto: Análise Preditiva de Saúde Populacional (Precision Healthcare)

> **Disciplina:** Projeto Final de Engenharia de Computação  
> **Instituição:** Faculdade Engenheiro Salvador Arena  
> **Data:** 17 de Março de 2026  
> **Versão:** 1.0

---

# Descrição Executiva

Este notebook contempla a etapa de **Engenharia de Dados (M1)**. O objetivo é desenvolver um pipeline de **ETL (Extract, Transform, Load)** capaz de consumir dados de saúde provenientes de um dataset público do Kaggle, realizar o tratamento de integridade e estruturar os dados sob a arquitetura de **Star Schema**.

A modelagem foi projetada para suportar análises preditivas em saúde populacional, permitindo a identificação de padrões clínicos, operacionais e financeiros relacionados a internações hospitalares.

---

# Equipe

| Integrante | RA | Responsabilidade |
|---|---|---|
| Carlos Eduardo Tumiati | 082210009 | ETL |
| Rilleri Tech | 082210007 | Documentação / QA |
| Ewerthon Moreira | 082210022 | Modelagem |
| Victor Luis | 082210029 | Analista |

---

# Stack Tecnológica

- **Linguagem:** Python 3.x
- **Bibliotecas Principais:** Pandas, NumPy
- **Ambiente:** Google Colab + Google Drive (Storage)

---

# Fonte de Dados

Os dados utilizados neste projeto foram obtidos a partir de um dataset público disponível no Kaggle, contendo informações hospitalares, incluindo:

- Dados demográficos dos pacientes
- Informações clínicas
- Dados administrativos hospitalares
- Custos de internação

---

# Pipeline ETL

## Extração

Os dados foram extraídos a partir de um dataset hospedado no Kaggle.

Uma cópia dos dados brutos foi armazenada no Google Drive para garantir persistência e rastreabilidade.

---

## Transformação

Durante esta etapa, foram aplicadas as seguintes técnicas de engenharia de dados:

- Remoção de registros duplicados
- Tratamento de valores nulos
- Conversão de tipos de dados (especialmente datas)
- Criação de novas variáveis derivadas (*feature engineering*)

### Variáveis Criadas

- `dias_internado`
  - Diferença entre data de alta e data de admissão

Além disso, foi realizada a estruturação dos dados no formato **Star Schema**, separando fatos e dimensões.

---

## Carga

Os dados processados foram armazenados no Google Drive em formato CSV, organizados em camadas:

```text
/data/raw       → dados brutos
/data/processed → tabelas dimensionais e fato
