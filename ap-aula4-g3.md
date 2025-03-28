# **Requisito Funcional 04**

> De acordo com os requisitos funcionais especificados no arquivo do [Cenário Problema](ap-aula2-g3.md), o requisito funcional 04 define: Deve ser possível cadastrar fornecedores e registrar pedidos de reposição.

---

## **1 - Descrição detalhada do requisito**

O sistema deve permitir o cadastro, gerenciamento e consulta de fornecedores, armazenando informações essenciais como razão social, CNPJ, endereço, telefone, e-mail e lista de produtos fornecidos. Além disso, o sistema deve possibilitar a criação, edição, e acompanhamento de pedidos de reposição de estoque, vinculando-os aos fornecedores cadastrados.

Para garantir um fluxo eficiente de reposição de mercadorias, o sistema deve permitir que usuários qualificados criem pedidos de reposição com base no estoque atual, histórico de vendas e prazos de entrega dos fornecedores. O pedido deve conter detalhes como:

- Cadastrar Fornecedor baseado em dados fornecidos pelo cartão CNPJ da RFB;
    
- Identificação do fornecedor cadastrado;
    
- Realizar o pedido de reposição, informando a lista de produtos e quantidade e fornecedor;
    
- Data do pedido;
    
- Lista de produtos solicitados (com quantidade e valor unitário);
    
- Prazo estimado de entrega;
    
- Status do pedido (pendente, aprovado, enviado, recebido, cancelado).
    

Após a criação do pedido, o sistema deve registrar o histórico e possibilitar seu acompanhamento. Quando o pedido for entregue, o estoque do supermercado deve ser atualizado automaticamente.

---

## **2 - Identificação das fontes dos requisitos**

Os requisitos foram levantados a partir das seguintes fontes:

- **Gestores de Compras**: Responsáveis pelo planejamento de reposição de estoque e negociação com fornecedores.
    
- **Equipe de Estoque**: Necessidade de monitoramento do nível de produtos e solicitação de reposição automática.
    
- **Funcionários de Atendimento**: Necessidade de evitar rupturas de estoque e garantir a disponibilidade dos produtos para os clientes.
    
- **Fornecedores**: Possibilidade de integração para recebimento automático de pedidos via e-mail ou API.
    
- **Normas Fiscais e Contábeis**: Regras para emissão de pedidos de compra e integração com documentos fiscais.
    

---

## **3 - Interesse dos Stakeholders**

O interesse dos stakeholders nesse requisito está diretamente ligado à eficiência operacional, redução de rupturas de estoque e otimização do fluxo de compras.

- **Gestores de Compras**: Desejam um sistema ágil para gerenciar fornecedores e pedidos, evitando atrasos e otimizando negociações.
    
- **Equipe de Estoque**: Precisa de um meio confiável para solicitar reposições, garantindo a disponibilidade de produtos.
    
- **Funcionários de Atendimento**: Querem evitar frustrações dos clientes devido à falta de produtos essenciais.
    
- **Fornecedores**: Interesse na automação do recebimento de pedidos e na melhoria da comunicação com o supermercado.
    
- **Administração da Empresa**: Busca controle e transparência nos processos de compra e estoque, reduzindo desperdícios e custos operacionais.
    

---

## **4 - Levantamento do Requisito por Entrevista**

Para obter informações detalhadas sobre a necessidade de cadastro de fornecedores e pedidos de reposição, foi realizada uma entrevista com **Carlos Silva**, gestor de compras do supermercado.

### **Entrevista com Carlos Silva (Gestor de Compras)**

**Entrevistador:** Quais são os principais desafios no processo de reposição de estoque hoje?

**Carlos Silva:** Atualmente, enfrentamos problemas com fornecedores que atrasam entregas e dificuldades em monitorar quando e quais produtos precisam ser repostos. Além disso, a falta de integração entre o estoque e os pedidos gera atrasos e risco de falta de produtos essenciais.

**Entrevistador:** Como você imagina que um sistema poderia resolver esses problemas?

**Carlos Silva:** Seria ideal ter um sistema que automatizasse a sugestão de pedidos com base no estoque e no histórico de vendas. Além disso, o cadastro eficiente de fornecedores ajudaria a organizar contatos e prazos de entrega.

**Entrevistador:** Existe alguma funcionalidade essencial que você acredita que não pode faltar?

**Carlos Silva:** O controle de status dos pedidos é essencial, para que possamos acompanhar se o fornecedor já enviou ou se há algum atraso. Também seria interessante um alerta para reposições urgentes.

**Entrevistador:** Como os fornecedores poderiam se beneficiar desse sistema?

**Carlos Silva:** Se tivermos integração via e-mail ou API para enviar os pedidos automaticamente, os fornecedores poderiam agilizar o processamento e reduzir erros.

Com base nessa entrevista, ficou evidente a necessidade de um sistema que integre estoque, pedidos e fornecedores de forma automatizada, garantindo eficiência e controle no processo de reposição de mercadorias.

---

## **5 - Fluxos de Execução**

### **Fluxo Principal – Cadastro de Fornecedores**

1. Usuário acessa a tela de cadastro de fornecedores.
    
2. Preenche as informações obrigatórias: razão social, CNPJ, endereço, telefone, e-mail e produtos fornecidos.
    
3. Confirma o cadastro.
    
4. O sistema valida os dados e armazena o fornecedor no banco de dados.
    

### **Fluxo Alternativo – Edição de Fornecedores**

1. Usuário seleciona um fornecedor cadastrado.
    
2. Altera os dados desejados.
    
3. Confirma as alterações.
    
4. O sistema valida e atualiza as informações.
    

### **Fluxo Principal – Registro de Pedido de Reposição**

1. Usuário acessa a tela de pedidos de reposição.
    
2. Seleciona um fornecedor cadastrado.
    
3. Insere os produtos desejados, com quantidade e valor unitário.
    
4. Define a data de entrega estimada.
    
5. Confirma o pedido.
    
6. O sistema registra o pedido e o disponibiliza para acompanhamento.
    

### **Fluxo Alternativo – Aprovação de Pedido (se necessário)**

1. Usuário com perfil de gestor acessa a lista de pedidos pendentes.
    
2. Avalia o pedido e pode aprová-lo ou rejeitá-lo.
    
3. Se aprovado, o pedido segue para envio ao fornecedor.
    
4. Se rejeitado, o sistema registra a justificativa.
    

### **Fluxo Principal – Recebimento de Pedido e Atualização de Estoque**

1. Usuário acessa a tela de pedidos e localiza um pedido com status "Enviado".
    
2. Confirma a chegada dos produtos e confere quantidades.
    
3. O sistema registra o recebimento e atualiza automaticamente o estoque.
    
4. O status do pedido muda para "Recebido".
    

---

## **6 - Perfis de Usuários com Permissão de Execução**

|**Perfil**|**Ações Permitidas**|
|---|---|
|**Gestor de Compras**|Cadastro e edição de fornecedores, criação e aprovação de pedidos de reposição, consulta de pedidos e fornecedores.|
|**Funcionário do Estoque**|Criação de pedidos de reposição, consulta de pedidos, confirmação de recebimento e atualização do estoque.|
|**Administrador do Sistema**|Controle total sobre fornecedores e pedidos, incluindo edição e exclusão de registros.|
