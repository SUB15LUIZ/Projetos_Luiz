# 📊 ETL - Banco Central (SGS) para Google Looker Studio

Este projeto realiza a extração de séries temporais públicas disponibilizadas pelo Sistema Gerenciador de Séries Temporais (SGS) do Banco Central do Brasil, utilizando sua API REST. As séries são organizadas e exportadas em arquivos CSV para fácil integração com o Google Looker Studio.

## ⚙️ Tecnologias Utilizadas
- Python 3 (Google Colab)
- Bibliotecas: `pandas`, `requests`
- Google Drive (armazenamento dos arquivos)
- Looker Studio (visualização e dashboards)

## 📥 Arquivo de Entrada

O script consome um arquivo Excel `Lista_de_series.xlsx`, que deve conter as seguintes colunas:

| Coluna             | Descrição                                                   |
|--------------------|-------------------------------------------------------------|
| `Codigo`           | Código da série no SGS (exemplo: 20718 para taxa SELIC)     |
| `Frequencia_dado`  | Frequência dos dados: `Mensal`, `Trimestral`, etc.          |
| `Nome_Ajustado`    | Nome amigável para uso como nome da coluna no output        |

## 📤 Arquivos de Saída
- `series_unificadas_mensal.csv`
- `series_unificadas_trimestral.csv`
- `erros_consulta.csv` — caso alguma série apresente erro durante a extração

## 🚀 Como Executar
1. Acesse o notebook no Google Colab
2. Monte o Google Drive
3. Execute o script `consulta_sgs_bacen.py`
4. Os arquivos CSV serão salvos em: `/Colab Notebooks/Consulta_Bacen`
5. Importe os arquivos CSV no Google Looker Studio para construir seus dashboards

## ✅ Exemplo de Uso
```python
!pip install pandas requests
!python consulta_sgs_bacen.py
```

## 📄 Licença
Este projeto é de uso livre e gratuito. Fique à vontade para utilizar, adaptar e contribuir!
