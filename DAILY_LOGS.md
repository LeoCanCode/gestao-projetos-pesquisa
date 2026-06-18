# DAILY_LOGS.md

> Projeto: MVP - Sistema de Gestão de Projetos de Pesquisa
> Repositório: [grupo-pesquisa-mvp]
> Sprint: Sprint 1 — Duração: Dias 1 a 7
> Scrum Master (responsável pelo log): Leonardo
> Ferramenta de reunião: Google Meet

---

## Equipe

| Membro   | Papel                          |
|----------|--------------------------------|
| Leonardo | Scrum Master / Product Owner   |
| Bruno    | Developer                      |
| Helena   | QA (Quality Assurance)         |

---

## Daily Scrum — Dia 2

- **Data:** Segunda-feira — Dia 2 da Sprint
- **Horário:** 09h00 – 09h15
- **Formato:** Google Meet
- **Participantes:** Leonardo | Bruno | Helena

---

### Leonardo (Scrum Master / PO)

**O que fiz ontem (Dia 1 — Planejamento)?**
> Participei do Sprint Planning, refinamos o backlog no Jira,
> definimos as estimativas em Fibonacci para todas as histórias
> e subtarefas, e priorizamos as entregas da Sprint 1.
> Também criei a estrutura inicial do repositório e adicionei
> o arquivo SPRINT_BACKLOG.md.

**O que farei hoje?**
> Vou iniciar a KAN-37 (Configuração de Software) — preparar
> o ambiente de desenvolvimento com as dependências do projeto
> (Node.js / framework backend, banco de dados).
> Também iniciarei o esboço do KAN-40 (Projeto Conceitual do BD).

**Impedimentos?**
> Nenhum impedimento no momento.

---

### Bruno (Developer)

**O que fiz ontem (Dia 1 — Planejamento)?**
> Participei do Sprint Planning, ajudei a estimar as tarefas
> no Jira e entendi o escopo das US01 e US03 que serão minhas
> responsabilidades principais.

**O que farei hoje?**
> Vou trabalhar na KAN-36 (Configuração de Hardware) — verificar
> e documentar a configuração das máquinas da equipe.
> Paralelamente, vou iniciar a leitura dos requisitos da
> KAN-15 (Criar modelo Projeto) para já ir pensando na estrutura.

**Impedimentos?**
> Nenhum impedimento no momento.

---

### Helena (QA)

**O que fiz ontem (Dia 1 — Planejamento)?**
> Participei do Sprint Planning, contribuí com a estimativa
> das tarefas e entendi as histórias de usuário que precisarei
> validar: US01, US02, US03 e US04.

**O que farei hoje?**
> Vou criar o arquivo KAN-32 (DAILY_LOGS.md) e o
> KAN-33 (RETROSPECTIVE.md) no repositório com a estrutura
> base. Também vou levantar os critérios de aceitação
> para os testes das KAN-18, KAN-21, KAN-25 e KAN-28.

**Impedimentos?**
> Nenhum impedimento no momento.

---

### Resumo do Dia 2
- Time alinhado com o backlog e papéis definidos.
- Início das configurações de ambiente (hardware e software).
- Estrutura do repositório e arquivos de documentação em andamento.
- **Nenhum impedimento registrado.**

---
---

## Daily Scrum — Dia 3

- **Data:** Terça-feira — Dia 3 da Sprint
- **Horário:** 09h00 – 09h15
- **Formato:** Google Meet
- **Participantes:** Leonardo | Bruno | Helena

---

### Leonardo (Scrum Master / PO)

**O que fiz ontem (Dia 2)?**
> Concluí a KAN-37 (Configuração de Software) — ambiente
> configurado com Node.js, Express e PostgreSQL instalados
> e documentados. Iniciei o esboço do KAN-40
> (Projeto Conceitual do BD): identifiquei as entidades
> principais: Projeto, Atividade e Membro.

**O que farei hoje?**
> Vou finalizar o KAN-40 (Projeto Conceitual do BD) com
> o diagrama entidade-relacionamento (DER) e iniciar o
> KAN-41 (Projeto Lógico do BD), mapeando as entidades
> para tabelas relacionais com atributos e chaves.

**Impedimentos?**
> Nenhum impedimento.

---

### Bruno (Developer)

**O que fiz ontem (Dia 2)?**
> Finalizei a KAN-36 (Configuração de Hardware) —
> documentei as especificações das máquinas do grupo.
> Iniciei a KAN-15 (Criar modelo Projeto) — defini os
> atributos iniciais da entidade Projeto:
> id, título, descrição, data_início, status.

