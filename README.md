# 📡 Processamento Digital de Sinais e Sistemas em Tempo Discreto

Este repositório compila os projetos práticos e teóricos desenvolvidos durante a disciplina de **Sinais e Sistemas em Tempo Discreto**, oferecida pelo Departamento de Engenharia Elétrica (ENE) da **Universidade de Brasília (UnB)**.

O objetivo principal destes projetos é demonstrar a aplicação de conceitos matemáticos avançados de processamento de sinais através da implementação de algoritmos "do zero" (from scratch), provando o domínio da matemática discreta sem a dependência inicial de funções caixa-preta.

## 🗂️ Estrutura do Repositório

O repositório está dividido em quatro projetos fundamentais que cobrem desde a base no domínio do tempo até a análise avançada no domínio da frequência:

### 1. [Fundamentos: Reamostragem, Convolução e Análise de Erro (MSE)](Projeto_1_Fundamentos/)
Projeto focado nas operações fundamentais de sinais e sistemas discretos no domínio do tempo e espaço.
* **Tópicos abordados:** Decimação e interpolação (aplicadas ao processamento de imagens), resposta ao impulso analítica vs. truncada.
* **Destaque:** Implementação manual da operação de Convolução Linear e cálculo do Erro Médio Quadrático (MSE) para validar a precisão do truncamento de sistemas.

### 2. [Projeto de Filtros e Aplicação Biomédica (ECG)](Projeto_2_Filtros_ECG/)
Projeto focado no tratamento de sinais reais de eletrocardiograma contaminados por ruídos e na transição do mundo analógico para o digital.
* **Tópicos abordados:** Projeto geométrico de Filtros Notch e Passa-Baixas (alocação de polos e zeros), Equações de Diferenças e Transformada Bilinear (Método de Tustin).
* **Destaque:** Filtragem de interferência da rede elétrica (60Hz) e ruídos térmicos, além da análise do *frequency warping* ao variar a taxa de amostragem de sistemas digitalizados.

### 3. [Transformada de Fourier e Decodificação DTMF (Goertzel)](Projeto_3_DTMF/)
Projeto focado na implementação da Transformada Discreta de Fourier (DFT) sem uso de bibliotecas prontas, analisando suas propriedades no domínio da frequência.
* **Tópicos abordados:** Amostragem de sinais contínuos, janelamento, extensão periódica, filtragem ideal no domínio da frequência e espectro de magnitude e fase.
* **Destaque:** Implementação manual da DFT pela definição, filtragem passa-baixas de sinais de ECG operando diretamente nos coeficientes de Fourier, e construção de um decodificador numérico de tons telefônicos (DTMF) utilizando um algoritmo otimizado (Goertzel simplificado).

### 4. [DFT, Filtragem por Janelas e Projeto de Filtros FIR por Amostragem](Projeto_4_filtros_FIR/)
Projeto focado na Transformada Discreta de Fourier como ferramenta de projeto e filtragem, tanto na teoria como na prática.
* **Tópicos abordados:** Implementação manual da DFT e do primeiro estágio de Cooley-Tukey (decomposição par/ímpar), filtragem no domínio da frequência com FFT, método *Overlap-and-Add* para processamento em blocos, e projeto de filtros FIR por amostragem em frequência.
* **Destaque:** DFT calculada sem nenhuma função caixa-preta (loop duplo puro), validada pelo MAE ~10⁻¹³ contra a decomposição par/ímpar. Implementação completa do *Overlap-and-Add* com erro máximo de 7×10⁻¹⁴ em relação ao `lfilter` nativo. Projeto de filtros FIR para ECG (fc = 50 Hz) demonstrando o impacto da centralização da *sinc* na qualidade espectral, e aplicação de *zero-phase filtering* (`filtfilt`) para eliminar o atraso de grupo de 40 ms nos picos R do ECG.

## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Python 3** (Executado via Google Colab)
* **NumPy:** Álgebra linear, geração de vetores de tempo/frequência e implementação de equações recursivas.
* **Matplotlib:** Plotagem de sinais no tempo, diagramas de Bode (escala logarítmica) e respostas em frequência.
* **SciPy:** Leitura de bases de dados biomédicos, manipulação de arquivos `.mat`, projeto de filtros (`firwin`, `freqz`, `lfilter`, `filtfilt`).
