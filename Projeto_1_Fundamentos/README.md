# 📉 Fundamentos de Sinais: Reamostragem, Convolução e Análise de Erro

Este projeto explora os fundamentos de sinais e sistemas no **domínio do tempo e do espaço**. O objetivo principal é demonstrar as consequências de manipular taxas de amostragem em dados bidimensionais (imagens) e provar a eficácia de sistemas lineares invariantes no tempo através da operação de convolução.

O grande diferencial deste projeto é a **implementação algorítmica purista**. Em vez de utilizar funções nativas e otimizadas de bibliotecas (como `numpy.convolve`), a operação de convolução foi implementada integralmente "do zero", utilizando laços de repetição sobre a matemática teórica.

## 🎯 Principais Desafios e Tópicos Abordados

1. **Processamento 2D (Decimação e Interpolação):**
   * Leitura e manipulação de matrizes de pixels de uma imagem.
   * **Decimação:** Redução da taxa de amostragem (downsampling), evidenciando a perda de resolução e compressão de dados.
   * **Interpolação:** Aumento artificial da taxa de amostragem (upsampling) com preenchimento de zeros e retenção de ordem zero (ZOH), demonstrando técnicas de reconstrução de sinal espacial.

2. **Resposta ao Impulso Analítica vs. Truncada:**
   * Cálculo e plotagem da resposta ao impulso real de um sistema $h[n]$.
   * Análise do impacto de truncar uma resposta infinita (IIR) para um tamanho finito da memória computacional.

3. **Convolução Linear "From Scratch":**
   * Implementação algorítmica da soma de convolução discreta $y[n] = \sum h[k]x[n-k]$.
   * Comparação entre a saída do sistema gerada pela convolução com $h[n]$ truncado versus a solução analítica exata.

4. **Análise de Erro (MSE):**
   * Cálculo rigoroso do Erro Médio Quadrático (MSE - *Mean Squared Error*) para quantificar a perda de precisão gerada pelo truncamento do sistema, validando matematicamente a aproximação.

## 📊 Visualização de Resultados


### Convolução e Precisão do Sistema
#### Comparação entre Convolução Truncada e Resposta Analítica
<img width="600" height="374" alt="convolve_trunc_analit" src="https://github.com/user-attachments/assets/a9e97332-adce-470b-ab2e-9152c77197ce" />

*O gráfico ilustra a sobreposição quase perfeita da convolução manual com o cálculo analítico, gerando um Erro Médio Quadrático (MSE) na ordem de $10^{-17}$
.*

### Impacto da Reamostragem em Imagens
#### Comparação Imagem Original vs Interpolada

<img width="412" height="412" alt="lena" src="https://github.com/user-attachments/assets/2af36732-3e06-4bc2-8db8-56734e944304" />

<img width="412" height="412" alt="decimada" src="https://github.com/user-attachments/assets/f25f80e0-9730-48d8-98ac-869a8888fedc" />

*Comparativo visual do efeito de downsampling no domínio do espaço.*

## 🛠️ Tecnologias Utilizadas
* **Python 3** (Google Colab)
* **NumPy:** Essencial para a construção do laço de convolução manual e cálculo de MSE.
* **Matplotlib:** Para plotagem de sinais discretos (`plt.stem`) e renderização das matrizes de imagem.

---
*Este projeto faz parte do portfólio de Sinais e Sistemas em Tempo Discreto.*
