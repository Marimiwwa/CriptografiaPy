# criptografia-python

Implementação do algoritmo de criptografia RSA em Python, feita do zero para estudar o conceito. *Projeto educacional, não use em produção.*

## O que faz
- Gera números primos grandes (teste de primalidade Miller-Rabin)
- Gera o par de chaves pública e privada
- Criptografa e descriptografa mensagens

## Como funciona
1. Obtém dois primos p e q com o teste Miller-Rabin
2. Calcula n = p * q e phi(n) = (p-1)(q-1) (função totiente de Euler)
3. Escolhe e coprimo de phi(n)
4. Calcula d, o inverso multiplicativo de e mod phi(n) (algoritmo de Euclides estendido)
5. Chave pública: (e, n). Chave privada: (d, n)
6. Cifrar: c = m^e mod n. Decifrar: m = c^d mod n

## Por que é seguro
A segurança depende da dificuldade de fatorar n em p e q. Com chave de 2048 bits, há cerca de 1,79 × 10^308 possibilidades no pior caso. Mesmo uma máquina que teste 1 bilhão por segundo levaria mais de 5 × 10^291 anos.

## Como rodar
```bash
python [arquivo.py]
