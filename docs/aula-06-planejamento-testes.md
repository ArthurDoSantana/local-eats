# PBL 5 - Planejamento e projeto de testes

## 1. Plano de testes

### Objetivo

Validar funcionalidades criticas para reduzir falhas com maior impacto em experiencia e confiabilidade.

### Escopo

**Dentro do escopo**

- Login
- Busca de restaurantes
- Favoritos
- Avaliacoes

**Fora do escopo**

- Teste de carga avancado
- Pentest completo
- Automacao total da regressao nesta etapa

### Estrategia

- Testes funcionais manuais baseados em risco
- Cobertura de cenarios de sucesso e erro
- Registro de evidencias
- Priorizacao de fluxos criticos

### Responsaveis

- QA 1: login e busca
- QA 2: favoritos e avaliacoes
- QA 3: evidencias e consolidacao
- Lider QA: revisao final e analise

## 2. Casos de teste (minimo 5)

### CT01 - Login com sucesso (happy path)

**Pre-condicao:** usuario valido cadastrado  
**Passos:**

1. Acessar tela de login
2. Informar e-mail e senha validos
3. Clicar em entrar

**Resultado esperado:** autenticacao concluida e redirecionamento para pagina principal.

### CT02 - Busca com filtros validos (happy path)

**Pre-condicao:** base com restaurantes cadastrados  
**Passos:**

1. Acessar busca
2. Informar termo "pizza"
3. Aplicar filtro de preco medio
4. Confirmar busca

**Resultado esperado:** lista coerente com termo e filtros.

### CT03 - Adicionar favorito (happy path)

**Pre-condicao:** usuario autenticado  
**Passos:**

1. Abrir detalhe de restaurante
2. Clicar em favoritar
3. Acessar lista de favoritos

**Resultado esperado:** restaurante visivel na lista de favoritos.

### CT04 - Login com senha invalida (erro)

**Pre-condicao:** usuario existente  
**Passos:**

1. Acessar login
2. Informar e-mail valido e senha invalida
3. Clicar em entrar

**Resultado esperado:** permanencia na tela e mensagem de erro clara.

### CT05 - Publicar avaliacao sem nota (erro)

**Pre-condicao:** usuario autenticado na tela de avaliacao  
**Passos:**

1. Inserir comentario sem nota
2. Tentar publicar

**Resultado esperado:** bloqueio da acao e mensagem de validacao de campo obrigatorio.

## 3. Execucao dos testes (simulada)

| ID | Resultado | Evidencia |
|---|---|---|
| CT01 | Passou | Login concluido e redirecionamento realizado |
| CT02 | Falhou | Busca retornou item fora da faixa de preco em cenario combinado |
| CT03 | Passou | Item favoritado exibido na lista apos navegacao |
| CT04 | Passou | Mensagem de erro exibida corretamente |
| CT05 | Falhou | Sistema permitiu envio sem nota em contexto mobile |

## 4. Analise dos resultados

- Total executado: **5**
- Passou: **3**
- Falhou: **2**
- Taxa de aprovacao: **60%**

### Principais problemas

1. Inconsistencia em filtros da busca.
2. Falha de validacao obrigatoria em avaliacao (mobile).

## 5. Reflexao final

- O plano organizou melhor a execucao e a priorizacao.
- Problemas relevantes apareceram apenas durante execucao de cenarios combinados.
- Melhorias para o proximo ciclo:
  - ampliar cobertura de combinacoes de filtro
  - checklist separado por plataforma (web/mobile)
  - regressao curta antes de cada release
  - evoluir para automacao dos fluxos criticos
