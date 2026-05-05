# Projeto Prático de Séries Televisivas

Este projeto, desenvolvido em C++, gerencia uma base de dados de séries televisivas. Através de uma interface de linha de comando, o usuário pode realizar diversas operações de manipulação de dados, como busca, inserção, remoção e ordenação.

## Integrantes
Desenvolvido para a disciplina de Introdução aos Algoritmos por:
- [Gilmar Silva de Medeiros Filho](https://github.com/gilmar-filho)
- [Hugo Dias Pontello](https://github.com/DPontello)
- João Miguel Chaves Fernandes

## Sobre o Projeto
O programa lê dados de séries a partir de um arquivo `.csv`, contendo informações como nome, ano de lançamento, personagem principal, visualizações, aprovação e gênero. A partir daí, o usuário pode interagir com um menu para manipular esses dados.

> **Nota:** Os dados no arquivo `serie.csv` são ilustrativos e podem não corresponder à realidade.

## Funcionalidades
- **Busca**: Pesquisar séries por nome (usando busca binária) ou por gênero (busca sequencial).
- **Inserção**: Adicionar uma ou mais séries ao banco de dados.
- **Impressão**: Listar todos os dados ou um intervalo específico de registros.
- **Ordenação**: Ordenar os dados por visualizações na estreia ou por aprovação do público, em ordem crescente ou decrescente (usando Shell Sort).
- **Remoção**: Mover uma série para a "lixeira", marcando-a como removida.
- **Lixeira**: Visualizar séries removidas e restaurá-las individualmente, em grupo ou todas de uma vez.
- **Persistência**: Salvar todas as alterações em um novo arquivo `.csv` ou sobrescrever o original.

## Pré-requisitos
- Um compilador C++ (ex: g++).
- O arquivo de dados `serie.csv` presente no mesmo diretório do executável.

## Como Compilar e Executar

1.  Abra um terminal no diretório do projeto.
2.  Compile o código-fonte:
    ```bash
    g++ projeto_pratico-series_televisivas-v12.cpp -o series_manager
    ```
3.  Execute o programa:
    ```bash
    ./series_manager
    ```

## Estrutura de Arquivos
- `projeto_pratico-series_televisivas-v12.cpp`: O código-fonte principal do projeto.
- `serie.csv`: Arquivo de entrada com os dados das séries. A primeira linha é um cabeçalho informativo, a segunda contém o número de registros, e as linhas seguintes contêm os dados de cada série, separados por `;`.
- `series_binario.dat`: Arquivo binário gerado e utilizado pelo programa para operações internas e para manter o estado entre as execuções das funcionalidades.

## Observação de Compatibilidade
O programa foi desenvolvido e testado em um ambiente Linux. Pode haver problemas de compatibilidade ao compilar e executar em outros sistemas operacionais, como o Windows, principalmente devido ao uso do comando `system("clear")`.