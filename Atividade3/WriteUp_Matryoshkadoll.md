## Resolução

O exercício fornece um arquivo JPG contendo a imagem de uma boneca Matrioska, um brinquedo tradicional russo conhecido por possuir outras bonecas progressivamente menores armazenadas umas dentro das outras.

![Imagem](imagens)

Seguindo essa lógica, enviamos a imagem para o site [Aperi'Solve](https://aperisolve.fr/). Na aba **PCRT (PNG Check & Repair Tool)**, conseguimos extrair um arquivo contendo outra imagem semelhante, porém um pouco menor, com o nome `2_c.jpg`.

Repetimos o mesmo processo mais três vezes, seguindo a lógica das bonecas Matrioskas, até encontrar um arquivo chamado `flag.txt`.

Ao abrir o arquivo, encontramos a seguinte flag:

```text
academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}
```

**Flag encontrada:** `academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}`
