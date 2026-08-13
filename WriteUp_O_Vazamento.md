# Analise do Enunciado

A questão nos fornece inicialmente as seguintes informações

* Hash exposto: `ef92b778bafe771e89245b89ecbc08a44a4e166c06659911881f383d4473e94f`
* Arquivo executável: `desafio_1`

Note que `desafio_1` é um executável ELF 64-bit para Linux.

## Quebrando o Hash

Utilizando o site [CrackStation](https://crackstation.net) e fornecendo o hash exposto, o site identifica automaticamente o tipo do hash e fornece o resultado:

* Tipo: `sha256`
* Resultado: `password123`

## Utilizando o Executável

Ao iniciar o arquivo executável fornecido pelo exercício, ele pede uma senha. A senha sendo o resultado do hash que acabamos de encontrar (`password123`).

## Encontrando a Flag

Após inserir a senha, o executável nos devolve a Flag:

```text
DUCK{Th1s_1s_the_c0rr3ct_passw0rd}
```
