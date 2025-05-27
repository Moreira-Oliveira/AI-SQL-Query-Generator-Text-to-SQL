# AI-SQL-Query-Generator-Text-to-SQL

🚀 Visão Geral

🛠 Objetivo: Desenvolver uma aplicação que utiliza Inteligência Artificial (IA) para transformar descrições em linguagem natural (português) em queries SQL prontas para execução, facilitando a vida de analistas de dados, desenvolvedores e profissionais de negócios que não dominam SQL.

🧩 Funcionalidades Principais:

* Geração automática de queries SQL a partir de texto em português.

* Explicação detalhada da sintaxe SQL gerada.

* Exemplo de saída esperada (dados simulados).

* Opção de download da query em formato .sql.

🧩 Tecnologias:

* Backend: Python (Streamlit, Gemini API)

* IA: Modelo Gemini (Google AI) para processamento de linguagem natural.

* Gerenciamento de Ambientes: Anaconda (Conda)


🧰 Configuração do Projeto

Pré-requisitos

* Python 3.12+

* Anaconda (opcional, mas recomendado para gerenciamento de ambientes)

* Conta no Google AI Studio (para acessar a API do Gemini


🔍 Implementação

Para reproduzir o projeto é preciso criar uma chave AAAPI oferecidaa gratuitamente pelo Google, paraa acessar o o LLM Gemini. Para poder criá-la é só acessar esse site https://ai.google.dev/gemini-api/docs/api-key?hl=pt-br (Será necessário efetuar login com sua conta do Google).

![image](https://github.com/user-attachments/assets/518e05d4-613d-43c5-89b8-cf2f79345bcf)


Após isso vamos colocar ele no arquivo oculto .env que vai esta nos arquivos que estou deixando aqui nesse projeto.

![image](https://github.com/user-attachments/assets/841a6129-c5b8-4e29-89d7-f4773380d232)


🛠 Com tudo pronto vamos começar:

* Abra o terminal ou prompt de comando, navegue até a pasta com os arquivos e execute o comando abaixo para criar um ambiente virtual:

conda create --name projetosqlaigenerator python=3.12

* Ative o ambiente:

conda activate dsasqlaigenerator (ou: source activate dsasqlaigenerator)

* Instale o pip e as dependências:

conda install pip
pip install -r requirements.txt 

* Execute o comando abaixo e acesse a app pelo navegador.

streamlit run projeto_ai_app.py

🔍 Após executar streamlit run projeto_ai_app.py, com base no código se dará nesse rerumo do Fluxo da Aplicação:

1. Inicialização do Servidor Streamlit:

* Um servidor web local será iniciado (geralmente em http://localhost:8501).

* Uma interface gráfica (UI) será aberta automaticamente no seu navegador.

2. Interface do Usuário (UI):

* Título: "projeto AI SQL Query Generator" (Text-to-SQL).

* Subtítulo: "Eu sou um assistente de IA customizado e vou gerar templates de queries SQL para você!".

* Área de Texto: Onde o usuário descreve, em português, a query SQL desejada (ex: "Crie uma query para calcular a média de vendas por mês").

* Botão: "Gerar Query SQL".

3. Processamento pela IA (Gemini):

📌 Quando o usuário clica no botão:

* O texto em português é enviado para o modelo Gemini 2.0 Flash via API.

* A IA gera:

3.1 Query SQL (ex: SELECT AVG(vendas) FROM tabela GROUP BY mes).

3.2 Exemplo de Saída (tabela fictícia com dados simulados).

3.3 Explicação da Sintaxe (descrição das cláusulas SQL usadas).

4. Exibição dos Resultados:

📌 Os resultados são organizados em abas na interface:

* Aba 1: Código SQL gerado (com syntax highlighting).

* Aba 2: Saída esperada (exemplo de dados em formato de tabela).

* Aba 3: Explicação técnica (para aprendizado do usuário).

5. Download da Query:

* Um botão "Baixar Resultado" permite salvar a query SQL + explicação em um arquivo .sql.

6. Sidebar (Barra Lateral):

* Contém instruções de uso e um botão de "Suporte" (que exibe um e-mail fictício de contato).

✅ E assim temos isso:

Tela Inicial
![image](https://github.com/user-attachments/assets/5a680630-3022-4f3b-b053-fba0d0514b1e)


COnsulta SQL
![image](https://github.com/user-attachments/assets/d732dfa9-91f4-4656-b3fe-87eae674274a)


Saída Esperada
![image](https://github.com/user-attachments/assets/65646c8c-b67c-4e5c-b88a-458e01abde23)


Explicação
![image](https://github.com/user-attachments/assets/65b4cfbb-4acf-46e5-97ee-e4a68753854c)


📚 Conclusão do Projeto

Este projeto demonstra como a Inteligência Artificial pode simplificar e acelerar a criação de queries SQL, tornando-a acessível até mesmo para quem não tem expertise em bancos de dados. Ao combinar o poder do Gemini (Google AI) com uma interface amigável (Streamlit), desenvolvemos uma ferramenta que:

✅ Traduz linguagem natural em SQL: Basta descrever o que você precisa em português, e a IA gera a query pronta para uso.

✅ Ensina enquanto executa: Além do código, a aplicação explica a sintaxe e mostra exemplos de saída, funcionando como um tutor de SQL.

✅ É fácil de configurar e usar: Com poucos comandos, qualquer pessoa pode rodar a aplicação localmente.

📚 Impacto e Aplicações Práticas

* Para analistas de dados: Elimina a necessidade de memorizar funções SQL complexas.

* Para equipes comerciais: Permite extrair insights de bancos de dados sem depender de desenvolvedores.

* Para educação: Ótimo recurso para estudantes aprenderem SQL na prática.

📚 Limitações e Melhorias Futuras

📌 A precisão da IA depende da clareza do prompt do usuário.

📌 Seria interessante adicionar:

* Suporte a mais bancos de dados (MySQL, BigQuery, etc.).

* Validação automática de queries.

* Histórico de consultas geradas.

📚 Considerações Finais

Este projeto não é apenas um gerador de SQL, mas um assistente inteligente que reduz a barreira entre a necessidade do usuário e a complexidade técnica. Com ajustes e expansões, pode se tornar uma ferramenta indispensável para qualquer pessoa que trabalhe com dados.

# "Transforme perguntas em queries e dados em insights — com um simples texto." 🚀

# Pronto para testar? Execute streamlit run projeto_ai_app.py e comece a gerar suas queries agora mesmo!




