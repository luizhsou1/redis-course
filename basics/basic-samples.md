## Exemplos básicos

**SET $CHAVE $VALOR**
(Atribui um valor a uma chave, onde valor pode ser vários tipos, strings, números, arrays, objetos complexos...)

**DEL \$CHAVE**
(Deleta uma determinada chave)

> **Exemplos**

## Instalação no linux ou Mac

\> SET "antepenultimo_sorteio" "13, 16, 32, 35, 38, 47"

**Jeito Melhor de armazenar**
\> SET "resultado:29-05-2020:megasena" "2, 15, 18, 30, 35, 42"

\> SET "resultado:22-05-2020:megasena" "14, 17, 18, 25, 32, 41"

\> SET "resultado:15-05-2020:megasena" "13, 16, 32, 35, 38, 47"

Agora temos um padrão para buscar pelo Comando: KEY

**Jeito Ainda Melhor de armazenar**
\> MSET "resultado:29-05-2020:megasena" "2, 15, 18, 30, 35, 42" "resultado:22-05-2020:megasena" "14, 17, 18, 25, 32, 41" "resultado:15-05-2020:megasena" "13, 16, 32, 35, 38, 47"

Além do padrão, precisamos ir apenas uma vez no redis para armazenar todas as chaves

**Buscar todas as chaves que começam com resultado**
\> KEYS "resultado\*"

**Buscar todas as chaves que começam com resultado e sejam de maio de 2020**
\> KEYS "resultado:\*-05-2020:megasena"

**Buscar todas as chaves que começam com resultado e sejam de 20 de maio a 29 de maio de 2020**
\> KEYS "resultado:2?-05-2020:megasena"

**Pegar o resultado do sorteio do dia 29-08-2020**
\> GET "resultado:29-05-2020:megasena"

**Buscar todas as chaves que o dia termina com 2 ou 5**
\> KEYS "resultado:?[25]-??-????:megasena"
