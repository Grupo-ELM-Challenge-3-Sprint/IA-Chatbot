# IA-Chatbot
Repositório de IA &amp; Chatbot

SimplesHC: Chatbot de Atendimento para Pacientes do Hospital das Clínicas (HC)
Link Google Planilhas: https://docs.google.com/spreadsheets/d/1DaC9nGiU56OksQXOjvVcqF_MFBWDUESGcYgiNph7gO0/edit?usp=sharing

MEMBROS DO GRUPO:
Enzo Okuizumi RM 561432
Lucas Barros RM 566422
Milton Marcelino RM 564836

--------------------------------------------------------------------------------

1. DESCRIÇÃO GERAL DO DATASET

Este arquivo descreve o dataset de Perguntas e Respostas Frequentes (FAQ) criado para o treinamento de uma Inteligência Artificial conversacional (chatbot). O dataset está no formato CSV e é composto por 104 exemplos, estruturados em três colunas: "pergunta", "resposta" e "intent".


2. ADERÊNCIA AO TEMA DO DESAFIO

O desafio proposto é "criar ferramentas/maneiras para auxiliar aqueles com dificuldade em utilizar o celular na saúde digital", com o objetivo de "diminuir a taxa de absenteísmo de 20% para <10%".

Este dataset adere 100% ao tema ao fornecer a base de conhecimento para um chatbot, que é uma ferramenta digital de fácil interação e acessível. O conteúdo foi estrategicamente focado em resolver as principais dúvidas que levam um paciente a faltar em uma consulta ou exame.

Os dados abordam diretamente as causas do absenteísmo através de categorias (rótulos) como:
- `absenteismo_consequencias`: Informa ao paciente a importância de não faltar.
- `localizacao_hc`: Ajuda o paciente a não se perder no complexo hospitalar.
- `preparo_exames`: Garante que o paciente chegue ao hospital apto a realizar o procedimento.
- `documentos_obrigatorios`: Evita que o paciente perca a viagem por falta de um documento.
- `tecnologia_ajuda`: Oferece alternativas para pacientes com dificuldades em usar ferramentas digitais, como o portal online.


3. DETALHAMENTO DOS DADOS

3.1. Fonte e Método de Coleta
Os dados foram construídos pela equipe do projeto através de um processo metodológico de pesquisa e curadoria. O método consistiu nas seguintes etapas:
1.  Levantamento de Requisitos: A equipe realizou um brainstorming para mapear a jornada do paciente do SUS no Hospital das Clínicas e identificar as principais dúvidas e dificuldades que contribuem para o absenteísmo.
2.  Pesquisa e Validação: Foram consultadas fontes de informação públicas do HCFMUSP para validar os procedimentos, endereços e regras gerais do complexo hospitalar, garantindo a acurácia das respostas.
3.  Criação e Aumento de Dados (Data Augmentation): A partir de perguntas-base para cada categoria, a equipe gerou um conjunto expandido de variações que simulam a linguagem natural de um paciente. Este processo incluiu a criação de exemplos com linguagem coloquial, diferentes construções frasais e terminologias populares (ex: "cartão amarelo"), a fim de aumentar a robustez e a capacidade de generalização do futuro modelo de IA.
4.  Curadoria Manual: Todo o conjunto de dados passou por uma etapa final de revisão e refinamento manual pela equipe para assegurar a alta qualidade, a clareza das respostas e a perfeita adequação ao contexto do hospital e do desafio.

3.2. Estrutura e Significado dos Dados
O dataset está organizado em um arquivo CSV com as seguintes colunas:
- `pergunta`: Contém a frase (utterance) que simula a dúvida de um usuário/paciente. Para cada intenção, foram criadas múltiplas variações desta pergunta.
- `resposta`: Contém a resposta padrão, clara e informativa que o chatbot deve fornecer ao identificar a intenção do usuário.
- `intent`: É o rótulo (label) que classifica a intenção principal por trás da pergunta do usuário. Este é o campo mais importante para o treinamento do modelo de NLU (Natural Language Understanding).

3.3. Quantidade e Qualidade
- **Quantidade:** O dataset final é composto por 104 pares de pergunta-resposta, distribuídos em 8 intenções distintas.
- **Qualidade:** A qualidade do dataset foi uma prioridade. As perguntas foram "humanizadas" para incluir linguagem coloquial, abreviações e diferentes construções frasais, aumentando a robustez do futuro modelo. As respostas foram elaboradas para serem acessíveis, diretas e acionáveis, evitando jargões técnicos.

3.4. Rótulos (Intents)
Os dados foram classificados com 8 rótulos (intents) principais, que representam as categorias de dúvidas dos pacientes:
- `agendamento_remarcar`: Dúvidas sobre como alterar a data de consultas ou exames.
- `absenteismo_consequencias`: Questões sobre as implicações de faltar a um agendamento.
- `tecnologia_ajuda`: Pedidos de ajuda para usar as ferramentas digitais do hospital (portal/app).
- `documentos_obrigatorios`: Dúvidas sobre quais documentos levar no dia do atendimento.
- `resultados_exames`: Perguntas sobre como acessar os resultados de exames.
- `localizacao_hc`: Dúvidas de localização e como navegar pelo complexo do HC.
- `custos_sus`: Perguntas sobre a gratuidade dos serviços prestados pelo SUS.
- `preparo_exames`: Dúvidas sobre jejum e outros preparos necessários para procedimentos.

3.5. Características Importantes
- **Linguagem Acessível:** O vocabulário utilizado é simples e direto, pensado para um público amplo, incluindo pessoas com baixa literalidade digital ou idosos.
- **Contexto Específico:** O conteúdo menciona termos e locais próprios do Hospital das Clínicas (InCor, ICr, PAMB, "cartão amarelo"), tornando o chatbot um especialista no ambiente do HC.
- **Foco na Resolução:** Cada resposta foi pensada para não apenas informar, mas guiar o paciente sobre qual ação tomar, visando a autossuficiência e a redução da ansiedade.


4. OBJETIVO DE USO DO DATASET

O objetivo principal deste dataset é servir como base de treinamento e validação para um modelo de Inteligência Artificial de Processamento de Linguagem Natural (PLN).

Ao treinar um modelo com estes dados, pretende-se criar um chatbot capaz de:
1.  Compreender as perguntas mais comuns dos pacientes do HC, mesmo que feitas de maneiras variadas.
2.  Fornecer respostas padronizadas, corretas e úteis de forma instantânea, 24/7.
3.  Reduzir a carga de trabalho do atendimento humano, liberando os funcionários para casos mais complexos.
4.  Atingir o objetivo final do desafio: diminuir a taxa de absenteísmo ao empoderar o paciente com informação clara e acessível, removendo barreiras que o impediriam de comparecer à sua consulta ou exame.
