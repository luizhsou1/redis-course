## As últimas notícias

Listas das últimas notícias

**Listas, ordenação e limites**
\> LPUSH ultimas_noticias "HTML qualquer com a notícia 1" (Adiciona na esquerda da lista movendo todos os outros para uma posição mais a direita)
\> LINDEX ultimas_noticias 3 (Pega o quarto elemento da lista)
\> LLEN ultimas_noticias (Quantidade de elementos da lista)
\> LRANGE ultimas_noticias 0 2 (Pega as 3 primeiras notícias, da posição 0 até a posição 2)
