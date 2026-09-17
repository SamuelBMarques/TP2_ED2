# 📊 Estruturas de Dados II — TP2

Implementação e comparação de diferentes **algoritmos de ordenação externa**, desenvolvida em **C** para a disciplina de **Estruturas de Dados II (ED2)**.

O projeto trabalha com arquivos contendo grandes quantidades de registros e analisa o desempenho de diferentes métodos de ordenação.

---

## 🎯 Objetivo

O objetivo é comparar diferentes estratégias de **ordenação externa**, considerando:

* Número de comparações
* Número de leituras
* Número de escritas
* Tempo de execução do método
* Tempo total de execução

Os testes são realizados com diferentes quantidades de registros e diferentes organizações dos arquivos.

---

## 🔄 Métodos de ordenação

O projeto implementa três métodos:

| Método | Algoritmo                                            |
| ------ | ---------------------------------------------------- |
| `1`    | Intercalação Balanceada com QuickSort                |
| `2`    | Intercalação Balanceada com Seleção por Substituição |
| `3`    | QuickSort Externo                                    |

Os métodos são testados utilizando arquivos ordenados de forma:

* Ascendente
* Descendente
* Aleatória

---

## 📊 Testes

A bateria de testes considera diferentes quantidades de registros:

```text
100
1.000
10.000
100.000
471.705
```

Cada método é executado para as três situações de organização dos arquivos.

Os resultados são armazenados em:

```text
resultados_testes.csv
```

O script `testador.py` automatiza os experimentos e coleta as métricas de desempenho.

---

## 🛠️ Tecnologias e conceitos

* **C**
* Python
* Arquivos binários
* Ordenação externa
* QuickSort
* Intercalação Balanceada
* Seleção por Substituição
* Manipulação de arquivos
* Análise de desempenho

---

## 📁 Estrutura do projeto

```text
TP2_ED2/
│
├── include/
│   ├── quickSortExt.h
│   ├── intercalacao_balanceada.h
│   ├── conversor.h
│   └── area.h
│
├── src/
│   ├── ...
│
├── ordena
├── resultados_testes.csv
├── testador.py
├── verifica
├── verifica_perdidos
├── verifica_perdidos.c
├── Makefile
└── README.md
```

* `src/` — implementação dos algoritmos
* `include/` — arquivos de cabeçalho
* `testador.py` — automação dos testes
* `resultados_testes.csv` — resultados dos experimentos
* `Makefile` — compilação do projeto

---

## 💻 Compilação

O projeto utiliza um **Makefile** para facilitar a compilação.

```bash
make
```

Para remover os arquivos gerados:

```bash
make clean
```

---

## ▶️ Execução

O programa recebe como argumentos:

```text
./ordena <método> <quantidade> <situação> [flag]
```

Exemplo:

```bash
./ordena 1 10000 3
```

Onde:

* `método` — algoritmo de ordenação (`1` a `3`)
* `quantidade` — número de registros
* `situação` — organização do arquivo:

  * `1` — Ascendente
  * `2` — Descendente
  * `3` — Aleatória
* `[-P]` — opção para exibir os registros antes e depois da ordenação

---

## 🧪 Automação dos testes

Para executar a bateria completa de testes:

```bash
python3 testador.py
```

O script executa automaticamente todas as combinações de:

* 3 métodos
* 5 tamanhos de entrada
* 3 situações de arquivo

e salva os resultados em `resultados_testes.csv`.

---

## 📚 Contexto acadêmico

Projeto desenvolvido para a disciplina de **Estruturas de Dados II (ED2)**.

**Alunos:** Samuel Braga Marques, Gabriel Barony, Thiago Zanete, Thayllon Bragança, Marco Antônio Silva

---

## 👨‍💻 Autor

**Samuel Braga Marques**

GitHub: [@SamuelBMarques](https://github.com/SamuelBMarques)
