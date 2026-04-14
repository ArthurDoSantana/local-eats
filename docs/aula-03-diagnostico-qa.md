# PBL 2 - Papeis, responsabilidades e praticas de QA

## 1. Diagnostico da situacao atual

A startup mostra crescimento rapido sem estrutura de qualidade madura:

- Erros ao finalizar pedidos
- Pedidos duplicados para restaurantes
- Defeitos chegando em producao
- Falta de clareza sobre responsavel por qualidade

### Causas provaveis

- Requisitos e criterios de aceitacao pouco claros
- Testes feitos tarde, perto da entrega
- Ausencia de triagem de bugs e definicao de severidade
- Qualidade tratada de forma reativa, nao preventiva

## 2. Papeis da equipe e relacao com qualidade

| Papel | Responsabilidades principais | Relacao com qualidade |
|---|---|---|
| Product Owner | Priorizar backlog e definir valor | Garante requisitos claros e criterios de aceitacao |
| Analista de Sistemas/Negocio | Refinar regras e fluxo | Reduz ambiguidades e defeitos de especificacao |
| Desenvolvedor | Implementar features e correcoes | Previne defeitos com testes unitarios e code review |
| QA / Analista de Qualidade | Planejar/executar testes e reportar riscos | Detecta falhas e orienta melhoria continua |
| DevOps | CI/CD, deploy e monitoramento | Evita falhas de entrega e melhora estabilidade |

## 3. Responsabilidades de qualidade

| Atividade | Responsavel principal | Apoio |
|---|---|---|
| Definir criterios de aceitacao | PO + Analista | QA + Dev |
| Revisar requisitos | Analista | PO + QA |
| Planejar testes | QA | Time |
| Executar testes funcionais | QA | Dev |
| Testes unitarios | Dev | Tech Lead |
| Registrar e priorizar bugs | QA | PO + Dev |
| Revisao de codigo | Dev | Tech Lead |
| Validacao pre-release | QA + PO | DevOps |
| Monitoramento pos-release | DevOps | QA + Dev |

## 4. Praticas basicas de QA recomendadas

1. Definition of Done com criterios minimos de qualidade.
2. Triagem semanal de bugs por severidade e impacto.
3. Regressao dos fluxos criticos (login, pedido, confirmacao, status).
4. Code review obrigatorio para toda feature.
5. Checklist de release com smoke test e plano de rollback.

## 5. Anuncios de contratacao

### Vaga 1: Analista de Qualidade de Software (QA)

**Empresa:** Local Eats  
**Modelo:** Hibrido

**Descricao da vaga**  
Atuar na estruturacao dos testes, prevencao de defeitos e melhoria continua da qualidade.

**Principais responsabilidades**

- Planejar e executar testes funcionais e regressivos
- Criar e manter casos de teste
- Registrar e acompanhar bugs
- Apoiar criterios de aceitacao com PO e Dev
- Comunicar riscos de qualidade

**Requisitos obrigatorios**

- Base em testes de software
- Boa escrita de cenarios e evidencias
- Comunicacao e colaboracao com time tecnico
- Nocoes de Git

**Requisitos desejaveis**

- Experiencia com testes web/mobile
- Ferramentas de bug tracking
- Nocoes de automacao

**Certificacoes/cursos relevantes**

- ISTQB CTFL
- Cursos de testes funcionais e API

### Vaga 2: DevOps Junior/Pleno

**Empresa:** Local Eats  
**Modelo:** Hibrido/Remoto

**Descricao da vaga**  
Consolidar pipeline de entrega e monitoramento para aumentar confiabilidade de releases.

**Principais responsabilidades**

- Manter pipeline CI/CD
- Automatizar build, teste e deploy
- Monitorar erros e disponibilidade
- Definir estrategia de rollback
- Suportar observabilidade

**Requisitos obrigatorios**

- Conhecimento de CI/CD
- Git
- Nocoes de nuvem
- Troubleshooting basico

**Requisitos desejaveis**

- Docker
- Ferramentas de monitoramento
- Feature flags e deploy gradual
