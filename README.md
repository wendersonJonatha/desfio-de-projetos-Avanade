# desfio-de-projetos-Avanade

Projeto DIO: Busca Inteligente com Azure Cognitive Search
Este projeto tem como objetivo demonstrar a utilização do Azure Cognitive Search em conjunto com AI Search para indexar e consultar dados relacionados ao desafio da DIO. A solução emprega habilidades cognitivas (AI Skills) para enriquecer os dados, proporcionando uma experiência de busca avançada e insights valiosos. O projeto é uma excelente adição ao portfólio, destacando habilidades em cloud computing e inteligência artificial.

Sumário
Visão Geral

Configuração do Ambiente no Azure

Definição do Índice de Busca

Processo de Indexação

Enriquecimento de Dados com AI Skills

Realizando Consultas

Aprendizados e Insights

Expansões Futuras

Como Contribuir

Licença

Visão Geral
O Azure Cognitive Search é uma ferramenta poderosa para criar soluções de busca inteligente. Neste projeto, exploramos como configurar um serviço de busca, indexar dados e aplicar habilidades cognitivas para enriquecer as informações. O resultado é uma aplicação capaz de realizar consultas avançadas, filtrar resultados e extrair insights de forma eficiente.

Configuração do Ambiente no Azure
Passos para Configuração
Criação do Serviço:

Acesse o Azure Portal.

Crie um recurso do tipo Azure Cognitive Search.

Anote o endpoint e a chave de API, que serão usados para interagir com o serviço.

Pré-Requisitos:

Uma conta ativa no Azure.

Azure CLI instalado e configurado.

Ambiente de desenvolvimento preparado (Python, Node.js, etc.).
Definição do Índice de Busca
O índice é a estrutura que define como os dados serão organizados e pesquisados. Ele contém campos que podem ser pesquisáveis, filtráveis ou classificáveis.

Exemplo de Definição de Índice (JSON)
(´´

{
  "name": "desafio-dio-index",
  "fields": [
    {
      "name": "id",
      "type": "Edm.String",
      "key": true,
      "filterable": true
    },
    {
      "name": "titulo",
      "type": "Edm.String",
      "searchable": true
    },
    {
      "name": "descricao",
      "type": "Edm.String",
      "searchable": true
    },
    {
      "name": "dataCriacao",
      "type": "Edm.DateTimeOffset",
      "filterable": true,
      "sortable": true
    }
  ]
}´´´)

Processo de Indexação
Após definir o índice, os dados são enviados para o Azure Cognitive Search. Isso pode ser feito via API REST ou SDKs disponíveis.

Exemplo de Upload de Dados em Python


