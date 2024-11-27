# Chatbot de Personagens
Este projeto implementa um chatbot baseado em árvore de conhecimento que responde a perguntas sobre personagens fictícios. Ele usa técnicas de processamento de linguagem natural (NLP) e manipulação de árvores para estruturar dados e gerar respostas.

## ⚙️ Como Funciona
O chatbot utiliza uma estrutura de árvore para organizar informações de personagens. Cada nó representa uma categoria (entidade) ou um detalhe específico (intenção). Ao receber uma pergunta, o chatbot:

* Tokeniza e processa o texto para identificar palavras importantes.
* Identifica **Entidades** e **Intenções**, mapeando-as na estrutura da árvore.
* Busca **Respostas** na árvore, retornando informações armazenadas.
* Se necessário, realiza consultas externas (como a contagem de personagens).

## 🛠️ Principais Componentes
* **Árvore de Conhecimento**: Representa as entidades e intenções organizadas hierarquicamente.
* **Extração de Entidades e Intenções**: Filtra e processa perguntas usando o modelo `UnigramTagger` e stemming.
* **Consulta no DataFrame**: Permite respostas dinâmicas, como a contagem de personagens.

## 🖥️ Como Rodar a Aplicação
* Python 3.7+
* Instale as dependências com:
  ```bash
  pip install nltk pandas

## Passos

* Baixe o repositório ou clone com:
    ```bash
    git clone https://github.com/DiegoH3nr1que/chatbot_project

    cd chatbot_project

### Execute o notebook Jupyter:
 * execute as células para inicializar a árvore, carregar os dados e interagir com o chatbot.

## 📦 Dependências

* NLTK: Utilizado para tokenização, stemming e taggers.
* Pandas: Para manipulação de tabelas e dados tabulares.

### Instale as dependências necessárias com:

```bash

pip install nltk pandas

```

## 🔄 Fluxograma de Funcionamento

Segue um fluxograma para ilustrar o funcionamento do chatbot:

1° Usuário faz uma pergunta.

2° A pergunta é processada (tokenização e stemming).

3° Entidades e intenções são extraídas.

4° O chatbot busca a resposta na árvore:

* Se a resposta for uma mensagem armazenada, é retornada ao usuário.

* Se a resposta for uma consulta dinâmica uma função é acionada.
Resposta é retornada ao usuário.

``` mermaid
graph TD
    A[Usuário faz uma pergunta] --> B[Processamento de texto]
    B --> C[Tokenização e Stemming]
    C --> D[Identificar Entidades]
    C --> E[Identificar Intenções]
    D --> F[Busca na Árvore]
    E --> F
    F --> G{Resposta Encontrada?}
    G -->|Sim| H[Enviar Resposta ao Usuário]
    G -->|Não| I[Consulta Externa]
    I --> H
```

O fluxograma acima ilustra o funcionamento do chatbot, desde a recepção da pergunta até o envio da resposta ao usuário.

## ✨ Exemplo de Uso

### Entrada
* Usuário pergunta: "Quem é o irmão da Cassandra?"

### Processamento
* Entidade identificada: Cassandra
* Intenção identificada: irmão

### Resposta
"O irmão de Cassandra é o Professor Charles Xavier, líder dos X-Men, com quem ela compartilha uma conexão telepática e um histórico conflituoso."