**O que farei hoje?**
> Vou concluir a KAN-15 (Criar modelo Projeto) e
> iniciar a KAN-16 (Criar formulário de cadastro de Projeto)
> — estruturar o formulário HTML/frontend com os campos
> necessários para cadastro.

**Impedimentos?**
> Preciso que o Leonardo finalize o modelo lógico do BD
> para garantir que os campos do formulário estejam
> alinhados com as tabelas. (dependência identificada)

---

### Helena (QA)

**O que fiz ontem (Dia 2)?**
> Criei e subi os arquivos KAN-32 (DAILY_LOGS.md) e
> KAN-33 (RETROSPECTIVE.md) no repositório com a
> estrutura base. Elaborei o checklist de critérios
> de aceitação para KAN-18 (Testar cadastro de Projeto).

**O que farei hoje?**
> Vou elaborar os critérios de aceitação e casos de
> teste para KAN-21 (Testar listagem) e KAN-25
> (Testar cadastro de Atividade). Também vou iniciar
> a KAN-38 (Validação dos ambientes de hardware e software)
> — verificar se os ambientes configurados pelo Leonardo
> e Bruno estão funcionais.

**Impedimentos?**
> Aguardando o ambiente de software do Leonardo estar
> totalmente disponível para rodar a validação completa.
> (dependência leve — deve ser resolvida hoje)

---

### Resumo do Dia 3
- Ambientes de hardware e software praticamente finalizados.
- Modelo conceitual do BD em fase de conclusão.
- Formulário de cadastro de Projeto sendo iniciado.
- **Impedimentos:** Bruno depende do modelo lógico do BD
  (Leonardo priorizará isso hoje). Helena depende do
  ambiente de Leonardo para validação completa.

---
---

## Daily Scrum — Dia 4

- **Data:** Quarta-feira — Dia 4 da Sprint
- **Horário:** 09h00 – 09h15
- **Formato:** Google Meet
- **Participantes:** Leonardo | Bruno | Helena

---

### Leonardo (Scrum Master / PO)

**O que fiz ontem (Dia 3)?**
> Finalizei o KAN-40 (Projeto Conceitual do BD) — DER
> entregue e commitado no repositório. Porém, ao revisar
> o KAN-41 (Projeto Lógico do BD), percebi que subestimamos
> a complexidade do relacionamento entre Atividade e Membro:
> inicialmente modelamos como 1:N, mas o requisito permite
> que uma atividade seja atribuída a mais de um membro,
> exigindo uma tabela associativa. Isso atrasou a entrega
> do modelo lógico — ainda não foi concluído.

**O que farei hoje?**
> Prioridade total em finalizar o KAN-41 (Projeto Lógico
> do BD) com o relacionamento N:M corrigido. Assim que
> entregar o modelo para Bruno, iniciarei a KAN-42
> (Implantação do BD).

**Impedimentos?**
> O erro de modelagem do Dia 3 gerou retrabalho e está
> atrasando Bruno. Vou resolver isso ainda pela manha
> de hoje. (impedimento interno — retrabalho de modelagem)

---

### Bruno (Developer)

**O que fiz ontem (Dia 3)?**
> Tentei avançar na KAN-16 (Criar formulário de cadastro)
> sem esperar o modelo lógico, mas precisei parar pois
> os campos do formulário dependem diretamente da estrutura
> final das tabelas. Acabei reaproveitando o tempo para
> aprofundar a leitura dos requisitos das US03 e US04.

**O que farei hoje?**
> Aguardarei a entrega do modelo lógico pelo Leonardo
> (prevista para a manha). Assim que receber, finalizarei
> a KAN-15 (Criar modelo Projeto) com os atributos
> corretos e darei sequencia na KAN-16 (Criar formulário).

**Impedimentos?**
> Bloqueado aguardando o modelo lógico do BD (KAN-41).
> (impedimento ativo — dependência de Leonardo)

---

### Helena (QA)

**O que fiz ontem (Dia 3)?**
> Finalizei os critérios de aceitação de KAN-21 e KAN-25.
> Iniciei a KAN-38 (Validação dos ambientes), mas identifiquei
> que o ambiente de software do Leonardo ainda nao estava
> estavel o suficiente para validacao completa — versao do
> Node.js divergia entre as maquinas do grupo (v18 vs v20),
> causando inconsistencia na execucao do projeto.
> Reportei o problema para Leonardo via Jira.

**O que farei hoje?**
> Acompanharei a resolucao da inconsistencia de versao do
> Node.js junto com Leonardo. Assim que o ambiente estiver
> padronizado, finalizarei a KAN-38 (Validacao dos ambientes).
> Enquanto isso, vou adiantar a estrutura do KAN-48 (README).

