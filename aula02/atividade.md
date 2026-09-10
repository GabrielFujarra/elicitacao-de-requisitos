# Aula 2 — Histórias de Usuário, Critérios de Aceitação e MoSCoW
 
**Contexto:** Aplicativo de delivery de comida. Três necessidades vagas foram transformadas em histórias de usuário (com o princípio INVEST em mente) e critérios de aceitação no formato Dado/Quando/Então.
 
---
 
## 1. Acompanhamento do pedido pelo usuário
 
> **Como** usuário do aplicativo,
> **eu quero** acompanhar o status do meu pedido em tempo real após a compra,
> **para que** eu saiba em que etapa ele está e quando vai chegar.
 
**Por que atende ao INVEST:**
- **Independente**: não depende de outras funcionalidades para ser entregue.
- **Negociável**: a forma de exibição (mapa, barra de progresso, notificações) pode ser discutida com o time.
- **Valiosa**: reduz ansiedade do cliente e chamados de suporte do tipo "cadê meu pedido?".
- **Estimável**: escopo claro o suficiente para estimar esforço.
- **Pequena**: cabe em uma sprint.
- **Testável**: os critérios abaixo são verificáveis.
### Critérios de aceitação
 
1. **Dado** que o usuário fez um pedido e o restaurante o confirmou,
   **quando** o restaurante inicia o preparo,
   **então** o status do pedido é atualizado para "Em preparo" e exibido no app.
2. **Dado** que o pedido está em preparo,
   **quando** o entregador retira o pedido no restaurante,
   **então** o status muda para "A caminho" e o app passa a exibir a localização estimada do entregador.
3. **Dado** que o pedido está "A caminho",
   **quando** o entregador confirma a entrega no local de destino,
   **então** o status muda para "Entregue" e o usuário recebe uma notificação push.
---
 
## 2. Restaurante avisando indisponibilidade de item
 
> **Como** restaurante parceiro,
> **eu quero** marcar um item do cardápio como indisponível,
> **para que** os clientes não consigam pedir produtos que não posso preparar no momento.
 
**Por que atende ao INVEST:**
- **Independente**: funcionalidade isolada do fluxo de pedido do cliente.
- **Negociável**: pode evoluir para indisponibilidade temporária/agendada depois.
- **Valiosa**: evita pedidos cancelados e frustração do cliente.
- **Estimável**: ação simples de CRUD sobre o cardápio.
- **Pequena**: entregável em poucos dias.
- **Testável**: critérios claros de visibilidade do item.
### Critérios de aceitação
 
1. **Dado** que estou logado no painel do restaurante,
   **quando** marco um item como indisponível,
   **então** esse item deixa de ser exibido no cardápio visível aos clientes.
2. **Dado** que um item está marcado como indisponível,
   **quando** um cliente pesquisa ou navega pelo cardápio,
   **então** o sistema não retorna esse item nos resultados nem permite adicioná-lo ao carrinho.
3. **Dado** que um item estava indisponível,
   **quando** o restaurante desmarca a indisponibilidade,
   **então** o item volta a aparecer normalmente no cardápio para os clientes.
---
 
## 3. Entregador reportando problema durante a entrega
 
> **Como** entregador,
> **eu quero** reportar um problema durante a entrega,
> **para que** o suporte seja acionado e possa me ajudar a resolver a situação rapidamente.
 
**Por que atende ao INVEST:**
- **Independente**: não depende das histórias anteriores.
- **Negociável**: categorias de problema e canal de resposta podem ser refinados.
- **Valiosa**: reduz entregas travadas e melhora a experiência do entregador.
- **Estimável**: escopo definido (formulário + notificação).
- **Pequena**: entregável em uma sprint.
- **Testável**: fluxo de reporte e resposta é verificável.
### Critérios de aceitação
 
1. **Dado** que estou realizando uma entrega,
   **quando** encontro um problema (ex.: endereço não localizado, cliente ausente, item danificado),
   **então** consigo abrir no app um formulário de reporte de problema com opções pré-definidas e campo de descrição.
2. **Dado** que preenchi o formulário de problema,
   **quando** envio o reporte,
   **então** o suporte é notificado imediatamente com os detalhes da ocorrência e o número do pedido.
3. **Dado** que um problema foi reportado,
   **quando** o suporte registra uma resposta ou instrução,
   **então** o entregador recebe uma notificação no app com os próximos passos.
---
 
## Priorização MoSCoW
 
| Prioridade | História | Justificativa |
|---|---|---|
| **Must have** | Acompanhamento do pedido pelo usuário | É o núcleo da experiência do cliente pós-compra; sem isso o app perde confiança e gera alto volume de suporte. |
| **Should have** | Restaurante avisando indisponibilidade de item | Importante para evitar cancelamentos e frustração, mas o app pode funcionar sem isso no curto prazo (ex.: cancelamento manual). |
| **Could have** | Entregador reportando problema | Agrega valor operacional, mas pode ser resolvido inicialmente por um canal alternativo (telefone/chat de suporte) até ser priorizado. |
| **Won't have (por ora)** | — | Nenhuma das três foi classificada como fora do escopo; todas entram no roadmap, apenas em momentos diferentes. |
