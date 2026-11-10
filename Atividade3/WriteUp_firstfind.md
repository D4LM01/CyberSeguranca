## Resolução

O exercício fornece um arquivo compactado chamado `files.zip`, contendo diversas pastas e arquivos.

O enunciado solicita especificamente que encontremos o arquivo `uber_secret.txt`.

Utilizando o terminal do sistema operacional **Kali Linux**, podemos executar o seguinte comando para localizar o arquivo:

```bash
find . -name "uber_secret.txt"
```

Esse comando realiza uma busca recursiva a partir do diretório atual, procurando por arquivos com o nome especificado.

Também seria possível encontrar o arquivo explorando manualmente as pastas. Após a busca, descobrimos que ele está localizado no seguinte caminho:

```text
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber_secret.txt
```

Ao acessar o arquivo, encontramos a seguinte flag:

```text
academy{f1nd_15_f457_ab443fd1}
```

**Flag encontrada:** `academy{f1nd_15_f457_ab443fd1}`
