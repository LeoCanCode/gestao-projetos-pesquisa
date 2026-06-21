> Projeto: MVP - Sistema de Gestão de Projetos de Pesquisa
> Repositório: gestao-projetos-pesquisa
> Sprint: Sprint 1 — Dia 7
> Facilitador: Leonardo (Scrum Master)
> Participantes: Leonardo | Bruno | Helena
> Observacao: Reuniao realizada apenas entre a equipe,
> sem a presenca do chefe do grupo de pesquisa.
> Ferramenta de reunião: Google Meet

---

## Informacoes da Reuniao

- **Data:** Dia 7 da Sprint
- **Horario:** 10h00 – 10h45
- **Formato:** Google Meet
- **Tecnica utilizada:** Start / Stop / Continue

---

## Contexto

> Ao final da Sprint 1, a equipe se reuniu para refletir
> sobre o processo de trabalho, identificar o que funcionou
> bem, o que atrapalhou e o que precisa mudar para a
> proxima Sprint. A reuniao foi conduzida pelo Leonardo
> e cada membro contribuiu livremente com seus pontos.

---

## START
### O que devemos COMECAR a fazer?

---

**1. Usar branches separadas no Git para cada funcionalidade**
> Durante a Sprint 1, o time trabalhou majoritariamente
> na branch principal (main), o que gerou conflitos de
> merge em alguns momentos e dificultou o rastreamento
> de quais mudancas pertenciam a cada tarefa.
> Na proxima Sprint, cada funcionalidade ou historia de
> usuario deve ter sua propria branch, seguindo o padrao:
> feature/nome-da-funcionalidade.
>
> - Responsavel por implementar: Bruno
> - Prazo: A partir do primeiro dia da proxima Sprint

---

**2. Validar o modelo do banco de dados com toda a equipe
antes de iniciar o desenvolvimento**
> O retrabalho gerado no Dia 4 — quando foi identificado
> que o relacionamento entre Atividade e Membro deveria
> ser N:M e nao 1:N — poderia ter sido evitado se o
> modelo conceitual tivesse sido revisado coletivamente
> antes de ser considerado finalizado.
> Na proxima Sprint, o modelo do BD deve ser apresentado
> e aprovado por todos antes de qualquer implementacao.
>
> - Responsavel por implementar: Leonardo
> - Prazo: Durante o Sprint Planning da proxima Sprint

---

**3. Iniciar os testes de integracao mais cedo no ciclo
da Sprint**
> Conforme levantado pela Helena no Dia 6 e reforçado
> na Sprint Review, os testes de integracao end-to-end
> nao foram totalmente cobertos pois as entregas de
> desenvolvimento se concentraram no ultimo dia.
> Na proxima Sprint, os testes de integracao devem
> ser iniciados assim que as primeiras funcionalidades
> estiverem disponiveis, e nao apenas ao final.
>
> - Responsavel por implementar: Helena
> - Prazo: A partir do Dia 4 da proxima Sprint

---

## STOP
### O que devemos PARAR de fazer?

---

**1. Comecar a desenvolver sem o ambiente padronizado**
> A inconsistencia de versao do Node.js entre as maquinas
> do grupo (v18 vs v20), identificada pela Helena no Dia 3,
> gerou um impedimento que atrasou a validacao dos ambientes
> e custou tempo precioso da Sprint. O ambiente de
> desenvolvimento deve ser padronizado e documentado
> antes de qualquer linha de codigo ser escrita.
>
> - Impacto gerado: atraso na KAN-38 e retrabalho
>   na configuracao das maquinas.

---

**2. Trabalhar em tarefas com dependencias nao resolvidas**
> Bruno iniciou partes da KAN-16 (Criar formulario de
> cadastro) sem ter o modelo logico do BD finalizado,
> o que resultou em retrabalho posterior para alinhar
> os campos do formulario com a estrutura real das tabelas.
> As dependencias entre tarefas devem ser mapeadas e
> respeitadas — uma tarefa so deve ser iniciada quando
> seus pre-requisitos estiverem concluidos.
>
> - Impacto gerado: retrabalho no formulario e
>   desalinhamento temporario entre frontend e backend.

