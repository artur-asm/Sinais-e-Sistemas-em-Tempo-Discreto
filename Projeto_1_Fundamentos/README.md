[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Quite-my-Tempo/Sinais-e-Sistemas-em-Tempo-Discreto/blob/main/Projeto1_Fundamentos/projeto1.ipynb)

# 📉 Fundamentos de Sinais: Reamostragem, Convolução e Análise de Erro

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](COLOQUE_SEU_LINK_AQUI)

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

*(Adicione imagens aqui para ilustrar o projeto. Exemplos sugeridos:)*

### Convolução e Precisão do Sistema
![Comparação entre Convolução Truncada e Resposta Analítica](caminho_para_sua_imagem_convolucao.png)
*O gráfico ilustra a sobreposição quase perfeita da convolução manual com o cálculo analítico, gerando um Erro Médio Quadrático (MSE) na ordem de $10^{-17}$.*

### Impacto da Reamostragem em Imagens
![Comparação Imagem Original vs Decimada](caminho_para_sua_imagem_decimacao.png)
*Comparativo visual do efeito de downsampling no domínio do espaço.*

## 🛠️ Tecnologias Utilizadas
* **Python 3** (Google Colab)
* **NumPy:** Essencial para a construção do laço de convolução manual e cálculo de MSE.
* **Matplotlib:** Para plotagem de sinais discretos (`plt.stem`) e renderização das matrizes de imagem.

---
*Este projeto faz parte do portfólio de Sinais e Sistemas em Tempo Discreto.*
