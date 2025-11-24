# 📘 Projeto: Identificação de Sistemas via Funções Complexas e MMQ

Este projeto realiza a identificação de um sistema dinâmico utilizando dois métodos distintos:

- **Filtragem por Funções Complexas** (DFT + IDFT)  
- **Modelo por Mínimos Quadrados (MMQ/ARX)**  

O objetivo é comparar o desempenho de cada abordagem na reconstrução das saídas **x(t)** e **y(t)** a partir de dados reais com ruído.

---

## 📂 Conteúdo do Projeto

- Análise do sinal de entrada e das saídas reais/ruidosas  
- Ajuste via **Funções Complexas**  
  - Construção da DFT  
  - Aplicação de filtro espectral  
  - Reconstrução via IDFT  
- Ajuste via **MMQ (ARX)**  
  - Modelo dinâmico com atrasos de entrada e saída  
  - Estimação dos parâmetros via mínimos quadrados  
- Avaliações estatísticas  
  - Erro Médio Quadrático (EMQ)  
  - Correlação de Pearson  
  - Regressão Linear entre sinais ruidosos e ajustados  

---

## 📊 Resultados Principais

Após ajuste dos limiares de filtragem, o método de **Funções Complexas** apresentou o melhor desempenho para ambas as saídas.

### ✔️ Para **x(t)**:
- **EMQ (Complexas):** 0.0109  
- **EMQ (MMQ):** 0.0132  
- **r (Complexas):** 0.6915  
- **r (MMQ):** 0.6059  

### ✔️ Para **y(t)**:
- **EMQ (Complexas):** 0.0131  
- **EMQ (MMQ):** 0.0154  
- **r (Complexas):** 0.9250  
- **r (MMQ):** 0.9110  

➡️ As Funções Complexas preservaram melhor as componentes relevantes do espectro e suavizaram o ruído de forma mais eficiente.

---

## 🧠 Conclusão

Funções Complexas apresentaram o melhor desempenho global, tanto em erro quanto em correlação.  
Esse método se mostrou especialmente eficaz devido à capacidade de selecionar frequências dominantes e representar sinais harmônicos de forma natural.

O MMQ apresentou bons resultados, especialmente para sinais dependentes da dinâmica da entrada, mas foi superado pela filtragem espectral quando configurada com limiar adequado.

---

## 📁 Dataset

Contém:
- t (tempo)  
- u(t) (entrada)  
- x(t), y(t) (saídas ruidosas)  
- x₁(t), y₁(t) (saídas ideais)

---

## 🛠 Tecnologias Utilizadas

- Python  
- NumPy  
- Matplotlib  
- SciPy  
- Jupyter / VS Code  

---

## Autor

Guilherme Ribeiro Amorim  

