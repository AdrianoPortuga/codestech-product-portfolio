# Status dos Projetos Codestech

**Atualizado em:** 2 de setembro de 2026  
**Fonte:** repositórios GitHub acessíveis da conta `AdrianoPortuga`, histórico recente de commits e documentação do portfólio.  
**Objetivo:** manter uma fotografia executiva do que está ativo, preservado, em protótipo ou apenas documentado.

## Resumo executivo

A Codestech possui atualmente um conjunto misto de produtos ativos, ativos tecnológicos preservados, protótipos e projetos conceituais.

O foco operacional atual está concentrado na **SchoolIA**, cuja implementação está distribuída principalmente entre:

- `codestech-mini-api` — backend e serviços da plataforma;
- `v0-treinamentoweb-v2-frontend` — frontend canônico da plataforma de treinamento;
- `codestech-site` — site público e fluxos de entrada/cadastro.

Os cinco sistemas legados importados em 1º de setembro permanecem preservados como patrimônio tecnológico, sem decisão de retomada imediata.

## 1. Projetos em atividade operacional

| Projeto / repositório | Situação em 02/09/2026 | Observação |
|---|---|---|
| `codestech-mini-api` | **Ativo / produção com atenção** | Backend da SchoolIA e serviços associados. Houve tentativa de Sprint 2 em 02/09, seguida de revert após falha de runtime no Railway. A árvore anterior saudável foi restaurada. |
| `v0-treinamentoweb-v2-frontend` | **Ativo / frontend canônico** | Frontend atual da SchoolIA Training OS. Possui evolução recente em configuração comercial, autenticação, recuperação de senha e fluxos CAM. |
| `codestech-site` | **Ativo** | Site institucional/comercial, com integrações e fluxo CAM; recebeu correções recentes de cadastro e mobile. |
| `codestech-product-portfolio` | **Ativo / documentação executiva** | Portfólio público seguro, sem código privado de produção. Centraliza cases, posicionamento e documentação dos produtos. |

### Ponto crítico atual — SchoolIA backend

Em 2 de setembro de 2026 foram registrados no `codestech-mini-api`:

1. commit de **Sprint 2 — entrada autônoma e matrícula configurável**;
2. posteriormente, **revert da Sprint 2 após falha de runtime no Railway**;
3. decisão técnica registrada no commit: restaurar a última árvore saudável enquanto o log do deployment é investigado.

Portanto, a SchoolIA continua sendo o produto prioritário, mas a Sprint 2 não deve ser considerada concluída em produção até nova validação do Railway.

## 2. SchoolIA — leitura consolidada

### Frontend

Repositório: `v0-treinamentoweb-v2-frontend`

**Papel atual:** plataforma web canônica de treinamento.

Evoluções recentes identificadas:

- configuração comercial dos cursos;
- recuperação de senha por telefone ou e-mail;
- autenticação e manutenção dos fluxos CAM;
- integração com backend da SchoolIA;
- área de gestão/professor e evolução do modelo de cursos.

### Backend

Repositório: `codestech-mini-api`

**Papel atual:** backend operacional da SchoolIA.

Evoluções recentes identificadas:

- motor comercial de cursos;
- matrícula e catálogo público;
- recuperação de senha;
- fluxos de alunos/professores;
- auditoria e correção do banco de questões CAM;
- integrações e rotinas de produção.

**Estado atual:** operacional na versão restaurada anterior à Sprint 2 que falhou no Railway em 02/09/2026.

### Site

Repositório: `codestech-site`

**Papel atual:** porta de entrada pública da Codestech/SchoolIA.

Evoluções recentes:

- cadastro CAM;
- tratamento de erros de registro;
- validação de ativação;
- correção de navegação mobile.

## 3. Produtos legados preservados

Estes repositórios foram importados de forma sanitizada em 1º de setembro de 2026 e analisados tecnicamente.

| Produto | Repositório | Estado | Diretriz |
|---|---|---|---|
| Gestão de Academia — API | `codestech-academia-api` | **Preservado / pausado** | Manter como ativo tecnológico. |
| Gestão de Academia — Web | `codestech-academia-web` | **Preservado / pausado** | Tratar junto com a API como um único produto futuro. |
| Cobrança Condominial WhatsApp | `codestech-condominio-whatsapp` | **Preservado / melhor candidato comercial legado** | Primeiro candidato para futura validação comercial entre os legados. |
| Portal de Influenciadores | `codestech-portal-influencers` | **Preservado / pausado** | Retomar apenas com caso comercial claro. |
| ERP Delivery | `codestech-delivery` | **Preservado / pausado** | Alto valor técnico, porém alta complexidade operacional. |

