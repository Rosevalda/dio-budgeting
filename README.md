# 🤖 Budgeting API with Spring AI - Projeto Final

Uma API inteligente desenvolvida com **Spring Boot** e **Spring AI** para gerenciamento de orçamentos pessoais. A aplicação processa comandos de voz, faz transcrição de áudio, entende a intenção do usuário utilizando modelos de linguagem (LLM) e executa ações reais no sistema via *Tool Calling* (como criar ou consultar transações financeiras).

> 📌 **Projeto desenvolvido durante o Desafio de Projeto da Trilha Spring Boot da Digital Innovation One (DIO).**

---

## 🎯 Objetivo do Projeto

O foco desta aplicação é conectar recursos de **Inteligência Artificial Generativa** com uma arquitetura Java robusta e pronta para produção. Mais do que gerar respostas em texto, a API é capaz de transformar chamadas de áudio em dados estruturados e interagir com a camada de persistência de dados.

---

## 🔄 Fluxo Principal da API

1. **Recepção do Áudio:** O cliente envia um arquivo de áudio (ex: `.mp3` ou `.wav`) contendo um comando de voz (ex: *"Gastei 50 reais com almoço hoje"*).
2. **Transcrição (Audio-to-Text):** O Spring AI envia o áudio para o modelo de transcrição (Whisper / OpenAI).
3. **Processamento e Intenção:** O texto é analisado pelo `ChatClient` do Spring AI.
4. **Tool Calling (Execução de Função):** A IA reconhece a intenção e aciona a ferramenta Java correspondente para criar ou consultar registros no banco de dados.
5. **Persistência de Dados:** A transação financeira é validada e gravada via Spring Data JPA.
6. **Resposta Final:** A API retorna a confirmação formatada em texto (e/ou áudio) para o usuário.

---

## 🛠️ Tecnologias Utilizadas

* **Java 25**
* **Spring Boot 3.2.x**
* **Spring AI** (Integração com OpenAI / ChatClient / Tool Calling)
* **Spring Data JPA** (Persistência)
* **MySQL / H2 Database**
* **Gradle** (Gerenciador de dependências)


---

## 🧠 Aprendizados

Durante este desafio, aprendi e pratiquei:

* Como configurar e gerenciar dependências do **Spring AI** com repositórios de Milestone.
* O conceito e a implementação de **Tool Calling (Function Calling)** para permitir que LLMs invoquem rotinas no backend Java.
* Integração de modelos multimodais (transcrição de áudio e geração de texto).
* Organização de arquitetura limpa em projetos Java combinando Spring Boot e IA.
