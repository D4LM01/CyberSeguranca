# AES-128 ECB — Análise e Descriptografia

## Analisando o enunciado

A questão fornece as seguintes informações:

* **Algoritmo utilizado:** AES-128
* **Modo de operação:** ECB
* **Tamanho da chave:** 16 caracteres
* **Chave:** `cybersecurity!!!`
* **Conteúdo interceptado:** `rpX3wOcHdoOHpWzRTPjVBdHx5oUPCZfC2w0hPkuLQOI=`

> **Observação:** o conteúdo interceptado está codificado em **Base64**.

---

## Decodificando o conteúdo

Primeiramente, utilizamos o site [dCode — Base64 Encoding](https://www.dcode.fr/base-64-encoding) para decodificar o conteúdo em Base64 para **Hexadecimal**.

O resultado obtido foi:

```text
AE 95 F7 C0 E7 07 76 83 87 A5 6C D1 4C F8 D5 05
D1 F1 E6 85 0F 09 97 C2 DB 0D 21 3E 4B 8B 40 E2
```

Em seguida, utilizamos o [CyberChef](https://gchq.github.io/CyberChef/) para realizar a descriptografia utilizando **AES Decrypt**.

### Configuração do AES Decrypt

| Campo              | Valor                                                                                             |
| ------------------ | ------------------------------------------------------------------------------------------------- |
| **Input**          | `AE 95 F7 C0 E7 07 76 83 87 A5 6C D1 4C F8 D5 05 D1 F1 E6 85 0F 09 97 C2 DB 0D 21 3E 4B 8B 40 E2` |
| **Key**            | `cybersecurity!!!`                                                                                |
| **Key Encoding**   | `LATIN1`                                                                                          |
| **Mode**           | `ECB/NoPadding`                                                                                   |
| **Input Encoding** | `Hex`                                                                                             |
| **Output**         | `Raw`                                                                                             |
| **IV from Input**  | `OFF`                                                                                             |

O modo **ECB** não utiliza IV, por isso não é necessário fornecer um vetor de inicialização.

---

## Resultado

Após realizar a descriptografia, obtemos a seguinte **flag**:

```text
DUCK{AES_is_symmetric_crypto}
```

### Flag

> **DUCK{AES_is_symmetric_crypto}**
