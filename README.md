# MVP Análise de Dados e Boas Práticas - Classificação de Exoplanetas (Kepler)

Este projeto apresenta uma análise exploratória de dados (EDA) e um modelo de classificação para o conjunto de dados **Kepler Objects of Interest (KOI)**, gerado pela missão da sonda Kepler da NASA. O objetivo é identificar padrões que distinguem exoplanetas confirmados de falsos positivos astronômicos.

## Descrição do Problema

O conjunto de dados KOI contém informações sobre objetos celestes que apresentam sinais de trânsito planetário. O desafio consiste em realizar uma **classificação supervisionada** para distinguir entre duas categorias:
- **Exoplanetas Confirmados**: Objetos cuja natureza planetária foi verificada.
- **Falsos Positivos**: Objetos que inicialmente pareciam planetas, mas verificou-se que eram outros fenômenos (como estrelas binárias ou ruído instrumental).

### Hipóteses do Estudo
1. **Limiar de Raio**: Existe um tamanho de raio planetário acima do qual a probabilidade de confirmação cai drasticamente.
2. **Profundidade de Trânsito**: A queda no brilho da estrela hospedeira impacta diretamente na classificação.
3. **Limite Térmico**: Objetos com temperaturas de equilíbrio muito elevadas tendem a ser classificados como Falsos Positivos.

## Como rodar este projeto

### Pré-requisitos
- Python 3.8+
- Jupyter Notebook ou Google Colab

### Instalação
1. Clone o repositório:
   ```bash
   git clone https://github.com/igorcavalcante/MVP_analise_exploratoria.git
   cd MVP_analise_exploratoria
   ```
2. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt
   ```

### Execução
Abra o arquivo `analise.ipynb` no seu ambiente Jupyter e execute as células em sequência para visualizar a análise completa e o treinamento do modelo.

## Tecnologias Utilizadas
- **Linguagem**: Python
- **Manipulação de Dados**: Pandas, NumPy
- **Visualização**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn (Random Forest, RobustScaler)

## Resultados
O modelo de **Random Forest** treinado alcançou uma **acurácia de 91%** e um **F1-Score de 0.91**, demonstrando ser uma baseline sólida para a identificação automática de exoplanetas. As análises gráficas confirmaram as três hipóteses iniciais, destacando a importância do raio e da temperatura de equilíbrio na filtragem de candidatos.

## 🔗 Referências
- [Nasa Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/index.html)
- [Dataset KOI Cumulative](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=cumulative)

---
**Autor**: Igor Raphael Lins Cavalcante
