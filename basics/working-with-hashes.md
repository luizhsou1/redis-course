## Trabalhando com Hashes

**Armazenar valores do tipo hash**
\> HSET resultado:24-05-2020:megasena "numeros" "13, 15, 22, 28, 43, 48"
\> HSET resultado:24-05-2020:megasena "ganhadores" 23

**Buscar valores do tipo hash a partir da chave e campo**
\> HGET resultado:24-05-2020:megasena "numeros"
\> HGET resultado:24-05-2020:megasena "ganhadores"

**Remover chaves/campos**
\> HDEL resultado:24-05-2020:megasena "numeros"
\> HDEL resultado:24-05-2020:megasena "ganhadores"
