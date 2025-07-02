# Definições 

## Metemática

- `∀` = "para todo" ou "para qualquer"
- `∃` = "existe"
- `∄` = "não existe"
- `∈` = "pertence"
- `∉` = "não pertence"
- `∑` = "somatário"
- `⊃` = "contém"
- `⊅` = "não contém"
- `⊂` = "está contido"
- `⊄` = "não está contido"
- `⊆` = "subconjunto de" ou "está contido em"
- `⊇` = "subconjunto de" ou "está contido em"
- `/` = "tal que"

## Grafos

- `G = (V, E)` = um grafo é uma relação entre vértices e arestas.

    Um grafo G = (V, E) em que V é o conjunto de vértices e E o conjunto de 
    arestas de forma que:

    - `E = { (u, v) | u, v ∈ V }` grafo direcionado
    - `E = { {u, v} | u, v ∈ V }` grafo não-direcionado


- Vértices = objeto simples que pode ter nome e outros atributos.

- Arestas = conexão entre dois vértices.

---

- Grafo Direcionado = `E = { (u,v) / u,v ∈ V }`
    
    Um grafo direcionado é par `G = (V,E)`, em que V é um conjunto finito e E é uma 
    relação binária em V.

- Grafo Não-Direcionado = `E = { {u,v} / u,v ∈ V }`

    Um grafo não direcionado é um par `G = (V,E)` em que o conjunto de arestas E 
    consiste em pares de vértices não orientados. A aresta `(vi , vj)` e `(vj , vi)`
    são consideradas a mesma aresta.

---

- Multi-Grafo = um grafo que permite arestas paralelas e loops.

- Grafo Simples = um grafo que não possui loops e nem arestas paralelas

- Grafo Nulo = um grafo que tem arestas, porém possui vértices.

---

- Grafo Completo = Um grafo G=(V,E) é completo se para cada par de vértices 
                   vi e vj existe uma aresta entre vi e vj. Em um grafo completo 
                   quaisquer dois vértices distintos são adjacentes (Kn).

- Grafo Ponderado = `(G,w)`, ponderado nos vértices ou nas arestas.
                    w = peso

- Grafo Rotulado = Um grafo `G = (V,A)` é dito ser rotulado em vértices (ou arestas)
                   quando a cada vértice (ou aresta) estiver associado um rótulo.

- Grafo Valorado = Um grafo `G = (V,A)` é dito ser valorado quando existe uma ou 
                   mais funções relacionando V e/ou A com um conjunto de números.

## Arestas Parelelas e Loops

- Arestas paralelas = `G = (V,E) -> V = {a,b}, E = { (a,b), (a,b) }`

    Quando mais de uma aresta está associada ao mesmo par de vértices.

- Arestas anti-paralelas = `G = (V,E) -> V = {a,b}, E = { (a,b), (b,a) }`

    Quando há um aresta indo de vi para vj e de vj para vi.

- Loop = `G = (V,E) -> V = {a}, E = { (a,a) }`

    É uma aresta associada ao par de vértices (vi, vi).


## Grau

- Grafo não direcionado: 

    grau `δ(v)` = número de arestas que incidem em v.

- Grafo direcionado:

    grau de entrada `δ−(v)` = número de arestas que chegam em v 
    grau de saída `δ+(v)` = número de arestas que saem em v

> Um laço conta duas vezes para o grau de um vértice

## Cardinalidade

É a quantidade de elementos diferentes.

`|V|` = quantidade de vértices
`|E|` = quantidade de arestas

## 
