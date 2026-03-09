# 📚 Chatbot Inteligente para Análise de Documentos PDF

## 📌 Visão Geral do Projeto

Este projeto tem como objetivo desenvolver um sistema de busca inteligente utilizando inteligência artificial generativa, embeddings e buscas vetorizadas. Ele foi construído para atuar como um assistente virtual focado em compreender, processar e responder perguntas com base em uma base de conhecimento proprietária (arquivos PDF).

O cenário prático deste projeto simula a rotina de um estudante que está escrevendo um Trabalho de Conclusão de Curso (TCC) e precisa revisar e correlacionar diversos artigos científicos, extraindo informações relevantes e citações de forma rápida e eficiente.

## 🎯 Objetivos Alcançados

- ✅ Carregamento e processamento de artigos em formato PDF [17].
- ✅ Implementação de um sistema de busca vetorial utilizando o **Azure AI Search** para indexar as informações .
- ✅ Utilização do modelo **GPT-4o** via **Azure AI Foundry** para gerar respostas fundamentadas nos documentos.
- ✅ Criação de um ambiente de interações conversacionais contextualizadas aos arquivos carregados.

## 🚀 Resumo da Experiência

Durante o desenvolvimento do projeto, o foco foi estruturar o fluxo de conversão de dados não estruturados (PDFs) para uma base de dados vetorizada [4]. A experiência de integrar o Armazenamento de Blobs e o AI Search com o modelo GPT-4o proporcionou _insights_ valiosos sobre como as tecnologias de RAG (Retrieval-Augmented Generation) operam na prática.

**Nota sobre as interações:** Os testes, validações e interações com os arquivos vetorizados foram realizados **exclusivamente no ambiente do Playground do Azure AI Foundry**. A interface do Playground mostrou-se totalmente satisfatória para enviar as perguntas, validar as citações (referências dos PDFs) e extrair os resumos e correlações entre os autores necessários para a construção do projeto.

## 📖 Como Implementar

Para replicar este projeto, consulte o nosso guia completo com o passo a passo:
👉 **[Guia de Implementação da Solução](guia.md)**

## 📸 Screenshots do Processo

Abaixo estão os registros visuais de cada etapa do desenvolvimento hospedados na pasta `screenshots` do repositório:

1. **Criação do Recurso AI Foundry:**
   ![Recurso AI Foundry Criado](/screenshots/recurso%20do%20ai%20foundry%20criado.png) _Visão geral do Hub criado no Azure._

2. **Implantação do Modelo:**
   ![Implantando GPT-4o](screenshots/implantgando%20o%20gpt-4o%20no%20chat.png) _Configuração e implantação do modelo GPT-4o no projeto._

3. **Configuração dos Dados (Storage e Search):**
   ![Configuração de Blob e Search](screenshots/criado%20blob%20e%20recurso%20de%20pesquisa%20para%20indexar%20arquivos.png) _Conectando as fontes de dados do Azure._

4. **Processo de Vetorização:**
   ![Vetorizando os PDFs](screenshots/vetorizando%20os%20pdfs.png) _Revisão e conclusão da adição dos arquivos carregados._

5. **Índice Vetorial Finalizado:**
   ![Índice Vetor Criado](screenshots/indice%20vetor%20criado.png) _Playground de chat reconhecendo a base de dados indexada._

6. **Interação com Sucesso no Playground:**
   ![Resposta Satisfatória](screenshots/resposta%20satisfatório%20do%20agente%20em%20uma%20pergunda%20específica.png) _Agente respondendo corretamente a uma pergunta específica com base nos atores analisados na base de conhecimento._