**Impedimentos?**
> Ambiente com versoes divergentes de Node.js entre as
> maquinas do grupo impede a validacao completa.
> (impedimento ativo — aguardando padronizacao do ambiente)

---

### Resumo do Dia 4
- Retrabalho identificado no modelo logico do BD (relacionamento
  N:M nao previsto inicialmente) — Leonardo corrigindo hoje.
- Bruno bloqueado aguardando o modelo logico corrigido.
- Inconsistencia de versao do Node.js identificada pela Helena
  — ambiente precisa ser padronizado.
- **Dois impedimentos ativos:** retrabalho no BD e divergencia
  de ambiente. Ambos com resolucao prevista para hoje.
- Sprint levemente atrasada em relacao ao planejado —
  Leonardo ira revisar o burndown e avaliar riscos.

---
---

## Daily Scrum — Dia 5

- **Data:** Quinta-feira — Dia 5 da Sprint
- **Horário:** 09h00 – 09h15
- **Formato:** Google Meet
- **Participantes:** Leonardo | Bruno | Helena

---

### Leonardo (Scrum Master / PO)

**O que fiz ontem (Dia 4)?**
> Finalizei o KAN-41 (Projeto Logico do BD) com o
> relacionamento N:M corrigido — tabela associativa
> atividade_membro criada. Compartilhei o modelo com
> Bruno logo pela manha, desbloqueando seu trabalho.
> Tambem padronizei a versao do Node.js para v20 em
> todas as maquinas do grupo e documentei no README,
> resolvendo o impedimento da Helena.
> Iniciei a KAN-42 (Implantacao do BD), mas nao consegui
> concluir — o script SQL ainda esta em construcao.

**O que farei hoje?**
> Prioridade em finalizar a KAN-42 (Implantacao do BD)
> ainda pela manha. Revisarei o burndown — estamos com
> um dia de atraso em relacao ao planejado e precisamos
> avaliar se todas as tarefas serao entregues no Dia 7.

**Impedimentos?**
> Nenhum impedimento tecnico. Porem, o atraso acumulado
> exige atencao — vou propor ao time foco total nas
> entregas funcionais hoje e amanha.

---

### Bruno (Developer)

**O que fiz ontem (Dia 4)?**
> Com o modelo logico recebido pela manha, finalizei
> a KAN-15 (Criar modelo Projeto) com os atributos
> corretos. Avancei bem na KAN-16 (Criar formulario
> de cadastro) — estrutura HTML pronta, mas a integracao
> com o backend ainda nao foi feita pois o banco ainda
> nao estava disponivel (KAN-42 pendente).

**O que farei hoje?**
> Vou finalizar a KAN-16 (Criar formulario de cadastro).
> Assim que Leonardo disponibilizar o banco (KAN-42),
> implementarei imediatamente a KAN-17 (Implementar
> persistencia). Tambem iniciarei a KAN-22
> (Criar modelo Atividades) para nao perder tempo.

**Impedimentos?**
> Aguardando a conclusao do banco (KAN-42) para integrar
> o formulario ao backend. (dependencia de Leonardo —
> prevista para resolucao ainda hoje pela manha)

---

### Helena (QA)

**O que fiz ontem (Dia 4)?**
> Com o ambiente padronizado pelo Leonardo, finalizei
> a KAN-38 (Validacao dos ambientes) — ambos aprovados
> e resultado registrado no repositorio. Avancei bastante
> na escrita do KAN-48 (README) com instrucoes de
> instalacao e pre-requisitos.

**O que farei hoje?**
> Vou concluir o KAN-48 (README). Também realizarei
> testes exploratorios no formulario de cadastro (KAN-16)
> assim que Bruno disponibilizar. Quero adiantar ao
> maximo os testes para compensar o atraso dos dias
> anteriores.

**Impedimentos?**
> Nenhum impedimento no momento.

---

### Resumo do Dia 5
- Impedimentos do Dia 4 resolvidos: modelo logico corrigido
  e ambiente padronizado.
- Bruno desbloqueado — formulario de cadastro em finalizacao.
- BD ainda nao implantado, gerando nova dependencia para hoje.
- Sprint com aproximadamente um dia de atraso em relacao
  ao planejado — time ciente e focado em recuperar o ritmo.
- **Nenhum novo impedimento registrado.**

---
---

## Daily Scrum — Dia 6

- **Data:** Sexta-feira — Dia 6 da Sprint
- **Horário:** 09h00 – 09h15
- **Formato:** Google Meet
- **Participantes:** Leonardo | Bruno | Helena

---

### Leonardo (Scrum Master / PO)

