# Análise Experimental do Algoritmo de Load Balancing Aplicado ao Problema de Job Scheduling

Este repositório contém a implementação e experimentação do algoritmo de **Load Balancing**, aplicado ao problema clássico de **Job Scheduling**.  
O trabalho faz parte da disciplina **Análise de Algoritmos**, com foco na investigação prática de desempenho, eficiência, comportamento e limitações de algoritmos gulosos em cenários reais de distribuição de tarefas.

---

## 1. Objetivo do Projeto

O objetivo principal deste estudo é analisar experimentalmente o comportamento do algoritmo de **Load Balancing** na distribuição de tarefas entre múltiplas máquinas.

A análise busca:

- Avaliar o makespan em diferentes cenários de entrada  
- Observar a eficiência da estratégia gulosa  
- Identificar possíveis limitações e gargalos  
- Comparar a distribuição de carga entre máquinas  
- Relacionar os resultados com a teoria da disciplina  

---

##  2. Problema de Job Scheduling

O problema consiste em distribuir um conjunto de tarefas entre **máquinas paralelas**, buscando minimizar o tempo total de execução (makespan).  

Formalmente, dado:

Este problema é conhecido por ser **NP-Difícil**, tornando heurísticas como o Load Balancing fundamentais em cenários reais.

---

## 3. Algoritmo Utilizado – Load Balancing (Greedy)

O algoritmo segue a abordagem gulosa:

1. Inicia todas as máquinas com carga zero  
2. Para cada tarefa, identifica a máquina menos carregada  
3. Atribui a tarefa a essa máquina  
4. Atualiza a carga  
5. No final, calcula o makespan  

###  Complexidade
A estratégia simples utilizada possui complexidade:

O(n × m)

onde:  
- **n** = número de tarefas  
- **m** = número de máquinas  

---

## 4. Metodologia Experimental

Foram realizados três experimentos:

- **Experimento A:** lista pequena  
- **Experimento B:** lista intermediária  
- **Experimento C:** lista extensa com grande variação  

Cada experimento segue o mesmo processo:

1. Inicialização das cargas
2. Distribuição sequencial das tarefas  
3. Contagem de operações  
4. Cálculo do makespan  
5. Geração de gráficos  

---

## 5. Resultados Obtidos

Os gráficos gerados mostram a carga final de cada máquina, permitindo comparar visualmente o equilíbrio (ou desequilíbrio) criado pelo algoritmo.

Você pode visualizar os gráficos no Apêndice do relatório ou gerar novamente executando o código deste repositório.

Principais observações:

- Tarefas pequenas tendem a gerar distribuições mais equilibradas  
- Aumentos na variação das tarefas criam picos de carga  
- A estratégia gulosa não prevê o efeito de tarefas futuras  
- O makespan cresce proporcionalmente ao desbalanceamento  

---

## 6. Discussão

Os experimentos evidenciam que:

- O algoritmo é eficiente, rápido e simples  
- Produz bons resultados para listas pequenas  
- Sofre desequilíbrio em listas grandes e heterogêneas  
- Reflete exatamente o comportamento esperado de heurísticas gulosas  

O método funciona como uma boa aproximação, mas não garante a solução ótima — fato essencial ao se lidar com problemas NP-difíceis como Job Scheduling.

---

##7. Código-Fonte

O código principal da simulação encontra-se disponível em:

- `load_balancing.py`  
- `experimentos.py`  

---

## 8. Referências

- Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. **Algorithms**, MIT Press.  
- Kleinberg, J., & Tardos, E. **Algorithm Design**, Pearson.  
- Tanenbaum, A. S. **Modern Operating Systems**, Prentice Hall.  
- Ullman, J. **NP-Complete Scheduling Problems**, Stanford University.  
- Artigos sobre heurísticas gulosas e balanceamento de carga em sistemas distribuídos.

---

## 9. Apêndice – Códigos Utilizados

Os códigos completos utilizados nos experimentos estão incluídos neste repositório.  
Para fins acadêmicos, mantêm identação, legibilidade e coerência com o relatório final entregue.

---

##  Autora

Letícia Bressanin
Estudante de Ciência da Computação – USC  
Focada em análise de algoritmos, desenvolvimento e aprendizado contínuo.

- Um conjunto de tarefas **T = {t1, t2, ..., tn}**  
- Um conjunto de máquinas **M = {M1, M2, M3}**  
- Cada tarefa possui um tempo de processamento associado  

O objetivo é encontrar uma distribuição que minimize:
