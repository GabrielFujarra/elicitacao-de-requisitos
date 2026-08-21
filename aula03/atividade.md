
# Atividade — Requisitos Não Funcionais (RNF) e ISO/IEC 25010
 
Para cada uma das três histórias de usuário, foram elaborados três Requisitos Não Funcionais (RNF) que reforçam a demanda descrita, cada um associado à característica correspondente da norma ISO/IEC 25010.
 
---
 
## História 1
 
**Como** cliente, **quero** avaliar o pedido depois da entrega, **para** ajudar outros clientes a escolherem melhor.
 
**Critérios de aceitação:**
- Dado que o pedido foi entregue, quando o cliente abre o app, então aparece a opção de avaliar o pedido.
- Dado que o cliente avalia com nota e comentário, quando confirma o envio, então a avaliação aparece no perfil do restaurante.
### RNFs
 
**RNF 1.1 — Desempenho**
A opção de avaliar o pedido deve ser exibida em até 2 segundos após a abertura do app, mesmo em períodos de pico de acesso.
- **Característica ISO/IEC 25010:** Eficiência de Desempenho (comportamento em relação ao tempo de resposta).
**RNF 1.2 — Segurança**
O sistema deve garantir que apenas o cliente que realizou o pedido possa avaliá-lo, impedindo avaliações de terceiros ou duplicadas.
- **Característica ISO/IEC 25010:** Segurança (controle de acesso e autenticidade da ação).
**RNF 1.3 — Confiabilidade**
Uma vez enviada, a avaliação (nota e comentário) não pode ser perdida por falha de conexão ou queda do sistema, devendo ser persistida de forma consistente.
- **Característica ISO/IEC 25010:** Confiabilidade (disponibilidade e tolerância a falhas).
---
 
## História 2
 
**Como** cliente, **quero** salvar um cartão de pagamento, **para** não digitar os dados a cada compra.
 
**Critérios de aceitação:**
- Dado que o cliente cadastra um cartão válido, quando confirma o cadastro, então o cartão fica disponível para escolha no checkout.
- Dado que o cliente tem um cartão salvo, quando faz um novo pedido, então pode selecionar esse cartão sem redigitar os dados.
### RNFs
 
**RNF 2.1 — Segurança**
Os dados do cartão devem ser armazenados de forma criptografada (ou tokenizada), em conformidade com o padrão PCI-DSS, sem exposição do número completo em nenhuma interface.
- **Característica ISO/IEC 25010:** Segurança (confidencialidade dos dados sensíveis).
**RNF 2.2 — Usabilidade**
O cadastro do cartão deve ser concluído em no máximo 3 passos, com feedback claro de sucesso ou erro em cada etapa.
- **Característica ISO/IEC 25010:** Usabilidade (operabilidade e capacidade de aprendizagem).
**RNF 2.3 — Confiabilidade**
Os dados do cartão salvo não podem ser perdidos ou corrompidos entre sessões, garantindo que o cartão esteja sempre disponível em pedidos futuros.
- **Característica ISO/IEC 25010:** Confiabilidade (maturidade/integridade dos dados armazenados).
---
 
## História 3
 
**Como** dono de restaurante, **quero** ver um resumo diário de vendas, **para** acompanhar o desempenho do dia.
 
**Critérios de aceitação:**
- Dado que o dia comercial termina, quando o restaurante abre o painel de vendas, então vê o total de pedidos e o faturamento do dia.
- Dado que o restaurante seleciona um período diferente, quando aplica o filtro, então o resumo é recalculado para aquele período.
### RNFs
 
**RNF 3.1 — Eficiência de Desempenho**
O recálculo do resumo de vendas ao aplicar um filtro de período deve ocorrer em até 3 segundos, mesmo com grande volume de pedidos históricos.
- **Característica ISO/IEC 25010:** Eficiência de Desempenho (comportamento em relação ao tempo de resposta e utilização de recursos).
**RNF 3.2 — Usabilidade**
O painel de vendas deve apresentar os dados (total de pedidos e faturamento) de forma clara e visualmente compreensível, sem exigir treinamento prévio do dono do restaurante.
- **Característica ISO/IEC 25010:** Usabilidade (inteligibilidade e estética da interface).
**RNF 3.3 — Portabilidade**
O painel de vendas deve funcionar corretamente em diferentes dispositivos (desktop e mobile) e navegadores, mantendo a mesma funcionalidade.
- **Característica ISO/IEC 25010:** Portabilidade (adaptabilidade a diferentes ambientes).
---
 
## Resumo
 
| História | RNF | Característica ISO/IEC 25010 |
|---|---|---|
| 1 | Tempo de resposta ao exibir opção de avaliação | Eficiência de Desempenho |
| 1 | Restrição de avaliação ao cliente do pedido | Segurança |
| 1 | Persistência garantida da avaliação enviada | Confiabilidade |
| 2 | Criptografia/tokenização dos dados do cartão | Segurança |
| 2 | Cadastro em poucos passos com feedback claro | Usabilidade |
| 2 | Integridade dos dados do cartão entre sessões | Confiabilidade |
| 3 | Recálculo rápido do resumo ao aplicar filtro | Eficiência de Desempenho |
| 3 | Clareza visual do painel de vendas | Usabilidade |
| 3 | Funcionamento em múltiplos dispositivos/navegadores | Portabilidade |
