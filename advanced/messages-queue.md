## Uma fila de espera de emails e mensagens para serem enviadas

Coloca alguma coisa na fila até que alguém consiga atender ela, atender a fila da esquerda para a direita.

\> RPUSH "fila:confirma-email" "luizhsou1@gmail.com"
\> RPUSH "fila:confirma-email" "luiz.hsouza97@gmail.com"
\> RPUSH "fila:confirma-email" "luizhsouza97@outlook.com"

\> LPOP fila:confirma-email (Arrasca o elemento mais da esquerda da fila, no caso o luizhsou1@gmail.com)

\> BLPOP fila:confirma-email 10 (Arranca o elemento da fila, caso não tenha e já se passou 10 segundos encerra o pedido, retornando nil)
\> BLPOP fila:confirma-email 0 (Arranca o elemento da fila, caso não tenha espera infinitamente até que se tenha um elemento para arrancar da fila)
