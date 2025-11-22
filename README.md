# 🚚💰 Otimizador de Lucro para Transporte  
### Modelagem Matemática + Algoritmos de Otimização + Análise Comparativa

Este projeto demonstra a aplicação de técnicas de **Otimização Combinatória** e **Meta-Heurísticas** para maximizar o lucro no transporte de cargas.  
Dado um conjunto de itens — cada um com **peso**, **volume** e **valor** — o objetivo é selecionar aqueles que ofereçam o **maior lucro possível**, respeitando as limitações físicas do veículo.


---

## 🎯 Objetivo do Projeto

Construir um sistema de otimização capaz de selecionar automaticamente o conjunto ideal de itens a transportar, maximizando o lucro total, sob duas restrições principais:

- **Capacidade máxima de peso**
- **Capacidade máxima de volume**

Este é um caso realista do **0/1 Multi-Constraint Knapsack Problem**, uma das classes de problemas **NP-Hard** mais importantes em logística, transporte e distribuição.

---

## 🧠 Tecnologias Utilizadas

O projeto faz uso de ferramentas fundamentais para modelagem matemática, análise numérica e desenvolvimento de heurísticas:

### **Linguagens & Ambiente**
- Python 3

### **Bibliotecas Principais**
- **NumPy** — vetorização e cálculos numéricos  
- **Pandas** — manipulação tabular dos itens  
- **Random / Math** — suporte para heurísticas estocásticas  
- **Matplotlib (opcional)** — gráficos comparativos  
- **DEAP (opcional)** — para versão avançada do algoritmo genético  

### **Categoria Tecnológica**
- Otimização Combinatória  
- Meta-heurísticas de Busca  
- Matemática Aplicada  
- Modelagem de Sistemas  
- Pesquisa Operacional  

---

## 📐 Formulação Matemática do Problema

Considere \( n \) itens, onde para cada item \( i \):

- \( p_i \) = valor (lucro)  
- \( w_i \) = peso  
- \( v_i \) = volume  
- \( x_i \in \{0,1\} \) = decisão de transportar ou não  

Com:

- \( W \) = capacidade máxima de peso  
- \( V \) = capacidade máxima de volume  

### **Função Objetivo**
Maximizar o lucro total:

\[
\max \sum_{i=1}^{n} p_i x_i
\]

### **Restrições**
\[
\sum_{i=1}^{n} w_i x_i \le W
\]

\[
\sum_{i=1}^{n} v_i x_i \le V
\]

\[
x_i \in \{0,1\}
\]

### **Classificação**
- Problema **NP-Hard**
- Solução exata possível apenas para instâncias menores (via DP)  
- Para cenários reais, é comum utilizar heurísticas/meta-heurísticas  

---

## 🧪 Algoritmos Avaliados no Projeto

Este projeto compara métodos exatos e heurísticos para avaliar sua eficácia na otimização do transporte:

### **🔹 Dynamic Programming (DP)**
- Método exato.  
- Retorna a melhor solução global.  
- Melhor desempenho geral.

### **🔹 Multi-Start Hill Climbing**
- Múltiplas buscas locais.  
- Uma das melhores heurísticas neste estudo.

### **🔹 Algoritmo Genético (GA)**
- Inspirado em evolução biológica.  
- Bom equilíbrio entre exploração e qualidade.

### **🔹 GRASP**
- Combina construção gulosa com busca local.  
- Resultados consistentes e robustos.

### **🔹 Simulated Annealing (SA)**
- Evita mínimos locais aceitando soluções piores temporariamente.

### **🔹 Tabu Search**
- Usa memória para evitar retornar a soluções anteriores.  

---

## 🏆 Resultados Obtidos

Resultados reais obtidos durante os experimentos:

| Algoritmo | Lucro Total |
|-----------|-------------|
| ⭐ **Dynamic Programming (DP)** | **27.811** |
| Multi-Start Hill Climbing | 17.523 |
| Algoritmo Genético (GA) | 17.110 |
| GRASP | 15.600 |
| Simulated Annealing | 10.800 |
| Tabu Search | 8.400 |

### 📌 Conclusão do Estudo

- **DP** obteve o melhor resultado absoluto — como esperado de um método exato.  
- Entre as heurísticas, o destaque foi o **Hill Climbing Multi-Start**.  
- O projeto demonstra claramente o trade-off entre **velocidade x qualidade**, que é central em problemas reais de logística.

---

## 🧩 Valor do Projeto para Portfólio

Este trabalho demonstra:

- Capacidade de modelagem matemática avançada  
- Domínio de meta-heurísticas e algoritmos de otimização  
- Conhecimento de problemas NP-hard aplicados à logística  
- Comparação quantitativa entre métodos distintos  
- Capacidade de estruturar e analisar soluções complexas  
- Clareza na comunicação técnica para projetos profissionais  

---

## 📜 Observação Final

Este projeto não é um produto final pronto para produção —  
ele foi construído para fins **didáticos**, **acadêmicos** e como **prova de domínio técnico** em otimização, logística e inteligência computacional.

