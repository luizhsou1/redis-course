## Quem acessou meu sistema

**Marcar que um usuário específico acessou meu site**
\> SETBIT acesso:29-05-2020 27 1
\> SETBIT acesso:29-05-2020 43 1
\> SETBIT acesso:29-05-2020 56 1
\> SETBIT acesso:29-05-2020 12 1

**Verificar se um usuário acessou meu sistema**
\> GETBIT acesso:29-05-2020 45 (result: 0)
\> GETBIT acesso:29-05-2020 27 (result: 1)

**Verificar quantos acessos teve em um dia**
\> BITCOUNT acesso:29-05-2020

**Quem acessou meu sistema no dia 28 e 29 de maio de 2020**
\> BITOP AND acesso:28-e-29-05-2020 acesso:28-05-2020 acesso:29-05-2020 (BIT OPERATOR)

Posteriormente rode:
\> GETBIT acesso:28-e-29-05-2020 \$ID_USER (Para saber se um usuário especifico acessou nos dois dias)
\> BITCOUNT acesso:28-e-29-05-2020 (Para saber quantos usuários acessaram nos dois dias)

**Quem acessou no final, pode ser que acessou no sábado ou domingo**
\> BITOP OR acesso:23-e-24-05-2020 acesso:23-05-2020 acesso:24-05-2020 (BIT OPERATOR)

Posteriormente rode:
\> GETBIT acesso:23-e-24-05-2020 \$ID_USER (Para saber se um usuário especifico acessou ou sábado ou domingo)
\> BITCOUNT acesso:23-e-24-05-2020 (Para saber quantos usuários acessaram ou sábado ou domingo)
