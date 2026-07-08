# Changelog — repositorio-luciana

Histórico de mudanças estruturais deste repositório. Não é changelog de conteúdo do dia a dia (isso fica implícito nos commits) — é para marcar decisões de organização.

## v1.1 — 08 de julho de 2026

Inspirado numa avaliação do `claude-mem` (plugin de memória de sessão para Claude Code) — não a ferramenta em si (infraestrutura própria, não fazia sentido aqui), mas 3 princípios de arquitetura que o padrão v1.0 ainda não tinha:

- **Camada de índice** (`memory/pessoas/_index.md`, `memory/projetos/_index.md`) — degrau intermediário entre o `CLAUDE.md` (top 30) e o perfil completo, escaneável antes de abrir arquivo. Mesma lógica de busca em duas etapas (índice compacto → detalhe sob demanda) usada por ferramentas de memória de sessão do Claude Code, adaptada a markdown puro.
- **Convenção de privacidade** (`## 🔒 Privado`) nos templates de pessoa e projeto — conteúdo sensível que informa o Claude sem nunca ser citado literalmente, exportado ou repassado.
- **Seção "Linha do tempo"** (opcional) nos templates de pessoa e projeto — para reconstituir histórico cronológico quando relevante, não só o estado atual.
- **Prática de encerramento de sessão** registrada em `CLAUDE.md` e `README.md`: ao final de trabalho substantivo, o Claude oferece proativamente um resumo do que vale registrar, em vez de depender só do gatilho "lembra disso" partir da pessoa.

Mesma atualização aplicada em conjunto a todos os repositórios pessoais do time (padrão Amazing PRO Personal Memory), a partir do que foi validado primeiro em `repositorio-juliana`.

## v1.0 — 07 de julho de 2026

- Criação da estrutura padrão Amazing PRO Personal Memory: `CLAUDE.md` (cache quente), `memory/` (glossário, pessoas, projetos, contexto), `melhores-praticas/`, `_meta/`.
- Repositório inicializado para Luciana.

---

**Convenção de versionamento:**
- **MAJOR:** mudança na estrutura de pastas (ex: nova categoria de memória)
- **MINOR:** nova convenção ou regra de organização adicionada
- **PATCH:** ajuste de conteúdo dentro da estrutura existente (não precisa de entrada aqui — só mudanças estruturais)
