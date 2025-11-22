# 🚚💰 Otimizador de Lucro para Transporte  
### Comparação de Algoritmos de Otimização (DP, GA, SA, GRASP, Tabu Search, Hill Climbing)

Este projeto implementa um **sistema de otimização logística** para maximizar o lucro do transporte de cargas considerando:

- **Peso máximo suportado**
- **Volume máximo disponível**
- **Valor dos itens transportados**

A lógica é inspirada no clássico **Knapsack Problem**, mas adaptada para uso real em **transporte e logística**, permitindo testar diferentes heurísticas e algoritmos de busca para encontrar a melhor solução.

---

# 🎯 Objetivo

Selecionar o conjunto ideal de itens a serem transportados para **maximizar o lucro** respeitando as seguintes restrições:

- Limite de **peso**
- Limite de **volume**
- Cada item tem:
  - Peso  
  - Volume  
  - Valor (lucro)

---

# 🧠 Algoritmos Incluídos no Projeto

O sistema testa automaticamente várias abordagens clássicas e modernas de otimização:

### 🔹 **1. Dynamic Programming (DP)**
- Entrega o resultado **ótimo global**.
- Melhor desempenho geral.
- Útil como baseline para comparar heurísticas.

### 🔹 **2. Multi-Start Hill Climbing**
- Reinicia diversas vezes em pontos aleatórios.
- Melhor heurística do projeto.
- Rápido e eficiente.

### 🔹 **3. Algoritmo Genético (GA)**
- Evolução populacional.
- Bom desempenho, resultado estável.

### 🔹 **4. GRASP**
- Combinação de guloso + busca local.
- Resultados intermediários.

### 🔹 **5. Simulated Annealing (SA)**
- Aceita soluções piores com probabilidade decrescente.
- Evita mínimos locais.

### 🔹 **6. Tabu Search**
- Usa memória de movimentos proibidos.
- Foi a heurística com pior desempenho neste conjunto de dados.

---

# 🏆 Ranking Final dos Algoritmos

Após execução no dataset do projeto, o ranking final foi:

| Algoritmo | Lucro Total Obtido |
|----------|---------------------|
| ⭐ **Dynamic Programming (DP)** | **27811** |
| Multi-Start Hill Climbing | 17523 |
| Algoritmo Genético (GA) | 17110 |
| GRASP | 15600 |
| Simulated Annealing | 10800 |
| Tabu Search | 8400 |

> **Conclusão:**  
> 🔥 *A melhor solução absoluta é encontrada por **DP**.*  
> 🚀 *A melhor heurística para cenários grandes ou dinâmicos é o **Hill Climbing Multi-Start***.

---


