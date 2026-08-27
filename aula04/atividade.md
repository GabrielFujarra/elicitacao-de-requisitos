# Sua vez de elicitar — Elicitação de Requisitos
 
Sistema de vendas por telefone/presencial, com três processos: **registro de pedidos** (vendedores), **cadastro/remoção de produtos** (administrador) e **controle de estoque** (time de estoque).
 
---
 
## 1. Processo: Registro de pedidos (Vendedores)
 
**Requisito 1.** O sistema deve permitir que o vendedor registre um novo pedido informando cliente, produtos, quantidades e canal de venda (telefone ou presencial).
- **Fonte 1.** Entrevista com o vendedor. Fonte humana, nível operacional, classe de usuário vendedor.
- **Fonte 2.** Entrevista com o gerente comercial. Fonte humana, nível tático, classe de usuário gerente.
- **Fonte 3.** Sistema de vendas atualmente usado pela empresa. Fonte não humana, categoria sistema legado.
**Requisito 2.** O sistema deve validar a disponibilidade em estoque do produto antes de confirmar o pedido.
- **Fonte 1.** Entrevista com o time de estoque. Fonte humana, nível operacional, classe de usuário estoquista.
- **Fonte 2.** Política de vendas e reserva de estoque. Fonte não humana, categoria documentação.
- **Fonte 3.** Observação (job shadowing) do atendimento telefônico. Fonte humana, nível operacional, classe de usuário vendedor.
**Requisito 3.** O sistema deve gerar um número/protocolo único para cada pedido registrado, permitindo consulta posterior.
- **Fonte 1.** Entrevista com o vendedor. Fonte humana, nível operacional, classe de usuário vendedor.
- **Fonte 2.** Análise de sistemas concorrentes de gestão de pedidos. Fonte não humana, categoria concorrência.
- **Fonte 3.** Norma/regulamento fiscal sobre emissão de comprovantes de venda. Fonte não humana, categoria norma.
---
 
## 2. Processo: Cadastro e remoção de produtos (Administrador)
 
**Requisito 1.** O sistema deve permitir que o administrador cadastre um novo produto com nome, descrição, preço, categoria e código identificador único.
- **Fonte 1.** Entrevista com o administrador. Fonte humana, nível operacional, classe de usuário administrador.
- **Fonte 2.** Planilha atual de catálogo de produtos. Fonte não humana, categoria sistema legado.
- **Fonte 3.** Entrevista com o diretor comercial sobre estratégia de catálogo. Fonte humana, nível estratégico, classe de usuário diretoria.
**Requisito 2.** O sistema deve permitir a remoção (ou inativação) de um produto, impedindo sua remoção caso existam pedidos pendentes associados a ele.
- **Fonte 1.** Entrevista com o administrador. Fonte humana, nível operacional, classe de usuário administrador.
- **Fonte 2.** Entrevista com o time de estoque sobre produtos descontinuados. Fonte humana, nível operacional, classe de usuário estoquista.
- **Fonte 3.** Documentação de regras de integridade referencial do sistema legado. Fonte não humana, categoria sistema legado.
**Requisito 3.** O sistema deve permitir a edição dos dados de um produto já cadastrado, mantendo um histórico das alterações de preço.
- **Fonte 1.** Entrevista com o administrador. Fonte humana, nível operacional, classe de usuário administrador.
- **Fonte 2.** Política comercial de reajuste de preços. Fonte não humana, categoria documentação.
- **Fonte 3.** Benchmark de sistemas concorrentes de catálogo de produtos. Fonte não humana, categoria concorrência.
---
 
## 3. Processo: Controle de estoque (Time de estoque)
 
**Requisito 1.** O sistema deve dar baixa automática na quantidade em estoque de um produto assim que um pedido for confirmado.
- **Fonte 1.** Entrevista com o estoquista. Fonte humana, nível operacional, classe de usuário estoquista.
- **Fonte 2.** Fluxo de processo atual de baixa manual em planilha. Fonte não humana, categoria sistema legado.
- **Fonte 3.** Entrevista com o vendedor sobre o impacto de estoque desatualizado na venda. Fonte humana, nível operacional, classe de usuário vendedor.
**Requisito 2.** O sistema deve permitir o registro de entradas de estoque (reposição), informando fornecedor, quantidade e data de recebimento.
- **Fonte 1.** Entrevista com o supervisor de estoque. Fonte humana, nível tático, classe de usuário supervisor.
- **Fonte 2.** Nota fiscal/documento de recebimento de fornecedor. Fonte não humana, categoria documentação.
- **Fonte 3.** Norma contábil sobre controle de entrada de mercadorias. Fonte não humana, categoria norma.
**Requisito 3.** O sistema deve emitir um alerta quando a quantidade de um produto em estoque atingir um nível mínimo definido.
- **Fonte 1.** Entrevista com o estoquista. Fonte humana, nível operacional, classe de usuário estoquista.
- **Fonte 2.** Entrevista com a diretoria sobre metas de nível de serviço e ruptura de estoque. Fonte humana, nível estratégico, classe de usuário diretoria.
- **Fonte 3.** Análise de sistemas concorrentes de gestão de estoque. Fonte não humana, categoria concorrência.
