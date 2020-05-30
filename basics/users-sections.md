## Seções de usuários

Por exemplo pode querer manter durante 30 min os produtos do carrinho de usuário em um redis, esse redis pode ser compartilhado entre os n hosts da minha aplicação, pensando em uma aplicação maior com várias instâncias. Só isso já tiraria a carga do meu banco.

**Setar Informações do usuário**
\> HMSET "sessao:usuario:1675" "nome" "Luiz Henrique" "sessao:usuario:1675" "total_produtos" "3" "sessao:usuario:1675" "sobrenome" "de Souza"

**Setar Informações do usuário depois de 30 min**
\> EXPIRE "sessao:usuario:1675" 1800

Uma boa seria toda vez que ele acessa a página, ganha mais 30 minutos

**Verificar quanto tempo falta**
\> TTL "sessao:usuario:1675" 1800
