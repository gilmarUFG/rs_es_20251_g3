
## 1. Técnicas para Especificação de Requisitos

A especificação de requisitos é uma etapa essencial no desenvolvimento de sistemas, pois define com precisão o que o sistema deve realizar. A escolha de técnicas adequadas contribui para que os requisitos sejam compreendidos por todas as partes interessadas e sirvam de base para o projeto e a implementação do software. A seguir, apresento duas técnicas amplamente utilizadas:

### 1.1. Histórias de Usuário (User Stories)

**Descrição:**  
Histórias de Usuário são descrições breves e simples de funcionalidades do ponto de vista do usuário final. Elas seguem o formato:

> *Como um(a)* `<tipo de usuário>`, *eu quero* `<realizar uma ação>` *para que* `<benefício ou objetivo>`.

**Cenários em que são aplicáveis:**
- Projetos com metodologias ágeis como Scrum ou XP;
- Ambientes com requisitos mutáveis ou em constante refinamento;
- Quando o foco principal é a entrega de valor ao usuário final;
- Para fomentar a colaboração entre equipe de desenvolvimento e stakeholders.

**Vantagens:**
- Simples e fáceis de entender, mesmo por stakeholders não técnicos;
- Priorizam o valor entregue ao usuário;
- Facilitam o planejamento incremental e adaptativo;
- Incentivam a comunicação entre os envolvidos.

**Desvantagens:**
- Podem ser superficiais para funcionalidades mais complexas;
- Exigem critérios de aceitação bem definidos para evitar ambiguidade;
- Não abordam requisitos não funcionais diretamente;
- Difíceis de escalar sem uso de épicos e temas em projetos maiores.

---

### 1.2. Casos de Uso (Use Cases)

**Descrição:**  
Casos de Uso descrevem como um ator (usuário ou sistema externo) interage com o sistema para alcançar um objetivo específico. Eles detalham os fluxos de eventos (principal, alternativos e de exceção) necessários para que a funcionalidade seja concluída com sucesso.

**Cenários em que são aplicáveis:**
- Projetos que requerem análise funcional detalhada;
- Sistemas com múltiplas interações entre usuários e o sistema;
- Quando se deseja modelar comportamentos esperados do sistema;
- Base para derivação de casos de teste e planejamento da interface.

**Vantagens:**
- Documentam de forma completa as interações do sistema;
- Ajudam na validação de requisitos funcionais;
- São úteis para equipes técnicas, analistas e testadores;
- Auxiliam na derivação de cenários de teste.

**Desvantagens:**
- Podem ser complexos e exigir muito tempo de elaboração;
- A formalidade pode dificultar o entendimento para partes não técnicas;
- O excesso de detalhes pode antecipar decisões de implementação;
- Em métodos ágeis, podem ser considerados burocráticos.

---

## 2. Especificação de Requisitos

A seguir, apresento dois requisitos do sistema com base nos cenários definidos, utilizando as duas técnicas descritas:

### Requisito A: Sugestões para Economia de Energia  
**Técnica Utilizada:** História de Usuário

**ID:** HU001  
**Título:** Sugestões de Economia de Energia  
**História de Usuário:**

> *Como um* usuário do sistema de gerenciamento de energia,  
> *eu quero* receber sugestões automáticas baseadas nos meus hábitos de consumo,  
> *para que* eu possa reduzir o consumo de energia e economizar na conta de luz.

**Critérios de Aceitação:**
1. O sistema deve monitorar os padrões de consumo do usuário.
2. As sugestões devem ser personalizadas com base nesses padrões.
3. As sugestões devem ser exibidas de forma clara na interface do sistema.
4. O usuário pode indicar se considerou a sugestão útil ou já implementada.
5. O sistema deve atualizar periodicamente as sugestões conforme novos dados forem coletados.

---

### Requisito B: Notificação sobre Alta nos Preços da Energia  
**Técnica Utilizada:** Caso de Uso

**ID:** CU002  
**Nome:** Notificar Períodos de Alta nos Preços de Energia  

**Atores:**
- Usuário do Sistema
- Sistema de Tarifação de Energia

**Descrição:**  
Este caso de uso descreve como o sistema informa o usuário sobre aumentos no preço da energia, especialmente em horários de pico ou durante bandeiras tarifárias desfavoráveis.

**Pré-condições:**
- O usuário está cadastrado e ativou o recebimento de notificações.
- O sistema tem acesso a dados atualizados sobre tarifas energéticas.

**Pós-condições:**
- O usuário é informado sobre o período de alta.
- O envio é registrado no sistema.

**Fluxo Principal:**
1. O sistema detecta a ativação de um período com tarifa elevada.
2. Identifica os usuários que optaram por receber notificações.
3. Gera uma mensagem com a informação da tarifa e o período de vigência.
4. Envia a notificação para os canais escolhidos pelo usuário (push, e-mail).
5. Registra o envio no histórico.

**Fluxo Alternativo:**
- Nenhum usuário habilitado: o sistema encerra a ação sem enviar notificações.

**Fluxo de Exceção:**
- Falha na obtenção da tarifa: o sistema registra o erro e não envia a notificação para evitar informações imprecisas.
- Falha no envio: o sistema tenta outro canal (se disponível) e registra o erro.

---