---

**3. Concentrar entregas de desenvolvimento no ultimo
dia da Sprint**
> O acumulo de tarefas de desenvolvimento no Dia 6
> foi consequencia direta dos atrasos dos dias anteriores,
> mas tambem de uma falta de antecipacao no planejamento.
> Isso gerou pressao desnecessaria sobre Bruno e
> comprimiu o tempo disponivel para os testes da Helena.
> Na proxima Sprint, o time deve monitorar o burndown
> diariamente e redistribuir tarefas assim que sinais
> de atraso forem identificados.
>
> - Impacto gerado: cobertura incompleta dos testes
>   de integracao e risco de qualidade na entrega.

---

## CONTINUE
### O que esta dando certo e devemos CONTINUAR fazendo?

---

**1. Comunicacao transparente entre os membros**
> Durante toda a Sprint, os impedimentos foram comunicados
> rapidamente — seja nas Dailies ou via Jira — sem que
> nenhum membro tentasse esconder dificuldades ou atrasos.
> Isso permitiu que os problemas fossem endereçados
> rapidamente, mesmo que com algum custo de tempo.
> Essa cultura de transparencia deve ser mantida.

---

**2. Uso do Jira para rastreamento das tarefas**
> O Jira se mostrou uma ferramenta eficaz para o time
> acompanhar o status das tarefas, registrar impedimentos
> e manter o backlog organizado. O habito de atualizar
> o status das tarefas no Jira apos cada entrega deve
> ser mantido e reforçado na proxima Sprint.

---

**3. Documentacao continua ao longo da Sprint**
> A Helena manteve os arquivos de documentacao atualizados
> durante toda a Sprint — README, DAILY_LOGS e
> RETROSPECTIVE — sem deixar para o ultimo dia.
> Esse habito evita o acumulo de documentacao e garante
> que o repositorio reflita o estado real do projeto
> a qualquer momento.

---

**4. Dailies objetivas e dentro do tempo**
> As reunioes diarias foram realizadas consistentemente
> dentro do limite de 15 minutos, com cada membro
> respondendo as tres perguntas de forma direta e
> sem desvios para discussoes tecnicas longas.
> Esse formato deve ser mantido.

---

## Acoes de Melhoria para a Proxima Sprint

| # | Acao                                              | Responsavel | Prazo                          |
|---|---------------------------------------------------|-------------|--------------------------------|
| 1 | Adotar branches por funcionalidade no Git         | Bruno       | Primeiro dia da proxima Sprint |
| 2 | Revisar e aprovar modelo do BD coletivamente      | Leonardo    | Durante o Sprint Planning      |
| 3 | Iniciar testes de integracao a partir do Dia 4    | Helena      | A partir do Dia 4              |
| 4 | Padronizar ambiente antes de iniciar o desenvolvimento | Leonardo | Durante o Sprint Planning      |
| 5 | Monitorar burndown diariamente e redistribuir tarefas se necessario | Leonardo | A partir do Dia 2  |

---

## Resumo Geral da Retrospectiva

| Categoria | Quantidade de Pontos Levantados |
|-----------|---------------------------------|
| Start     | 3                               |
| Stop      | 3                               |
| Continue  | 4                               |
| Acoes de Melhoria | 5                       |

---

> A equipe reconhece que a Sprint 1 foi um ciclo de
> aprendizado importante. Apesar dos impedimentos e
> do atraso acumulado nos dias intermediarios, todas
> as historias de usuario principais foram entregues
> e demonstradas na Sprint Review. Os pontos levantados
> nesta Retrospectiva serao considerados no planejamento
> da proxima Sprint para que o time evolua tanto em
> processo quanto em qualidade de entrega.

---

*Documento elaborado por: Helena (QA)*
*Data: Dia 7 da Sprint*
