# Guia de Implementação: Chatbot Inteligente para Análise de Documentos PDF

Este guia detalha o passo a passo para construir um sistema de busca vetorial interativo capaz de responder a perguntas com base em documentos PDF, utilizando os recursos do **Azure AI Foundry**. O processo aborda desde a criação do ambiente até a interação final no Playground.

## Passo 1: Preparação do Ambiente no Azure

1. Acesse o portal do Azure e crie um recurso do **Azure AI Foundry** (Hub) selecionando o grupo de recursos desejado e a região (ex: East US 2 ou Sweden Central) .
2. Após a criação do recurso principal, acesse o portal do AI Foundry e crie um **Novo Projeto**.

## Passo 2: Implantação dos Modelos de Inteligência Artificial

Para que o chatbot funcione, você precisará de dois modelos: um para a interface de chat e outro para transformar os textos em vetores (embeddings).

1. No menu do seu projeto, acesse a área de "Modelos" e clique em implantar um modelo base .
2. Implante o modelo de linguagem **GPT-4o** (para geração de respostas e chat).
3. Implante um modelo de **Embeddings** (ex: _text-embedding-ada-002_ ou _text-embedding-3-large_), que será responsável por converter o texto dos seus PDFs em um array de números (vetores).

## Passo 3: Criação de Recursos de Armazenamento e Pesquisa

Para hospedar e indexar os PDFs, o sistema exige recursos de armazenamento e busca estruturado.

1. Crie um recurso de **Armazenamento de Blobs do Azure** (Storage Account).
2. Crie um recurso de **Pesquisa de IA do Azure** (Azure AI Search). _Dica: Você pode optar pela camada básica, mas lembre-se de excluir o recurso após os testes para evitar custos elevados_.

## Passo 4: Carregamento e Vetorização dos Arquivos

1. Acesse o **Playground de Chat** no AI Foundry.
2. Vá até a seção "Adicionar seus dados" (Add your data) e escolha a opção para carregar arquivos.
3. Selecione a assinatura correta e conecte os recursos de Armazenamento de Blobs e Pesquisa de IA criados no passo anterior.
4. Faça o upload dos seus arquivos PDF.
5. Insira um nome para o índice e inicie o processo. O modelo de embeddings transformará trechos dos seus PDFs em vetores para criar o índice semântico.

## Passo 5: Teste e Interação no Playground

1. Com o índice de vetores criado com sucesso, você poderá personalizar a mensagem de sistema (System Prompt), como por exemplo: _"Você é um especialista que irá me ajudar com dúvidas sobre o tema"_.
2. Envie perguntas específicas no chat sobre o conteúdo dos PDFs. O sistema irá buscar no índice vetorial o contexto mais próximo e utilizará o GPT-4o para redigir a resposta com as devidas citações.

_Observação: O escopo deste guia limita-se aos testes diretamente no Playground do AI Foundry, dispensando a implantação em um Web App externo._
