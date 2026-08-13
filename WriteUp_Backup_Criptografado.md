# Analisando o enunciado

A questão nos fornece as seguintes informações

* O algoritmo utilizado foi AES-128
* O modo de operação foi ECB
* A chave possui 16 caracteres
* Chave: `cybersecurity!!!`
* Conteudo Interceptado: `rpX3wOcHdoOHpWzRTPjVBdHx5oUPCZfC2w0hPkuLQOI=`

note que o conteudo interceptado esta criptografado em Base64

## Decodificando

Utilizando o site [dCode — Base64 Encoding](https://www.dcode.fr/base-64-encoding), primeiramente decodificamos o código em Base64 para Hexadecimal, assim obtendo:

```text
AE 95 F7 C0 E7 07 76 83 87 A5 6C D1 4C F8 D5 05 D1 F1 E6 85 0F 09 97 C2 DB 0D 21 3E 4B 8B 40 E2
```

Agora utilizando o site [CyberChef](https://gchq.github.io/CyberChef/), selecionamos a ferramenta AES Decrypt e preenchemos os dados.

```text
Input (Texto): AE 95 F7 C0 E7 07 76 83 87 A5 6C D1 4C F8 D5 05 D1 F1 E6 85 0F 09 97 C2 DB 0D 21 3E 4B 8B 40 E2
Key: cybersecurity!!! (LATIN1)
Mode: ECB/NoPadding (pois não possuimos IV)
Input: Hex
Output: Raw
IV from input: OFF
```

## Resultado

Por fim obtendo a Flag:

```text
DUCK{AES_is_symmetric_crypto}
```