### Prioridade futura dos legados

1. Cobrança condominial por WhatsApp.
2. Gestão de academia.
3. Extração de base compartilhada/reutilizável.
4. ERP de delivery.
5. Portal de influenciadores.

Antes de qualquer relançamento: rotacionar credenciais antigas, remover dados sensíveis, atualizar dependências, criar testes e validar um cliente-piloto.

## 4. Outros produtos e experimentos no GitHub

| Repositório | Classificação atual |
|---|---|
| `newhotel-availability-agent` | Protótipo de agente para hotelaria |
| `newhotel-availability-web` | Protótipo web para hotelaria |
| `dora-roi-builder` | Conceito / ferramenta de decisão e ROI |
| `meeting-copilot` | Experimento / produto de copiloto de reuniões |
| `academia-ia-v1-robocriador` | Projeto privado experimental de IA |
| `DeepAgents` | Projeto privado de exploração técnica de agentes |
| `Projetointegracaosite` | Integração de sites / projeto de infraestrutura |
| `codestech-lead-api-docs` | Documentação pública de Lead API |
| `python-prize-wheel` | Projeto utilitário / experimental |

Esses projetos não devem competir por prioridade com a SchoolIA neste momento. Podem permanecer como ativos de experimentação, demonstração ou reaproveitamento futuro.

## 5. Projetos documentados no portfólio público

O portfólio público também contém cases e conceitos que não correspondem necessariamente a um produto em produção independente:

- EcoDigi Lab Portugal;
- Funding Portfolio OS / P01;
- Funding Radar / Portugal 2030;
- Gerês Digital Experience Network;
- NewHotel Availability Agent;
- NewHotel Availability Web;
- Dora ROI Builder;
- Codestech Mini API;
- Lead API;
- Site Integration Project;
- SchoolIA Training OS.

Esses cases servem principalmente para posicionamento executivo, apresentação a parceiros, clientes, investidores e recrutadores.

## 6. Prioridade recomendada do portfólio

### Prioridade A — executar agora

**SchoolIA Training OS**

Objetivo: estabilizar o backend, concluir de forma segura a Sprint 2 e continuar a evolução do produto canônico.

### Prioridade B — manter operacional

- Codestech Site;
- Lead/API e integrações necessárias à SchoolIA;
- portfólio público e documentação.

### Prioridade C — validar quando houver espaço comercial

**Cobrança Condominial por WhatsApp**

É o legado com melhor combinação de dor específica, venda explicável, receita recorrente e implantação relativamente controlável.

### Prioridade D — preservar sem investir agora

- Gestão de Academia;
- ERP Delivery;
- Portal de Influenciadores;
- protótipos de hotelaria;
- experimentos de agentes e automação.

## 7. Próximos checkpoints

1. Resolver a causa da falha de runtime da Sprint 2 no Railway.
2. Reaplicar a Sprint 2 somente após validação controlada.
3. Confirmar frontend + backend + fluxo de matrícula ponta a ponta.
4. Manter `v0-treinamentoweb-v2-frontend` como frontend canônico da SchoolIA.
5. Evitar abrir nova frente de produto enquanto a SchoolIA estiver em estabilização.
6. Depois da SchoolIA estabilizada, considerar discovery comercial do Condomínio WhatsApp.
7. Atualizar este documento sempre que um projeto mudar de fase: conceito → protótipo → MVP → produção → pausado.

## Conclusão

O portfólio Codestech está mais organizado do que estava antes da importação dos sistemas antigos: há hoje separação entre **produto prioritário**, **infraestrutura operacional**, **ativos legados**, **protótipos** e **cases estratégicos**.

A principal recomendação permanece simples: **não pulverizar desenvolvimento**. A SchoolIA deve continuar como produto central até estar tecnicamente estável e comercialmente utilizável. Os demais sistemas devem permanecer preservados e documentados para retomada orientada por oportunidade real de negócio.
