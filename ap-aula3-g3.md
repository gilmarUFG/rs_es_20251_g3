# **Requisito Funcional 04**

> De acordo com os requisitos funcionais especificados no arquivo [[ap-aula2-g3]], o requisito funcional 04 define: Deve ser possível cadastrar fornecedores e registrar pedidos de reposição.

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

## **3 - Fluxos de Execução**

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

## **4 - Perfis de Usuários com Permissão de Execução**

|**Perfil**|**Ações Permitidas**|
|---|---|
|**Gestor de Compras**|Cadastro e edição de fornecedores, criação e aprovação de pedidos de reposição, consulta de pedidos e fornecedores.|
|**Funcionário do Estoque**|Criação de pedidos de reposição, consulta de pedidos, confirmação de recebimento e atualização do estoque.|
|**Administrador do Sistema**|Controle total sobre fornecedores e pedidos, incluindo edição e exclusão de registros.|