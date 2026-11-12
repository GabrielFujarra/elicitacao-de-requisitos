# UC02 — Criar cobrança

**Sistema:** Sistema de Cobranças

## Identificação

| Campo | Descrição |
|---|---|
| **Ator principal** | Lojista |
| **Descrição** | O lojista registra uma nova cobrança para um cliente, informando valor e data de vencimento. O sistema envia a cobrança ao cliente e agenda um lembrete de vencimento. |
| **Gatilho** | O lojista seleciona a opção "Nova cobrança". |

## Pré-condições

- O lojista está autenticado no sistema.
- Existe pelo menos um cliente cadastrado, ou o lojista pode cadastrar um novo durante o fluxo (ver A1).

## Pós-condições

- A cobrança está registrada com o status **Pendente**.
- Um lembrete de vencimento está agendado para 3 dias antes da data limite.
- O cliente recebeu a cobrança com as instruções de pagamento.

## Fluxo principal

1. O lojista seleciona a opção "Nova cobrança".
2. O sistema exibe o formulário de cobrança.
3. O lojista seleciona o cliente.
4. O lojista informa o valor, a data de vencimento e uma descrição.
5. O lojista confirma o cadastro.
6. O sistema valida os dados informados.
7. O sistema registra a cobrança com o status Pendente.
8. O sistema agenda o lembrete de vencimento.
9. O sistema envia a cobrança ao cliente com as instruções de pagamento.
10. O sistema exibe ao lojista a confirmação de que a cobrança foi criada.
11. O caso de uso termina.

## Fluxo alternativo

### A1 — Cliente ainda não cadastrado

- **Quando:** no passo 3, o cliente desejado não aparece na lista.
- **Passos:**
  1. O lojista seleciona a opção "Cadastrar novo cliente".
  2. O sistema executa o caso de uso UC01 — Cadastrar cliente.
  3. O sistema retorna ao formulário de cobrança com o novo cliente já selecionado.
- **Retorno:** o fluxo volta ao passo 4 do fluxo principal.

## Exceção

### E1 — Dados inválidos

- **Quando:** no passo 6, o valor é menor ou igual a zero ou a data de vencimento está no passado.
- **Passos:**
  1. O sistema não registra a cobrança.
  2. O sistema destaca os campos inválidos e exibe uma mensagem explicando o erro.
- **Retorno:** o fluxo volta ao passo 4 do fluxo principal, para o lojista corrigir os dados.
