Prezada Professora!


INTRODUÇÃO:

Me chamo Lucas e faço IC para um professor de arquiteura e urbanismo da UFF, participo de uma equipe de 4 pessoas em pesquisa e sou o encarregado de criar o código do projeto, feito em python.

Meu trabalho consiste em criar um modelo computacional, no qual agentes (pessoas) andem por uma cidade (matriz bidimensional), escolham lugares para visitar e vão para tais lugares.

Para determinar o caminho que os agentes irão tomar, utilizo o algoritmo do A*, visto que a matriz é composta por celúlas andavéis (celulas que compõem ruas) e não andáveis (celulas que compõem prédios).


PROBLEMAS:

O código atualmente está bem lento visto que as matrizes autilizadas são bem grandes e uso uma grande quantidade de agentes, o que necessita gerar o caminho para cada um deles.

Para otimizar o A*, vi que poderia usar uma Heap como lista aberta (lista que armazena as células ainda não testadas) para diminuir o numero de acessos na lista aberta.

em meus testes, consegui implementar um heap funcional e incroporá-lo no A*, mas por algum motivo, o número de celulas testadas não dimunuiu e não consigo entender o porquê.

Irei encaminhar uma pasta compacatada que contém todos os arquivos utilzados no programa. É necessário baixar uma única dependência externa, o pygame, que pode ser instalado por uma IDE ou usando o comando no terminal: pip install pygame.



COMO USAR:

Nesta pasta há 2 arquivos principais, o "simulação_testes".py e o "Testes_Heap.py"

"Testes_Heap.py":

-- basta digitar o número de valores (N) para serem armazenados no heap.
-- o programa irá criar N células, que contém valores aleatóros de "f".
-- as células serão adiconadas ao heap e irão ocpar seu local adequado de acordo com se valor "f".
-- será possível acompanhar o passo-a-passo do programa a medida que ele adiciona as células e depois as retira, retirando sempre a primeira célula.


"simulação_testes.py"

-- antes de inciar o programa, o código contém algumas opções que podem ser manipuladas para diferentes testes, elas incluem:
--> qnt_linhas
--> qnt_colunas
--> tamanho_celula
--> matriz_randomica
--> grid.display_linhas_grid

tanto qnt_linhas e qnt_colunas podem ser alteradas em conjunto com tamanho célula para alterar o tamanho da tela do programa.

-altura da tela = qnt_linhas * tamanho_celula.
-largura da tela = qnt_colunas * tamanho_celula.

-o componente matriz_randomica se for igual a True, irá gerar uma matriz randômica, ou seja, com alguns espaços aleatórios não andáveis.
-caso contrário, todos os espaços serão andáveis.

- o grid.display_linhas_grid = True, fornece as linhas para observar o grid (a separação das células).

-- Ao inicar o programa, uma tela contendo o grid irá abrir.
-- deve-se agora selecionar a partida (verde) e a chegada do caminho no grid, clicando o botão direito do mouse em cima da célula que deseja selecionar.
-- após a partida e chegada estarem selecionadas, outras células ao serem selecionadas (com o botão direito do mouse) irão se tornar células não andáveis.
-- pressione a barra de espaço para iniciar a procura do caminho.
-- as células marcadas de roxo simbloziam as que foram testadas para a procura do caminho, mas que não fazem parte dele.
-- as células marcadas de azul simbolizam o caminho de fato.
-- uma mensagem no terminal aparecerá informando caso o caminho não seja possível de ser realizado.
-- caso o caminho tenha sido encontrado, ele aparecerá na tela e dados sobre a procura do caminho irão aparecer no terminal.
-- após o caminho ter sido descoberto, basta selecionar novas células para testar novo caminhos.


-- há dois tipos de A* criados, a versão 1 (que pode ser encontrado no arquivo "ClasseGridAStar.py", na função "a_star) e a versão 2(arquivo "ClasseGridAStar.py", na função "a_star_v2").
-- a versão 1 não possui a optimização heap e a versão 2 possui.
-- aperte 1, quando para usar a versão 1 na procura do caminho ou aperte 2 para usar a versão 2.


Sugiro que vc realize diferentes testes, especialmente em matrizes grandes (sugrio 100x100, tamanho_celula=6 e grid.display_linhas_grid=False) para testar as diferenças no rendimentos das diferentes versões do A*.

Qualquer observação/dúvida a respeito do código pode ser mandada para o meu email: lucasmartello@id.uff.br

Não sei se será de muita ajuda, mas não guardo direitos autorais pelo código, pode usá-lo a vontade.

Agradeço pela disponibilidade e pela ajuda,


Lucas Martello Nogueira