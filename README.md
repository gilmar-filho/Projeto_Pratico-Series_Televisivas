# Projeto Prático de Séries Televisivas

Este é um projeto feito na linguagem C++ para manipular uma base de dados de séries televisivas. O objetivo é fornecer uma interface ao usuário e permitir algumas ações como busca, adição, remoção e ordenação de dados.

## Integrantes
Este projeto foi desenvolvido para a disciplina de Introdução aos Algoritmos pelos alunos:
    [x] Gilmar Silva de Medeiros Filho
    [x] Hugo Dias Pontello
    [x] João Miguel Chaves Fernandes

## Descrição do Projeto
O código funciona mediante um arquivo .csv que contém dados variados sobre diversas séries televisivas. No arquivo se encontra informações como: Nome da série; 
Ano de Lançamento; Personagem Principal e seu Ator; Quantidade de Visualizações na Estreia; Aprovação do Público; e Gênero. 
(Obs_1.: Os dados são apenas para fins de uso no código, podem não corresponder à realidade.)
O programa inicia dando opções de busca, inserção, impressão, ordenação dos dados, remoção, lixeira e encerramento ao usuário. 
Conforme o usuário escolhe o que deseja fazer, o programa vai dando opções para que se chegue ao resultado desejado.
(Obs_2.: Programa escrito em Linux, talvez tenha problemas ao ser rodado em Windows!)
A seguir há uma breve explicação de cada função do código.

• Int main:
Reservamos a int main para escrita e exibição dos dados, tentamos tirar a maioria das 
operações da int main e transformá-las em funções para aumentar sua legibilidade e deixar mais 
fácil a manutenção do código.

• Função int procedimento:
Função onde estão as opções iniciais que o usuário pode realizar com o programa. Essa 
função retorna para a main o valor correspondente a operação desejada pelo usuário.

• Função void perguntas:
Função onde estão as perguntas e opções que aparecem para o usuário enquanto roda o 
programa. Colocamos essa função pra “limpar” a main.

• Função void gravacao_em_registro:
Função responsável pela leitura inicial e básica dos dados que foram incrementados 
através do arquivo, possui um laço de repetição para leitura de todos os dados do arquivo .csv 
em um vetor de registros.

• Função void arquivo_binario:
Função que salva todos os dados do vetor de registros em um arquivo binário.

• Função void shell_sort:
Função responsável pela ordenação eficiente dos dados por meio da técnica “Shell 
Sort”. Realiza a ordenação por Nome (para realizar a busca binária em outra função), por 
Visualizações na Estreia e Aprovação do Público (essas duas últimas de acordo com o que for 
pedido pelo usuário).

• Função void busca_binária_nome:
Função que realiza a busca binária por Nome da série. Caso o dado procurado não exista 
no arquivo, será exibida a mensagem: “Dado inexistente no banco de dados!”;

• Função void busca:
Função responsável pela busca por Gênero da série. Caso não sejam encontrados, a 
mensagem “Dado inexistente no banco de dados!” será exibida.

• Função void redimensionar:
Função responsável pelo redimensionamento do vetor de registros.

• Função void remoção:
Função responsável por remover um dado do arquivo. Essa função recebe o nome da 
série que o usuário deseja remover e faz uma busca sequencial pela série. Caso encontrado, 
atualiza o identificador da série com uma chave negativa (-1) e troca a posição com o último
dado.

• Função void inserção:
Função responsável por inserir novos dados escritos no terminal diretamente no arquivo 
binário, mensagens como “Nome:” e “Ano de lançamento:” são exibidas ao longo da execução 
do código para guiar e facilitar o processo do usuário que pretende realizar a inserção. Após a 
inserção dos novos dados, o usuário terá a opção de “Imprimir” ou “Salvar em um arquivo .csv” 
os dados do arquivo binário.

• Função void impressao:
Função responsável pela impressão dos dados do arquivo solicitados pelo usuário, a 
impressão vai exibir todos os dados daquela parte do arquivo, ou seja, identificador, nome, data, 
personagem, visualizações, aprovação e gênero. 

• Função void salvar_csv:
Função responsável pelo salvamento dos dados do arquivo binário em um arquivo .csv, 
que pode ser tanto o mesmo utilizado pela leitura inicial tanto quanto um novo, com o nome 
informado pelo usuário

• Função int quantRemoFuncao:
Funcão que realiza a contagem de dados com chave negativa (-1), ou seja, dados removidos pelo
usuário. Essa função é especialmente para as funções lixeira e restauracao, para otimizar e 
deixar o código mais limpo.

• Função void lixeira:
Função responsável por mostrar para o usuário os dados que foram removidos e dar as opções de
restauração.

• Função void restauracao:
Função que restaura os dados da lixeira mediante a vontade do usuário.
