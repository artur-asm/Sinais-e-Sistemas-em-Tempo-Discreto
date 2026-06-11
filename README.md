# 📡 Processamento Digital de Sinais e Sistemas em Tempo Discreto

Este repositório compila os projetos práticos e teóricos desenvolvidos durante a disciplina de **Sinais e Sistemas em Tempo Discreto**, oferecida pelo Departamento de Engenharia Elétrica (ENE) da **Universidade de Brasília (UnB)**.

O objetivo principal destes projetos é demonstrar a aplicação de conceitos matemáticos avançados de processamento de sinais através da implementação de algoritmos "do zero" (from scratch), provando o domínio da matemática discreta sem a dependência inicial de funções caixa-preta.

## 🗂️ Estrutura do Repositório

O repositório está dividido em dois projetos fundamentais que cobrem desde a base no domínio do tempo até o projeto de filtros no domínio da frequência:

### 1. [Fundamentos: Reamostragem, Convolução e Análise de Erro (MSE)](Projeto_1_Fundamentos/)
Projeto focado nas operações fundamentais de sinais e sistemas discretos no domínio do tempo e espaço.
* **Tópicos abordados:** Decimação e interpolação (aplicadas ao processamento de imagens), resposta ao impulso analítica vs. truncada.
* **Destaque:** Implementação manual da operação de Convolução Linear e cálculo do Erro Médio Quadrático (MSE) para validar a precisão do truncamento de sistemas.

### 2. [Projeto de Filtros e Aplicação Biomédica (ECG)](Projeto_2_Filtros_ECG/)
Projeto focado no tratamento de sinais reais de eletrocardiograma contaminados por ruídos e na transição do mundo analógico para o digital.
* **Tópicos abordados:** Projeto geométrico de Filtros Notch e Passa-Baixas (alocação de polos e zeros), Equações de Diferenças e Transformada Bilinear (Método de Tustin).
* **Destaque:** Filtragem de interferência da rede elétrica (60Hz) e ruídos térmicos, além da análise do *frequency warping* ao variar a taxa de amostragem de sistemas digitalizados.

## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Python 3** (Executado via Google Colab)
* **NumPy:** Álgebra linear, geração de vetores de tempo/frequência e implementação de equações recursivas.
* **Matplotlib:** Plotagem de sinais no tempo, diagramas de Bode (escala logarítmica) e respostas em frequência.
* **SciPy:** Leitura de bases de dados biomédicos e manipulação de arquivos `.mat`.
