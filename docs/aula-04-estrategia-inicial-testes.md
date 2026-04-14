# PBL 3 - Estrategia inicial de testes

## 1. Funcionalidades principais

1. Login/Cadastro
2. Busca de restaurantes (culinaria, localizacao, preco)
3. Visualizacao de cardapio e detalhes
4. Favoritos
5. Avaliacoes
6. Recomendacoes personalizadas

## 2. Niveis de teste por funcionalidade

| Funcionalidade | Unitario | Integracao | Sistema | Aceitacao |
|---|---|---|---|---|
| Login/Cadastro | Validacao de e-mail/senha e regras de autenticacao | Front + API + banco | Fluxo completo de login/sessao | Usuario cria conta e entra sem erro |
| Busca | Regras de filtro/ordenacao/paginacao | Front + servico de busca + base | Busca com filtros combinados | Usuario encontra resultado correto rapidamente |
| Cardapio/Detalhes | Regras de exibicao de dados | API de restaurantes + imagens | Fluxo completo da tela de detalhes | Usuario entende opcoes e informacoes |
| Favoritos | Adicionar/remover/persistir | Conta + endpoint de favoritos | Favoritar/desfavoritar em web/mobile | Usuario salva e recupera favoritos |
| Avaliacoes | Validacao de nota/comentario | Usuario + restaurante + servico | Publicar/listar apos refresh | Usuario ve avaliacao persistida |
| Recomendacoes | Regras de personalizacao | Historico + perfil + motor | Lista personalizada por usuario | Usuario recebe sugestoes relevantes |

## 3. Prioridades e riscos

**Alta prioridade**

- Login/Cadastro: bloqueia toda a jornada.
- Busca: funcionalidade central do produto.
- Avaliacoes: impacto direto na confianca da plataforma.

**Media prioridade**

- Cardapio/Detalhes
- Favoritos
- Recomendacoes

## 4. Piramide de testes

- **Base (maior volume):** unitarios (~60%), por custo baixo e resposta rapida.
- **Meio:** integracao (~30%), para contratos entre modulos e servicos.
- **Topo (menor volume):** sistema/aceitacao (~10%), focado em fluxos criticos ponta a ponta.

## 5. Testes em producao

Sim, de forma controlada:

- Monitoramento sintetico para login e busca
- Feature flags para liberacao gradual
- Canary release para pequena parcela de usuarios
- Observabilidade de erro, latencia e taxa de sucesso

Com plano de rollback e alertas automaticos.
