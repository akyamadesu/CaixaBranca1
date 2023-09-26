# CaixaBranca1
Caixa branca - teste 1

- Erro #1 - A tentativa de integração com o driver do MySQL estava com o nome errado:
Class.forName("com.mysql.Driver.Manager").newInstance();

Ao invés disso, tentar:
Class.forName("com.mysql.cj.jdbc.Driver").newInstance();

1. A DOCUMENTAÇÃO FOI DESCRITA NO CÓDIGO?
  Não há nenhuma espécie de comentário dentro do código.

2. AS VARIÁVEIS E CONSTANTES POSSUEM BOA NOMENCLATURA?
  Sim, cada uma delas levam um nome autoexplicativo como "login", "senha", etc.

3. EXISTEM LEGIBILIDADE E ORGANIZAÇÃO NO CÓDIGO?
  Poderia ser adicionado alguns espaçamentos ou até mesmmo comentários para ajudar no entendimento e na legibilidade.
  
4. TODOS OS NULLPOINTERS FORAM TRATADOS?
  Não há tratamento explícito para NullPointerExceptions. Isso significa que, se algum objeto (como conn, st, rs) for nulo em algum momento, isso pode causar uma exceção em tempo de execução. 
  
5. A ARQUITETURA UTILIZADA FOI DEVIDAMENTE RESPEITADA?
  Não há uma arquitetura específica mencionada no código, mas parece estar seguindo um fluxo de pprocedimento.
  
6. AS CONEXÕES UTILIZADAS FORAM FECHADAS?
   Não há chamadas para conn.close(), o que pode resultar em vazamentos de conexão. É importante fechar as conexões após o uso para liberar recursos
