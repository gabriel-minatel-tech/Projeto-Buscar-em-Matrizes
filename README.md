# 🔎 Projeto Busca em Matrizes

> Busca binária em matrizes **n × m** com **C++**: de O(n·m) para O(log(n·m)).

![C++](https://img.shields.io/badge/C++-17-blue?logo=cplusplus)
![Disciplina](https://img.shields.io/badge/Algoritmos%20e%20Estrutura%20de%20Dados-purple)
![Status](https://img.shields.io/badge/status-em%20evolução-yellow)

---

## 📖 Sobre o projeto

Este projeto nasceu de atividades da disciplina de **Algoritmos e Estrutura de Dados** e mostra a evolução de uma ideia simples: **como buscar um valor em uma matriz sem percorrer todos os elementos?**

A busca tradicional visita cada posição, com custo proporcional a `n × m`. Aqui, eu ordeno a matriz e aplico **busca binária**, reduzindo a busca para **O(log(n·m))**, o mesmo que `log(linhas) + log(colunas)`.

## ⚙️ Como funciona

```
Matriz 2D  →  Vetor 1D  →  Ordenação  →  Matriz 2D ordenada  →  Busca binária
```

1. **Leitura**: o usuário define o tamanho (linhas × colunas) e preenche os valores.
2. **Achatamento**: a matriz 2D é convertida em um vetor 1D.
3. **Ordenação**: o vetor é ordenado por **Insertion Sort**.
4. **Reconstrução**: os valores ordenados voltam para a matriz 2D.
5. **Busca binária**: o algoritmo trabalha como se a matriz fosse um vetor, usando o mapeamento:

```cpp
linha  = meio / colunas;
coluna = meio % colunas;
```

## ✨ Destaques

- 🔁 Comparação entre a **busca tradicional** (força bruta, mantida comentada no código) e a **busca binária**
- 🧮 **Mapeamento 1D ↔ 2D** com divisão e módulo
- 📍 Retorna a **posição exata** `[linha][coluna]` do elemento
- 🥇 Em valores repetidos, encontra a **primeira ocorrência**
- 🌐 Interface em português no terminal

## 📊 Comparação de desempenho

| Etapa | Complexidade |
|---|---|
| Busca tradicional | O(n · m) |
| Busca binária (após ordenar) | O(log(n · m)) |
| Ordenação (Insertion Sort) | O((n · m)²) |

> 💡 A busca binária compensa quando a matriz é **ordenada uma vez** e **consultada várias vezes**.

## 🚀 Como executar

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/Projeto-Busca-em-Matrizes.git

# Entre na pasta
cd Projeto-Busca-em-Matrizes

# Compile
g++ main.cpp -o busca

# Execute
./busca
```

## 💻 Exemplo de uso

```
Informe quantas linhas haverá na matriz: 2
Informe quantas colunas haverá na matriz: 3
...
MATRIZ COM VALORES ORGANIZADOS:
1   3   5
7   9   12

Qual valor você quer buscar na matriz? 9
Elemento encontrado na posição [2][2]
```

## 🤝 Contribuições

Sugestões são bem-vindas! Abra uma *issue* ou envie um *pull request*.

## 👤 Autor

Feito por **[Gabriel Minatel]** · [LinkedIn](https://www.linkedin.com/in/gabriel-gibertone-minatel-335b943a6/) · [GitHub](https://github.com/gabriel-minatel-tech)

⭐ Gostou do projeto? Deixe uma estrela!
