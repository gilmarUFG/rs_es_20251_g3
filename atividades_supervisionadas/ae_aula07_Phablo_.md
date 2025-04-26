# Casos de Uso

Casos de uso são uma técnica de modelagem funcional utilizada para capturar os requisitos funcionais de um sistema. Um caso de uso descreve interações entre um ator (usuário ou sistema externo) e o sistema, com o objetivo de alcançar um resultado específico (por exemplo: "realizar login", "emitir relatório", "cadastrar cliente").

A técnica pode ser documentada com textos estruturados ou representada graficamente usando diagramas de casos de uso (UML).

## Passo a passo:

1. **Identificação dos Atores**  
   Quem interage com o sistema? (Ex: cliente, atendente, sistema externo)

2. **Identificação dos Casos de Uso**  
   Quais são as ações que os atores podem realizar?

3. **Descrição do Fluxo Principal**  
   Passo a passo normal da execução do caso de uso.

4. **Fluxos Alternativos e de Exceção**  
   Variações e comportamentos inesperados (ex: senha incorreta, falha de conexão).

5. **Pré-condições e Pós-condições**  
   O que deve estar válido antes/depois da execução.

## Cenários de Aplicação

- Ambientes onde é importante entender a interação dos usuários com o sistema.
- Equipes que utilizam UML ou métodos de engenharia de software clássicos como RUP.
- Projetos de sistemas orientados a objetos.
- Projetos com múltiplos perfis de usuário e requisitos funcionais complexos.

## Vantagens e Desvantagens

### Desvantagens

- Limitação para requisitos não funcionais: Não cobre bem aspectos como desempenho, segurança, usabilidade.
- Foco limitado em processos internos: Foca nas interações externas, não detalha muito a lógica interna do sistema.

### Vantagens

- Clareza: Descreve de forma clara o que o sistema deve fazer.
- Foco no usuário: Foca na experiência e necessidade do usuário final.
- Facilidade de comunicação: Útil para discutir com partes interessadas não técnicas.
- Base para testes: Pode ser usado como base para criação de cenários de testes.

## Aplicação da técnica de casos de uso ao cenário:

> **“O sistema deve permitir visualização do consumo de energia separado por cômodos ou departamentos.”**

### Ator Principal

Usuário do sistema (ex: síndico, gestor, morador, administrador)

### Objetivo

Permitir que o usuário visualize o consumo de energia elétrica detalhado por cômodo (em residências) ou departamento (em ambientes corporativos), promovendo um acompanhamento mais preciso e a identificação de desperdícios.

### Pré-condições

- O usuário deve estar autenticado no sistema.
- Os sensores de monitoramento de energia devem estar devidamente configurados e vinculados a cômodos/departamentos.

### Pós-condições

- O sistema exibe as informações de consumo separadas corretamente por cômodo/departamento.
- O usuário pode acessar visualizações em gráficos ou tabelas.

### Fluxo Principal

1. O usuário acessa a área de monitoramento energético.
2. O sistema apresenta uma lista de cômodos ou departamentos cadastrados.
3. O usuário seleciona um ou mais ambientes desejados.
4. O sistema recupera os dados de consumo relacionados à seleção.
5. O sistema exibe os dados por período (diário, semanal, mensal) em formato gráfico e/ou tabular.
6. O usuário pode alternar entre tipos de visualização ou exportar os dados.

### Fluxos Alternativos e de Exceção

- **3a.** Nenhum cômodo ou departamento cadastrado:  
  O sistema exibe uma mensagem informando que não há dados disponíveis e orienta o usuário a realizar o cadastro.

- **4a.** Falha ao recuperar dados:  
  O sistema exibe uma mensagem de erro e sugere tentar novamente mais tarde.

- **5a.** Nenhum dado encontrado para o período:  
  O sistema informa que não há consumo registrado naquele período.

---

# Histórias de Usuário

Histórias de usuário são uma técnica de especificação de requisitos que descreve, de forma simples e centrada no usuário, o que ele deseja realizar com o sistema e por quê. É uma forma de capturar os requisitos funcionais em linguagem natural e acessível, geralmente escrita em um formato padrão:

> **Como [tipo de usuário], quero [algo que o usuário deseja fazer], para que [benefício ou resultado esperado]**

## Passo a passo:

1. **Identificação dos Papéis (Personas)**  
   Quem são os usuários do sistema? Quais suas necessidades e objetivos?

2. **Escrita da História**  
   Descrever a história no formato padrão.

3. **Definição dos Critérios de Aceitação**  
   Lista de condições que devem ser verdadeiras para que a história seja considerada concluída com sucesso.  
   *Exemplo:*
   - O cliente pode visualizar todos os pedidos já realizados
   - Os pedidos devem ser exibidos em ordem cronológica

4. **Estimativa da Complexidade**  
   Estimativa de esforço (story points) feita pela equipe de desenvolvimento.

## Cenários de Aplicação

- Projetos com frequente interação com o cliente
- Times que trabalham com entregas incrementais
- Ambientes que valorizam comunicação constante e foco no valor de negócio

## Vantagens e Desvantagens

### Desvantagens

- Pouco detalhamento técnico
- Ambiguidade
- Dependência de critérios de aceitação bem definidos

### Vantagens

- Foco no valor para o usuário
- Comunicação clara
- Agilidade

## Aplicação da técnica de história de usuário ao cenário:

> **“O sistema deve analisar padrões de consumo e otimizar automaticamente o uso de energia em diferentes horários.”**

### 1. Identificação dos Papéis (Personas)

- **Gestor de Energia (Empresarial ou Predial):**  
  Deseja reduzir custos com energia e receber relatórios inteligentes com sugestões de economia baseadas em dados reais de uso.

- **Morador de Residência Inteligente:**  
  Quer economizar energia automaticamente, sem precisar monitorar manualmente os horários de uso dos aparelhos.

### 2. Escrita da História

**Como** usuário do sistema,  
**Quero** que ele analise padrões de consumo de energia,  
**Para que** possa otimizar automaticamente o uso nos horários mais eficientes e reduzir desperdícios.

### 3. Definição dos Critérios de Aceitação

- O sistema deve coletar dados de consumo de energia por faixa horária.
- O sistema deve identificar padrões recorrentes (horários de maior consumo).
- O sistema deve sugerir ou aplicar ações automáticas para reduzir consumo em horários de pico.
- O usuário pode ativar ou desativar a otimização automática via painel.
- As decisões do sistema devem ser registradas com data, hora, ambiente afetado e motivo da ação.
- O sistema deve fornecer relatórios com comparativo de consumo antes/depois da otimização.

### 4. Estimativa da Complexidade

- **Story Points:** 8  
  (Alta complexidade — envolve análise de dados, integração com dispositivos controláveis, criação de lógica de automação e interface de visualização)
