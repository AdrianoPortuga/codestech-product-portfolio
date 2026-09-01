# Análise do portfólio de produtos Codestech

**Data da análise:** 1 de setembro de 2026  
**Estado:** análise inicial concluída — evolução técnica pausada  
**Objetivo:** preservar a leitura estratégica e técnica dos sistemas já desenvolvidos para futuras pesquisas, decisões de produto e eventual retomada.

## Resumo executivo

A Codestech possui produtos reais, com código e funcionalidades relevantes, e não apenas protótipos. O conjunto representa um patrimônio tecnológico que pode ser reaproveitado no futuro, embora os sistemas ainda precisem de preparação técnica, segurança, testes e validação comercial antes de uma nova publicação.

Foram identificados cinco componentes principais:

1. API de gestão de academia.
2. Aplicação web de gestão de academia.
3. Cobrança condominial e envio de boletos por WhatsApp.
4. Portal de influenciadores.
5. ERP de delivery.

A orientação atual é **não avançar com correções, modernização ou implantação**. Os projetos devem permanecer preservados como ativos da Codestech até que exista uma decisão de negócio sobre qual deles retomar.

## Repositórios analisados

- `codestech-academia-api`
- `codestech-academia-web`
- `codestech-condominio-whatsapp`
- `codestech-portal-influencers`
- `codestech-delivery`

## Validação técnica inicial

| Projeto | Validação realizada | Resultado |
|---|---|---|
| Academia API | Compilação de sintaxe Python | Aprovada |
| Academia Web | Build de produção Next.js | Aprovado após fornecer variáveis obrigatórias de teste |
| Condomínio WhatsApp | Compilação de sintaxe Python | Aprovada |
| Portal de Influenciadores | Compilação de sintaxe Python | Aprovada |
| Delivery | Compilação de sintaxe Python | Aprovada |

O build inicial da Academia Web exigiu as variáveis `API_BASE_URL`, `SESSION_SECRET` e `NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME`. Com valores seguros de teste, o build foi concluído. Isso indica necessidade de configuração de ambiente, e não um bloqueio estrutural do código.

A compilação isolada não comprova o funcionamento integral. Uma validação completa exigiria bancos de dados descartáveis, configuração dos serviços externos e testes dos fluxos de negócio.

## Potencial dos produtos

### 1. Cobrança condominial por WhatsApp

**Potencial estratégico: muito alto.**

É o produto com proposta comercial mais simples de explicar: automatizar boletos, lembretes, comunicação e acompanhamento de cobrança de condomínios pelo WhatsApp.

Possíveis clientes:

- administradoras de condomínios;
- síndicos profissionais;
- empresas de cobrança;
- escritórios de contabilidade que atendem condomínios.

Possíveis modelos comerciais:

- mensalidade por condomínio;
- preço por unidade;
- preço por volume de mensagens ou cobranças;
- implantação mais assinatura mensal.

É o candidato prioritário para uma futura validação comercial, pois resolve um problema específico e permite demonstrar retorno financeiro.

### 2. Gestão de academia

**Potencial estratégico: alto, com concorrência relevante.**

O sistema contém recursos de alunos, planos, matrículas, treinos, agenda e financeiro. Pode tornar-se um SaaS para pequenas academias, estúdios, boxes e personal trainers.

O melhor posicionamento futuro não seria competir diretamente com grandes plataformas generalistas. Seria atender operações menores que procuram:

- simplicidade;
- preço acessível;
- implantação assistida;
- atendimento próximo;
- automação por WhatsApp;
- gestão de treino e evolução do aluno.

A API e a aplicação web devem ser tratadas como partes do mesmo produto.

### 3. ERP de delivery

**Potencial técnico: alto. Complexidade operacional: muito alta.**

É o sistema mais amplo do portfólio. Possui áreas ligadas a pedidos, produtos, complementos, estoque, caixa, pagamentos, entregadores, horários, cupons, campanhas, clientes, relatórios e configurações.

Esse sistema demonstra capacidade de desenvolvimento de um produto empresarial robusto. Entretanto, sua retomada exigiria:

- suporte operacional constante;
- atualização de integrações;
- segurança transacional;
- disponibilidade elevada;
- tratamento de pagamentos;
- possíveis obrigações fiscais;
- manutenção de muitos módulos;
- enfrentamento de concorrentes consolidados.

Não é recomendado como primeiro produto a ser relançado. Pode ser preservado como ativo tecnológico, base para módulos futuros ou oportunidade de parceria com uma empresa que já opere no setor.

### 4. Portal de influenciadores

**Potencial estratégico: médio.**

Possui estrutura para gerir influenciadores, empresas, perfis, relacionamento, configurações e rotinas administrativas.

Antes de uma futura retomada, será necessário definir:

