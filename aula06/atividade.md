# Caso Prático — Empatia, Definição, Ideação e Histórias de Usuário
 
> Observação: como sou uma IA, não vivo o dia a dia da mesma forma que uma pessoa, então escolhi um problema comum e real que muita gente enfrenta na rotina de trabalho, para manter o exercício genuíno. Fique à vontade para trocar pelo seu próprio incômodo semanal, se preferir — a estrutura abaixo serve de modelo.
 
## Problema escolhido
 
Esquecer de beber água ao longo de um dia de trabalho, ficando horas sem se hidratar até sentir os sintomas (sede forte, dor de cabeça, cansaço).
 
---
 
## 1. Empatia
 
**Pergunta.** Por que eu só percebo que estou com sede quando já estou com dor de cabeça, mesmo com a garrafa de água em cima da mesa?
 
## 2. Definição
 
Eu não bebo água ao longo do dia não por falta de vontade, mas porque não existe nenhum lembrete externo me avisando — dependo só da sensação de sede, e quando estou concentrado em uma tarefa esse sinal chega tarde demais, quando o corpo já está desidratado.
 
## 3. Ideação
 
- Notificação push a cada 2 horas durante o expediente, lembrando de beber água.
- Garrafa inteligente com sensor que acende uma luz quando passa muito tempo sem ser levantada da mesa.
- Resumo diário, ao final do dia, mostrando quanto de água foi registrado e comparando com a meta pessoal.
## 4. Escolha
 
**Ideia escolhida.** Notificação push a cada 2 horas durante o horário de trabalho, lembrando de beber água.
 
## 5. Histórias de usuário
 
1. **Como** usuário que trabalha muitas horas seguidas, **quero** receber uma notificação a cada 2 horas durante o meu expediente, **para** lembrar de beber água mesmo quando não percebo a sede a tempo.
2. **Como** usuário, **quero** poder configurar o intervalo entre os lembretes, **para** adaptar a frequência à minha própria rotina e necessidade de hidratação.
3. **Como** usuário, **quero** poder pausar as notificações fora do horário de trabalho, **para** não ser incomodado à noite, nos finais de semana ou durante folgas.
## 6. Critérios de aceitação
 
1. **Dado** que o usuário configurou o intervalo de lembretes para 2 horas, **quando** esse tempo se passa sem nenhuma interação registrada, **então** uma notificação push é enviada lembrando de beber água.
2. **Dado** que o usuário definiu um horário de início e fim de expediente, **quando** o horário atual está fora desse intervalo, **então** nenhuma notificação é enviada.
3. **Dado** que o usuário recebeu uma notificação de lembrete, **quando** ele toca em "bebi água" dentro do app, **então** o contador de tempo é reiniciado e a próxima notificação só é enviada após o intervalo configurado se repetir.

