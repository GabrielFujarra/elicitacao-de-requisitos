# Escolha de Técnicas de Elicitação de Requisitos
 
**Contexto:** Escola de idiomas (aulas presenciais e online) quer digitalizar três processos: matrícula de aluno novo, registro de frequência pelo professor e agendamento de reposição pelo aluno.
 
> Obs.: como não tenho acesso à lista exata das oito técnicas vistas em aula, usei um conjunto padrão de técnicas de elicitação (Entrevista, Análise de documentos, Observação, JAD/Workshop e Prototipagem). Se a lista da disciplina usar outros nomes para as mesmas ideias, é só renomear — o raciocínio da escolha continua válido.
 
---
 
## Processo 1 — Secretaria registra a matrícula de aluno novo
 
**Técnica.** Entrevista
 
**Definição.** Conversa guiada (estruturada ou semiestruturada) com quem executa o processo hoje, com o objetivo de entender passo a passo como ele é feito, quais informações são coletadas e quais regras são aplicadas.
 
**Stakeholder.** Secretária(o) da escola.
 
**Motivo.** A matrícula é um processo cheio de regras de negócio que só existem na cabeça de quem faz — quais documentos são exigidos, o que muda entre aluno menor e maior de idade, quais formas de pagamento são aceitas, o que acontece se a turma escolhida já estiver cheia. A entrevista permite perguntar diretamente "e se X acontecer?" e captar essas regras de forma rápida, sem depender de longos períodos de observação.
 
**Técnica complementar.** Análise de documentos
 
**Definição.** Levantar requisitos a partir da leitura de materiais já existentes — formulários, planilhas, contratos, fichas cadastrais — usados no processo atual.
 
**Stakeholder.** Secretaria (dona do formulário de matrícula em papel/planilha atual).
 
**Motivo.** O formulário de matrícula que já existe mostra, de forma objetiva, quais campos são realmente preenchidos hoje (nome, CPF, responsável, turma, forma de pagamento), servindo como checklist inicial de dados que o sistema precisa capturar, sem depender da memória de ninguém durante a entrevista.
 
---
 
## Processo 2 — Professor registra a frequência em cada aula
 
**Técnica.** Observação
 
**Definição.** Acompanhar o processo sendo executado no local real, no dia a dia, sem interferir, para capturar como ele acontece na prática — e não como a pessoa descreve de memória.
 
**Stakeholder.** Professor.
 
**Motivo.** Em entrevista, o professor pode não lembrar de um critério automático, como a forma que usa pra marcar falta parcial de quem chega atrasado. Esse tipo de regra é aplicado de forma quase inconsciente todo dia, e só aparece observando a aula acontecer de verdade — tanto na turma presencial quanto na sala online.
 
---
 
## Processo 3 — Aluno agenda reposição em outro horário quando falta
 
**Técnica.** JAD (Joint Application Design) / Workshop
 
**Definição.** Reunião estruturada com vários stakeholders ao mesmo tempo, mediada por um facilitador, para levantar e já alinhar requisitos em conjunto, em vez de coletar informações separadamente e depois tentar juntar as peças.
 
**Stakeholder.** Secretaria, professores e coordenação pedagógica (múltiplos stakeholders).
 
**Motivo.** O agendamento de reposição não depende só do aluno: envolve disponibilidade de horário do professor, vagas na turma de destino, limite de quantas reposições um aluno pode marcar e prazos. Se cada área fosse entrevistada separadamente, corre-se o risco de levantar regras conflitantes (ex.: secretaria diz que não há limite de reposições, professor diz que só aceita até 2 por aluno). O workshop resolve esse conflito na hora, com todos na mesma sala.
 
**Técnica complementar.** Prototipagem
 
**Definição.** Construir uma versão simplificada e navegável da tela antes de desenvolver de verdade, para validar com o usuário final se o fluxo faz sentido.
 
**Stakeholder.** Aluno.
 
**Motivo.** Agendar reposição é uma interação direta do aluno com o sistema, escolhendo entre horários disponíveis. Um protótipo permite testar com alunos reais se eles entendem as opções apresentadas e conseguem concluir o agendamento sozinhos, antes de gastar tempo de desenvolvimento em um fluxo confuso.