**O que fiz ontem (Dia 5)?**
> Finalizei a KAN-42 (Implantacao do BD) — script SQL
> criado, banco provisionado e dados de teste inseridos.
> Revisei o burndown: estamos com atraso, mas ainda e
> possivel entregar todas as funcionalidades principais
> se mantivermos o foco hoje. Iniciei a KAN-19
> (Criar tela de listagem de Projetos).

**O que farei hoje?**
> Vou finalizar a KAN-19 (Criar tela de listagem) e a
> KAN-20 (Implementar consulta ao banco). Tambem
> registrarei formalmente as dailies dos dias anteriores
> (KAN-45) e prepararei a pauta do KAN-46 (Sprint Review)
> para o Dia 7.

**Impedimentos?**
> Nenhum impedimento.

---

### Bruno (Developer)

**O que fiz ontem (Dia 5)?**
> Finalizei a KAN-16 (Criar formulario de cadastro).
> Com o banco disponibilizado pelo Leonardo, implementei
> a KAN-17 (Implementar persistencia) — rota POST criada,
> integracao com o banco funcionando para salvar projetos.
> Ao testar localmente, percebi que nao havia validacao
> de campos obrigatorios no backend — o sistema aceitava
> cadastros com titulo vazio. Corrigi antes de commitar.
> Iniciei a KAN-22 (Criar modelo Atividades).

**O que farei hoje?**
> Vou finalizar a KAN-22 (Criar modelo Atividades) e
> implementar a KAN-23 (Criar relacionamento Projeto x
> Atividade) e a KAN-24 (Criar formulario de cadastro
> de Atividade). A tarde, implementarei a KAN-26
> (Implementar atualizacao de status) e KAN-27
> (Validar transicao de status).

**Impedimentos?**
> Nenhum impedimento. Carga alta hoje, mas manageable.

---

### Helena (QA)

**O que fiz ontem (Dia 5)?**
> Finalizei o KAN-48 (README) — commitado no repositorio.
> Realizei testes exploratorios na KAN-16 (formulario
> de cadastro) e identifiquei os mesmos 2 pontos que
> Bruno ja havia corrigido (validacao de campos e feedback
> pos-submissao), alem de um novo: o formulario nao
> limpava os campos apos o cadastro bem-sucedido.
> Reportei o novo ponto para Bruno via Jira.
> Executei os testes formais da KAN-18 (Testar cadastro
> de Projeto) — aprovado apos as correcoes.

**O que farei hoje?**
> Vou executar a KAN-21 (Testar listagem de Projetos)
> assim que Leonardo finalizar a KAN-20. Tambem executarei
> a KAN-25 (Testar cadastro de Atividade) e a KAN-28
> (Testar atualizacao de status) conforme Bruno for
> entregando as funcionalidades ao longo do dia.
> E importante que eu consiga testar tudo hoje, pois
> o Dia 7 sera reservado para Review e Retrospectiva.

**Impedimentos?**
> Preocupacao com o tempo: se Bruno entregar as
> funcionalidades de Atividades somente no final da
> tarde, nao havera tempo habil para testes de integracao
> completos entre Projetos e Atividades.
> (risco identificado — nao e um bloqueio, mas merece atencao)

---

### Resumo do Dia 6 (Ultimo dia de desenvolvimento)
- BD implantado e funcional.
- US01 (Cadastrar Projeto) testada e aprovada pela QA.
- Bruno com carga alta — todas as funcionalidades de
  Atividades sendo desenvolvidas neste dia.
- Helena levanta risco real: testes de integracao entre
  Projetos e Atividades podem nao ser concluidos se as
  entregas de Bruno atrasarem.
- **Risco registrado pelo Scrum Master para discussao
  na Retrospectiva:** concentracao excessiva de tarefas
  no ultimo dia de desenvolvimento devido ao atraso
  acumulado nos dias anteriores.
- Sprint Review e Retrospective programados para o Dia 7.

---

## Resumo Geral da Sprint

| Dia | Foco Principal                             | Status              |
|-----|--------------------------------------------|---------------------|
| 1   | Sprint Planning + Setup do repositorio     | Concluido           |
| 2   | Configuracao de ambientes + Docs base      | Concluido           |
| 3   | Modelos de BD + Inicio dos formularios     | Concluido com atraso|
| 4   | Retrabalho no BD + Correcao de ambiente    | Impedimentos ativos |
| 5   | Implantacao BD + Desenvolvimento US01      | Impedimentos resolvidos|
| 6   | Finalizacao US01/US02/US03/US04 + Testes   | Concluido           |
| 7   | Sprint Review + Retrospective              | Previsto            |

---

*Documento mantido por: Leonardo (Scrum Master)*
*Ultima atualizacao: Dia 6 da Sprint*
