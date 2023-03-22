#   Erros Encontrados

1 - Regra de Negócio: Se o admin for direcionado para as informações da empresa sem nenhuma alteração no código, quando tentar acessar as vendas ou os produtos causará a Exceção java.lang.NullPointerException, pois ele tentará pegar os dados da empresa logada, porém o admin não contém os mesmos parâmetros que uma empresa, então irá causar esse erro.

2 - Código : Quando logado como admin, não é possível ver as informações da empresa, e sim do cliente. Por esta razão, quando tenta realizar uma compra, ele irá dar o erro Java.lang.IndexOutOfBounds, pois, ele varre a lista de clientes até encontrar um cliente com o nome correspondente do usuário logado. Como o usuário admin não é um cliente, ele ultrapassa o tamanho da sua lista, causando o problema.

3 - Código: o Saldo não é alterado refletindo as taxas, pois, a empresa recebe o valor total (bruto).

4 - Boas práticas: Formatação de casas decimais de um número real.

5 - Estrutura de Dados: Tudo estava em um método só, causando muita perda de tempo na hora de encontrar partes específicas do código ou reparar um erro.

6 - Experiência do usuário: Toda operação que o usuário realiza, volta para a tela de login.

7 - Experiência do usuário: Opção "voltar".


# Soluções

1 e 2 - Para resolver o problema do usuário admin, eu imaginei que ele teria acesso a todas as informações de todas as empresas, então, criei um método que irá listar todas as vendas e produtos organizada da mesma forma que das informações das empresas, a única diferença, é que os dados não são separados pelo id.

3 - Antes de apresentar o valor, eu subtraí o total pela comissão e depois setei o valor da empresa.

4 - Formatei a quantidade de casas decimais dos preços e valores e interpolei Strings utilizando printF

5 - Para deixar o código mais organizado, eu separei ele em 3 métodos simples, cada um deles redireciona para as informações dos respectivos usuários logados. Exemplo: login: cliente, será redirecionado para o método acessoCliente e irá aparecer as suas respectivas opções.

6 - Com o código separado por métodos, ao invés de redirecionar para o inicio (método executar), eu redirecionei para as opções do respectivo usuário logado.

7 - Adicionei o a opção "voltar" quando ela é necessária.

# Melhorias

Melhorei visualmente todas as partes, separando mais as informações umas das outras e diferenciando opções home com * e as outras com -.


