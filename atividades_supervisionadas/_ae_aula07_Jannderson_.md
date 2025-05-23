Universidade Federal de Goiás   
Aluno: Jannderson Oliveira  
Professor: Gilmar Arantes  
Requisito de Sotware

## **Checklist-Based Reading**

### **Descrição**

Checklist-Based Reading é uma técnica de verificação e validação de requisitos baseada em uma lista de verificação padronizada, contendo perguntas ou critérios a serem analisados durante a leitura dos requisitos. Os revisores seguem a lista para avaliar a qualidade dos requisitos.

### **Cenários de Aplicação**

Ambientes onde há necessidade de padronizar a revisão de documentos.

Equipes com níveis variados de experiência, onde a lista ajuda a manter a consistência.

Projetos com grande volume de requisitos, onde a sistematização facilita a análise.

### **Vantagens**

Padronização da análise, evitando omissões importantes.

Facilidade de uso, mesmo por revisores com pouca experiência.

Cobertura sistemática de critérios importantes (ex: completude, ambiguidade, consistência).

###  **Desvantagens**

A qualidade da revisão depende da qualidade da checklist.

Pode haver uma falsa sensação de segurança, negligenciando aspectos não listados.

Pode ser menos eficaz para detectar problemas contextuais ou subjetivos.

##   **Inspeção Formal**

### **Descrição**

A Inspeção Formal é uma técnica estruturada de revisão de requisitos baseada em um **processo detalhista**, com **papéis definidos** (moderador, autor, leitor, registrador) e etapas formais como **planejamento, preparação, reunião de inspeção, retrabalho e follow-up**. Baseia-se no modelo de Fagan Inspection.

###  **Cenários de Aplicação**

Projetos críticos que exigem alta confiabilidade e rastreabilidade.

Ambientes que seguem normas de qualidade como CMMI, ISO/IEC 12207, DO-178C.

Situações onde é necessário documentar formalmente o processo de revisão.

###  **Vantagens**

Alta eficácia na detecção de falhas nos requisitos.

Processo bem documentado e controlado, ideal para auditorias e certificações.

Promove compartilhamento de conhecimento entre os membros da equipe.

###  **Desvantagens**

Custo elevado em tempo e recursos.

Complexidade organizacional (necessita de treinamento e definição de papéis).

Pode ser considerado burocrático para equipes ágeis ou pequenas.

### **Requisito 1 – Técnica: Checklist-Based Reading**

Requisito:  
 "O sistema deve calcular o consumo de energia de cada aparelho com base na potência informada (em watts) e no tempo de uso diário, fornecendo o consumo total em kWh por dia para cada equipamento."

**Aplicação da Técnica:**

O requisito é claro e compreensível? Sim, é compreensivel 

Define as entradas (potência, tempo de uso) e saídas (consumo em kWh)? SIm, descreve como deve ser feito e os detalhes técnicos

Está dentro do escopo do sistema? Sim, é um requisito de alta necessidade

É testável/verificável? Sim

Evita termos ambíguos? Sim, não possue ambiquidades

Não depende de outro requisito para compreensão? Sim, depende do requisito que exige fornecimento de relatórios.

### **Requisito 2 – Técnica: Inspeção Formal**

Requisito:  
 "O sistema deve permitir ao usuário visualizar o consumo diário de energia e apresentar gráficos comparativos entre os dias da semana, destacando variações no padrão de consumo."

**Aplicação da Técnica:**

**Etapas seguidas:**

**Leitura individual do requisito** pelos inspetores;

**Reunião de inspeção**, conduzida por um moderador, na qual o leitor apresenta o requisito e os inspetores apontam:

A necessidade de detalhar como será feita a visualização (ex.: tipos de gráfico);

Ambiguidade na expressão "destacando variações";

Sugestão de incluir exemplos ou critérios de variação;

**Relatório final**, registrando as observações e ajustes a serem feitos.

###  **Referências**

* Sommerville, I. (2011). *Software Engineering* (9th ed.). Pearson Education.

* IEEE Std 830-1998. *Recommended Practice for Software Requirements Specifications*.


  
