# Cenário Problema

Um supermercado possui um gerenciamento de estoque 100% manual, o que demanda muito trabalho e gera desperdício de tempo por parte dos funcionários, que precisam atualizar o estoque manualmente em um caderno. Buscando uma solução para esse problema, o supermercado entrou em contato com uma empresa de software para desenvolver um sistema de gerenciamento de estoque.

---

## Requisitos Funcionais

- **RF-01:** O sistema deve permitir cadastro e atualização automática de produtos.
- **RF-02:** Deve haver um controle de validade dos produtos, com alertas de vencimento.
- **RF-03:** O sistema deve gerar relatórios de entrada e saída de mercadorias.
- **RF-04:** Deve ser possível cadastrar fornecedores e registrar pedidos de reposição.
- **RF-05:** O sistema deve permitir que funcionários registrem reposições e baixas de estoque por meio de um terminal ou aplicativo.

---

## Requisitos Não Funcionais

- **RNF-01:** O sistema deve garantir alta disponibilidade, com tempo de inatividade inferior a 1% ao mês.
- **RNF-02:** As informações de clientes e transações devem ser armazenadas de forma segura, seguindo as normas da LGPD.
- **RNF-03:** O sistema deve oferecer uma interface amigável e responsiva, acessível por dispositivos móveis e desktops.
- **RNF-04:** O sistema deve ser capaz de processar pelo menos 500 transações simultâneas sem degradação de performance.
- **RNF-05:** Os dados devem ser armazenados em um banco de dados relacional com backups automáticos diários.

---

## Regras de Negócio

- **RN-01:** Controle de Validade dos Produtos:
  - O sistema não deve permitir a venda de produtos com prazo de validade expirado.
  - O sistema deve alertar o usuário sobre lotes de produtos que estejam a menos de 30 dias da data de vencimento.

- **RN-02:** Reposição Automática de Estoque:
  - O sistema deve fazer pedidos automáticos de lotes de produtos que estejam próximos de esgotar.

- **RN-03:** Controle de Entrada e Saída de Mercadorias:
  - O sistema deve registrar a entrada de produtos com base na nota fiscal de compra e gerar um acréscimo no estoque.
  - O sistema deve realizar um decréscimo no estoque quando houver saída (venda).

- **RN-04:** Vendas Acima de R$ 5.000,00:
  - Devem ser aprovadas manualmente por um gerente.

- **RN-05:** Gestão de Múltiplos Fornecedores:
  - O sistema deve permitir o acesso aos principais fornecedores de produtos da região.
  - Deve permitir filtragem por distância e localização.

