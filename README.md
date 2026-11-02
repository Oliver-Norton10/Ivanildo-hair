# Ivanildo Hair · Sistema de Agendamento Online

Sistema de agendamento **em produção** para um salão de beleza e barbearia. Os clientes marcam, consultam e remarcam horários pelo celular, e o proprietário administra a agenda num painel próprio.

🔗 **No ar:** [ivanildohair.com.br](https://ivanildohair.com.br)

## O problema

Antes, todo agendamento era feito por conversa no WhatsApp: o cliente perguntava os horários livres, o dono olhava a agenda, respondia, esperava a confirmação... Isso tomava tempo durante os atendimentos, gerava mensagens perdidas e, às vezes, dois clientes no mesmo horário.

## A solução

Eu desenvolvi um sistema que encaixa no jeito que os clientes já se comunicam com o salão:

1. O cliente manda uma mensagem no **WhatsApp** do estabelecimento.
2. Recebe uma **resposta automática com o link** de agendamento.
3. No link, preenche **nome e telefone**, escolhe a **categoria** (salão feminino ou barbearia), o **serviço**, o **dia** e o **horário**.
4. Confirma e pronto: o horário fica reservado e some da lista para os próximos clientes.

## Funcionalidades

**Para o cliente**
- **Agendamento rápido pelo celular,** com os horários livres calculados em tempo real.
- **Bloqueio de conflito:** o sistema não deixa dois clientes marcarem o mesmo horário.
- **"Meus agendamentos":** o cliente consulta e **remarca** os próprios horários.
- **Dados lembrados no aparelho,** para não precisar digitar nome e telefone de novo.
- **Confirmação com atalho para o WhatsApp** do salão.

**Para o proprietário (área restrita)**
- **Agenda** em calendário com visão semanal.
- **Bloqueio de horários** específicos ou do dia inteiro (folgas e compromissos).
- **Agendamento por telefone,** para registrar clientes que ligam ou chegam pessoalmente.
- **Finalização do atendimento.** Nos serviços químicos (alisamento, selante, permanente), o sistema registra qual química foi usada.
- **Histórico por cliente,** importante para saber o que já foi aplicado no cabelo de cada pessoa.
- **Lista de clientes e resumo do mês.**
- **Aviso no navegador** quando entra um novo agendamento.

## Tecnologias

| Camada | Tecnologia |
|---|---|
| Front-end | HTML, CSS e JavaScript puro, com layout mobile-first |
| Banco de dados | Supabase (PostgreSQL na nuvem) |
| Hospedagem | GitHub Pages com domínio próprio |
| Integração | Links do WhatsApp (`wa.me`) com mensagem pronta |

## Decisões que tomei

- **Começar pelo WhatsApp.** Os clientes do salão já usam o WhatsApp, então o agendamento começa por ali. Ninguém precisa instalar aplicativo nem criar conta.
- **Mobile-first.** Quase todo acesso vem do celular, então a interface foi pensada para o toque, com botões grandes e poucos passos.
- **Resiliência.** Se a conexão com o banco falhar ou demorar, o sistema avisa e não deixa botões travados.
- **Histórico de química.** Esse pedido veio do próprio dono: em serviços químicos, saber o que já foi aplicado evita danos ao cabelo do cliente.

## Resultado

O sistema está em uso real no salão. Os agendamentos chegam organizados, sem conflito de horário, e o proprietário parou de gerenciar a agenda pelo WhatsApp durante os atendimentos.

---

Desenvolvido por **Oliver Norton** · [GitHub](https://github.com/Oliver-Norton10)
