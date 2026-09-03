# Experimento 002 — limpeza do dataset de diabetes

## Objetivo

Preparar o **Pima Indians Diabetes Dataset** para uso em modelos de classificação, cuja variável-alvo é `Outcome` (presença ou ausência de diabetes).

## O que foi feito

- Análise exploratória dos 572 registros e 9 atributos por meio de estatísticas descritivas, histogramas e matriz de correlação.
- Identificação de `Glucose` como a variável mais correlacionada com `Outcome` (`0,480`), seguida por `BMI` (`0,308`).
- Levantamento de valores ausentes: `Insulin` (374), `SkinThickness` (227), `BloodPressure` (35), `BMI` (11) e `Glucose` (5).
- Remoção de `Insulin` e `SkinThickness`, pois concentravam a maior quantidade de dados ausentes.
- Preenchimento dos valores ausentes de `Glucose`, `BloodPressure` e `BMI` com a mediana de cada coluna.
- Exportação do conjunto tratado, sem valores ausentes, para [`data/diabetes_dataset_cleaned.csv`](data/diabetes_dataset_cleaned.csv).

## Resultado

O dataset final mantém os 572 registros e passa de 9 para 7 colunas. Neste notebook não houve normalização, treinamento ou avaliação de modelos; o trabalho ficou restrito à análise exploratória e ao pré-processamento.
