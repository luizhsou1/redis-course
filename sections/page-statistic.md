## Estastísticas de uma página

**Colocar o número de acesso a página contatos no dia 29-05-2020**
\> INCR pagina:/contato:29-05-2020 (Também posso decrementar com DECR)

**Incrementar em caso de vendas e decrementar em caso de devolução o valor total de vendas do dia 29-05-2020**
\> INCRBY vendas:/contato:29-05-2020:valor 15 (Venda)
\> DECRBY vendas:/contato:29-05-2020:valor 23 (Devolução)
\> INCRBY vendas:/contato:29-05-2020:valor 55 (Venda)

Obs.: Assim só soma inteiros

**Incrementar em caso de vendas e decrementar em caso de devolução o valor total de vendas do dia 29-05-2020**
\> INCRBYFLOAT vendas:/contato:29-05-2020:valor 15 (Venda)
\> DECRBYFLOAT vendas:/contato:29-05-2020:valor 23 (Devolução)
\> INCRBYFLOAT vendas:/contato:29-05-2020:valor 55 (Venda)

Obs.: Faz mais sentido nesse contexto operar floats
