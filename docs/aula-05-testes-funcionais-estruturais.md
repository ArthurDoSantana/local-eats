# PBL 4 - Testes funcionais vs estruturais

## 1. Funcionalidade escolhida

**Busca de restaurantes** (por culinaria, localizacao e faixa de preco).

**Expectativa do usuario:** resultado correto, rapido e coerente com filtros.

## 2. Testes caixa-preta (visao do usuario)

### Entradas

- Termo valido (ex.: pizza)
- Filtros combinados
- Campo vazio
- Sem resultados
- Caracteres especiais e acentuacao

### Comportamento esperado

- Retornar restaurantes compativeis
- Atualizar lista ao aplicar/remover filtros
- Exibir mensagem clara quando nao houver resultado
- Nao quebrar interface com entradas incomuns

### Erros encontrados por essa visao

- Resultado incorreto
- Filtro ignorado
- Lentidao
- Diferenca de comportamento entre web e mobile

## 3. Testes caixa-branca (visao do sistema)

### Possivel logica interna

- Normalizacao do termo de busca
- Montagem de query dinamica por filtros
- Regra de ordenacao por relevancia/distancia
- Paginacao e cache

### Pontos para testar no codigo

- Cobertura de ramos `if/else`
- Combinacoes de filtros nulos/parciais/completos
- Tratamento de excecao da API/banco
- Timeout e fallback
- Regras de ordenacao e deduplicacao

## 4. Comparacao entre abordagens

- Caixa-preta valida o comportamento externo e valor para o usuario.
- Caixa-branca valida robustez interna e caminhos logicos.

Cada abordagem encontra problemas diferentes e complementares.

## 5. Reflexao no contexto LocalEats

A melhor estrategia e combinar as duas abordagens.

- Apenas caixa-preta: pode ocultar fragilidades internas.
- Apenas caixa-branca: pode deixar passar falhas perceptiveis ao usuario.
