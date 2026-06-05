# 🫀 Filtragem Digital Aplicada a Sinais Biomédicos (ECG)

Este projeto foca na aplicação prática de Processamento Digital de Sinais (DSP) para a limpeza e condicionamento de Eletrocardiogramas (ECG).
Sinais biomédicos são altamente suscetíveis a ruídos externos, e este repositório demonstra o ciclo completo de projeto de filtros IIR para recuperar a morfologia original do batimento cardíaco.

## 🎯 Principais Desafios e Tópicos Abordados

1. **Rejeição de Rede Elétrica (Filtro Notch):**
   * Projeto geométrico no Círculo Unitário para aniquilar especificamente a interferência de 60 Hz da rede elétrica brasileira.
   * Implementação da equação de diferenças iterativa iterando amostra por amostra.

2. **Atenuação de Ruído Muscular e Térmico (Filtro Passa-Baixas):**
   * Projeto de um filtro passa-baixas com frequência de corte em 35 Hz.
   * Cálculo e aplicação rigorosa da **Normalização de Ganho DC** para garantir que a amplitude do sinal biomédico não sofra amplificações artificiais durante o processamento.

3. **Digitalização de Sistemas Analógicos:**
   * Mapeamento de um filtro contínuo no plano de Laplace (Plano s) para o domínio discreto (Plano z) utilizando a **Transformada Bilinear (Método de Tustin)**.
   * Análise profunda do fenômeno de *Frequency Warping* (efeito sanfona).
   * Avaliação do impacto de diferentes taxas de amostragem (Critérios de 10% e 1%) na estabilidade e fidelidade da cópia digital em relação ao sistema analógico ideal.

4. **Análise de Resposta Transitória:**
   * Comparação gráfica entre a resposta ao impulso analógica ideal e a resposta ao impulso digital escalonada pelo período de amostragem.
   * Avaliação da resposta do sistema a sinais de energia (exponenciais de decaimento).

## 📊 Visualização de Resultados

### Recuperação do Complexo QRS
<img width="1190" height="590" alt="image" src="https://github.com/user-attachments/assets/72acc5de-50be-4831-9be0-d4101c54fa89" />

*O gráfico ilustra a remoção completa da "grama" térmica de alta frequência e da sanfona de 60Hz, preservando perfeitamente a altura original dos picos graças à normalização de ganho.*

### O Impacto da Transformada Bilinear (Diagrama de Bode)
<img width="963" height="434" alt="image" src="https://github.com/user-attachments/assets/90e5c915-8632-4c22-a154-25ecd26eab2f" />

*A visualização comprova o mergulho do ganho em direção ao menos infinito na frequência de Nyquist, revelando o mapeamento não-linear característico do Método de Tustin e a periodicidade espectral.*

## 🛠️ Tecnologias Utilizadas
* **Python 3**
* **NumPy:** Utilizado para manipulação vetorial e execução algébrica das equações de diferença.
* **Matplotlib:** Para a geração dos diagramas de Bode em escala logarítmica e visualização temporal do ECG.
* **SciPy:** Limitado apenas à extração de dados brutos (`.mat`) da base biomédica simulada.
