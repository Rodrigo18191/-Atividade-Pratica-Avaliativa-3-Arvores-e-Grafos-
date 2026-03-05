# Análise Comparativa entre ShellSort e HeapSort

Aluno: Rodrigo Henrique Toniolli Oliveira (2411828)

---

## Questão 1

O HeapSort possui complexidade O(n log n) garantida em todos os casos porque o funcionamento do algoritmo não depende da ordem inicial dos elementos. Primeiro é feita a construção da estrutura chamada heap, que organiza os elementos em uma árvore binária completa onde o maior valor fica na raiz. Essa etapa tem custo aproximado de O(n).

Depois disso, o algoritmo remove o maior elemento (a raiz) e reorganiza a estrutura para manter a propriedade do heap. Essa reorganização custa O(log n) e é repetida para cada elemento do vetor. Como essa operação ocorre n vezes, o custo total se mantém em O(n log n).

Já o ShellSort não possui uma complexidade totalmente previsível porque o desempenho do algoritmo depende da sequência de gaps utilizada. Os gaps são os intervalos usados para comparar os elementos. Dependendo da sequência escolhida, o desempenho pode variar bastante, podendo chegar próximo de O(n²) em alguns casos. Por esse motivo, o tempo de execução do ShellSort não é tão previsível quanto o do HeapSort.

---

## Questão 2

Vetor inicial: [30, 12, 45, 6, 18, 3]

### a) Max-Heap correspondente

Após organizar os elementos para formar um Max-Heap, onde cada pai é maior que seus filhos, o vetor fica: [45, 18, 30, 6, 12, 3]

### b) Vetor após a primeira extração da raiz

Primeiro ocorre a troca da raiz com o último elemento: [3, 18, 30, 6, 12, 45]

Depois é feita a reorganização do heap (heapify), resultando em: [30, 18, 3, 6, 12, 45]

---

## Questão 3

A) Apenas II e IV

---

## Questão 4

Em um sistema que processa milhões de registros diariamente, o algoritmo mais indicado seria o HeapSort. Isso acontece porque ele possui complexidade O(n log n) garantida independentemente da organização inicial dos dados.

Essa previsibilidade é importante em sistemas grandes, pois garante um tempo de execução mais estável mesmo com grandes quantidades de informação. Já o ShellSort pode ter desempenho variável dependendo da sequência de gaps utilizada, o que pode gerar variações no tempo de execução quando o volume de dados é muito grande.

---

## Questão 5

A estrutura Heap é muito utilizada para implementar filas de prioridade. Nesse tipo de estrutura, cada elemento possui uma prioridade e o elemento com maior ou menor prioridade pode ser acessado rapidamente.

Em algoritmos de grafos, essa estrutura é usada para selecionar o próximo elemento mais importante a ser processado. Um exemplo clássico é o algoritmo de Dijkstra, utilizado para encontrar o menor caminho em um grafo. Nesse algoritmo, uma fila de prioridade baseada em Heap é utilizada para sempre selecionar o vértice com a menor distância conhecida até o momento.

Com o uso do Heap, as operações de inserção e remoção podem ser realizadas em O(log n), o que melhora significativamente a eficiência do algoritmo.