- quem é o cliente pagante;
- qual problema central será resolvido;
- se o foco será agência, marca ou influenciador;
- qual vantagem oferece em relação a planilhas e plataformas existentes;
- como campanhas, métricas e pagamentos serão tratados.

O projeto deve ser mantido como oportunidade, mas não priorizado sem um caso comercial concreto ou parceiro do setor.

### 5. Base tecnológica compartilhada

**Potencial estratégico: muito alto.**

O Portal de Influenciadores e o Delivery compartilham parte relevante da arquitetura, incluindo elementos de:

- autenticação;
- utilizadores;
- grupos e permissões;
- empresas;
- chaves de API;
- auditoria;
- configurações;
- acesso a banco de dados;
- componentes administrativos;
- serviços auxiliares.

Isso mostra que a Codestech já possui uma base que poderá originar um núcleo reutilizável para novos produtos. No futuro, autenticação, permissões, auditoria e componentes comuns poderão ser extraídos para uma fundação compartilhada.

Essa unificação não deve ser realizada agora. Primeiro será necessário escolher um produto real para retomada e estabilizar a sua base.

## Situação dos testes

A cobertura automatizada atual é praticamente inexistente:

- a Academia API possui arquivos `tests.py`, mas sem uma suíte efetiva;
- a Academia Web não possui testes automatizados identificáveis;
- Condomínio, Influenciadores e Delivery também não possuem suítes relevantes.

Antes de qualquer retomada comercial, deverão ser criados testes mínimos para:

- login e renovação de sessão;
- permissões por perfil;
- isolamento de dados entre empresas;
- criação, atualização e exclusão de registros;
- fluxos financeiros;
- cobranças e mensagens;
- pedidos e pagamentos;
- tratamento de falhas de integrações externas.

## Riscos técnicos preservados para futura análise

Foram identificados pontos que deverão ser tratados antes de qualquer publicação:

1. Chaves secretas fixas no código dos backends.
2. Credencial de integração do WhatsApp escrita no código do condomínio.
3. Credencial de banco presente na configuração de migração do Delivery.
4. Chave Django fixa na Academia API.
5. Chaves Flask fixas no Portal de Influenciadores e no Delivery.
6. Backups SQL, CSV de moradores e PDF de teste no material original do condomínio.
7. Dependências desatualizadas e vulnerabilidades conhecidas na Academia Web.
8. Forte duplicação entre Influenciadores e Delivery.
9. Ausência de testes automatizados.
10. Dependência de bancos e serviços externos ainda não documentados completamente.

Os valores das credenciais não são reproduzidos neste documento. Quando houver retomada, elas deverão ser consideradas expostas, revogadas e substituídas.

## Vulnerabilidades da Academia Web

A auditoria inicial das dependências encontrou vulnerabilidades conhecidas no conjunto instalado, incluindo ocorrências críticas e altas. A versão atual do Next.js está desatualizada para publicação futura.

A atualização deverá ser planejada e acompanhada por testes, pois uma atualização direta de versão principal pode afetar:

- middleware;
- autenticação;
- cookies;
- rotas de API;
- renderização dinâmica;
- comportamento do App Router.

## Classificação estratégica

| Ativo | Prioridade futura sugerida | Uso recomendado |
|---|---:|---|
| Condomínio WhatsApp | 1 | Validação comercial e possível SaaS |
| Gestão de Academia | 2 | SaaS de nicho para pequenas operações |
| Base compartilhada | 3 | Fundação para novos produtos Codestech |
| ERP de Delivery | 4 | Reaproveitamento técnico ou parceria |
| Portal de Influenciadores | 5 | Retomar somente com caso comercial definido |

## Diretriz para futura retomada

Quando a Codestech decidir avançar, a sequência recomendada será:

1. Escolher apenas um produto para validação.
2. Entrevistar potenciais clientes e confirmar a dor.
3. Definir proposta de valor e modelo de receita.
4. Revogar e substituir credenciais antigas.
5. Remover dados pessoais e arquivos sensíveis.
6. Configurar segredos por variáveis de ambiente.
7. Atualizar dependências vulneráveis.
8. Criar testes dos fluxos críticos.
9. Subir ambiente de homologação com banco descartável.
10. Validar com clientes-piloto antes de investir em escala.

## Conclusão

A Codestech já possui ativos tecnológicos relevantes. O valor atual não está em tentar publicar todos os sistemas imediatamente, mas em preservar o conhecimento, compreender o que cada base oferece e escolher futuramente o produto com melhor combinação de:

- problema claro;
- cliente pagante identificável;
- implantação simples;
- baixo custo de suporte;
- possibilidade de receita recorrente;
- reaproveitamento da tecnologia existente.

A recomendação estratégica atual é manter todos os repositórios preservados e pausados. Se houver uma futura retomada, o sistema de cobrança condominial por WhatsApp deve ser o primeiro candidato à validação comercial, seguido pelo produto de gestão de academia.
