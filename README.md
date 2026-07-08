# repositorio-luciana

> Repositório pessoal de **Luciana** no ecossistema Claude da Amazing PRO — memória de trabalho, melhores práticas e contexto acumulado ao longo do uso diário.

**Padrão:** Amazing PRO Personal Memory v1.2 | **Última atualização:** 08 de julho de 2026

---

## O que é este repositório

Este não é um repositório de código nem de skills compartilhadas — é o **cérebro pessoal** de Luciana dentro do Claude. Serve para três coisas:

1. **Memória de trabalho** — quem são as pessoas, projetos e termos que Luciana usa no dia a dia, para o Claude entender o contexto sem precisar reexplicar tudo a cada conversa.
2. **Melhores práticas** — processos, aprendizados e formas de trabalhar que Luciana quer que o Claude siga de forma consistente.
3. **Registro vivo** — um lugar que cresce com o tempo, em vez de se perder em conversas isoladas que não se conectam.

Ele é **irmão** do repositório mestre [`amazing-skills`](https://github.com/amazingthiago/amazing-skills), que contém as skills, agentes e metodologias oficiais da Amazing PRO. A relação entre os dois:

| | `amazing-skills` | `repositorio-luciana` |
|---|---|---|
| **O que guarda** | Metodologia oficial, skills, agentes, frameworks | Contexto pessoal, memória, práticas individuais |
| **Quem edita** | Time de metodologia / Thiago | Luciana |
| **Escopo** | Toda a empresa | Só o trabalho de Luciana |
| **Fonte da verdade para** | Como fazer (framework, processo, voz) | Quem, o quê, quando, como Luciana trabalha |

**Regra de ouro:** se a informação é sobre *método* (como a Amazing PRO faz X), ela pertence ao `amazing-skills`. Se é sobre *contexto pessoal* (quem Luciana conversa, quais projetos toca, como prefere trabalhar), pertence aqui.

---

## Onboarding — primeira personalização

Repositório novo ou ainda com os placeholders do template? Comece por aqui.

**1. Instruções do Claude** (uma vez, em Configurações → Preferências):
```
Use por MCP direto do GitHub o meu repositório de memória pessoal:
https://github.com/amazingthiago/repositorio-luciana

Leia o CLAUDE.md desse repositório para ter contexto sobre mim.
Nunca altere nenhum outro repositório do GitHub sem eu pedir isso
explicitamente nesta conversa.
```

**2. Disparar a entrevista** — nova conversa, cole:
```
Vamos personalizar meu repositório de memória pessoal:
https://github.com/amazingthiago/repositorio-luciana

Acesse o repositório e leia o arquivo _meta/ONBOARDING.md — ele tem o
roteiro da entrevista de personalização. Conduza a entrevista com base
nele, um bloco de perguntas por vez, no ritmo de uma conversa normal
(não me jogue tudo de uma vez).

Ao final de cada bloco, já vá salvando o que fizer sentido diretamente
no repositório (commit direto, não precisa pedir confirmação a cada
arquivo). A única regra é: não altere nenhum outro repositório sem eu
pedir explicitamente.

Quando terminar, me dê um resumo do que foi salvo e as instruções de
como usar o repositório no dia a dia.
```

**3. Responder a entrevista** — conversa normal. Seja direto no bloco sobre estilo de comunicação — é o que mais muda a experiência no dia a dia.

**4. [Opcional] Já tem conversas longas e produtivas com o Claude?** Funda preferências de lá também, em vez de recomeçar do zero. Na conversa antiga, cole:
```
Extraia minhas preferências, padrões e modelos de operação desta
conversa. Remova os vieses que podem atrapalhar a produtividade ou a
qualidade da resposta (elogios desnecessários, hedging, respostas
mais longas do que o necessário, e qualquer outro padrão que você
perceber que não me serve).
```
Depois que o Claude responder, cole:
```
Agora acesse meu repositório: https://github.com/amazingthiago/repositorio-luciana

Leia o _meta/ONBOARDING.md e o CLAUDE.md atual para entender a
governança do repositório, e funda essas preferências que você acabou
de extrair com o que já está salvo — sem duplicar e sem apagar nada
que já esteja lá, a menos que entre em contradição direta (nesse caso,
a informação mais recente vence).

Não altere nenhum outro repositório.
```

Roteiro completo da entrevista: `_meta/ONBOARDING.md`.

---

## Estrutura de pastas

```
repositorio-luciana/
├── README.md                  ← este arquivo
├── CLAUDE.md                  ← cache quente: carregado automaticamente pelo Claude
├── melhores-praticas/         ← processos e aprendizados que Luciana quer preservar
│   ├── README.md               (como registrar uma prática nova)
│   └── _template.md            (modelo para copiar)
├── memory/                    ← base completa de memória (consultada sob demanda)
│   ├── glossario.md            (decodificador completo de termos e siglas)
│   ├── pessoas/
│   │   ├── _index.md           (índice escaneável — camada intermediária, ver abaixo)
│   │   ├── _template.md        (modelo para copiar)
│   │   └── ...                 (um arquivo por pessoa)
│   ├── projetos/
│   │   ├── _index.md           (índice escaneável — camada intermediária, ver abaixo)
│   │   ├── _template.md        (modelo para copiar)
│   │   └── ...                 (um arquivo por projeto)
│   └── contexto/
│       └── empresa.md          (contexto institucional Amazing PRO)
└── _meta/
    ├── CHANGELOG.md            (histórico de mudanças estruturais deste repositório)
    └── ONBOARDING.md           (roteiro da entrevista de personalização, para o Claude seguir)
```

---

## Como usar

**1. Clone o repositório** e abra o Claude (Code, Desktop ou Cowork) dentro dessa pasta. O `CLAUDE.md` é carregado automaticamente no início de cada sessão — é ele que dá ao Claude o contexto de quem é Luciana, com quem trabalha e em quê.

**2. Durante o trabalho**, quando disser "lembra disso", "isso é importante guardar" ou similar, o Claude deve registrar a informação no lugar certo (ver regras abaixo) e, se relevante, referenciar em `CLAUDE.md`.

**3. Quando precisar de contexto profundo** (perfil completo de uma pessoa, histórico de um projeto), o Claude consulta o índice em `memory/pessoas/_index.md` ou `memory/projetos/_index.md` primeiro, e só abre o arquivo completo se valer a pena — não precisa estar tudo em `CLAUDE.md`.

---

## Como organizar — regra de promoção/demoção

O `CLAUDE.md` deve ficar **enxuto** (até ~100 linhas). Ele é o "top 30" — o que é usado com frequência. Tudo o resto vive em `memory/`.

| Tipo de informação | Vai para `CLAUDE.md` quando... | Vai para `memory/` quando... |
|---|---|---|
| Pessoa | É contato frequente / ativo | Sempre (perfil completo) — só promove ao CLAUDE.md se virar frequente |
| Termo/sigla | É usado quase toda semana | Sempre (glossário completo) |
| Projeto | Está ativo agora | Projeto encerrado ou pausado → só em `memory/`, remove do CLAUDE.md |
| Preferência de trabalho | Sempre no CLAUDE.md | — |
| Melhor prática | Nunca — vive em `melhores-praticas/` | — |

**Na prática:**
- Projeto encerrou → tira de `CLAUDE.md`, mantém o histórico em `memory/projetos/`.
- Pessoa virou contato raro → tira de `CLAUDE.md`, mantém o perfil em `memory/pessoas/`.
- Termo novo aparece uma vez → vai direto para `memory/glossario.md`. Se voltar a aparecer com frequência, promove para `CLAUDE.md`.

---

## Camada de índice — entre o `CLAUDE.md` e o perfil completo

`CLAUDE.md` cobre o "top 30" e `memory/` guarda tudo — mas entre os dois faltava um degrau: como o Claude decide, sem abrir todos os arquivos, se existe um perfil relevante pra uma pessoa ou projeto que não está no `CLAUDE.md`?

Para isso existem `memory/pessoas/_index.md` e `memory/projetos/_index.md` — uma linha por entrada, barata de escanear (nome, papel/status, qual arquivo abrir). O Claude consulta o índice primeiro; só abre o arquivo completo se o índice indicar que vale a pena. É a mesma lógica de busca em duas etapas (índice compacto → detalhe completo só do que interessa) usada por ferramentas de memória de sessão do Claude Code — adaptada aqui para arquivos markdown, sem precisar de banco de dados nem processo rodando.

**Regra:** todo perfil novo em `memory/pessoas/` ou `memory/projetos/` ganha uma linha no índice correspondente no mesmo commit em que é criado. Perfil sem entrada no índice é, na prática, invisível — ninguém vai adivinhar que existe.

---

## Convenção de privacidade

Este repositório vai acumular informação sensível — impressão sobre pessoas, decisões internas, coisas que Luciana quer que o Claude *saiba* pra ter contexto, mas nunca *repita* fora de lugar (numa citação, num resumo exportado, num relatório pra terceiros).

Para isso, marque o trecho com uma seção `## 🔒 Privado`:

```markdown
## 🔒 Privado

[Conteúdo que o Claude pode usar para entender contexto, mas nunca deve citar
literalmente, exportar, ou repetir para quem não seja o próprio Luciana.]
```

**Regra para o Claude:** conteúdo sob `## 🔒 Privado` informa o raciocínio, mas nunca aparece verbatim na resposta — nem em resumos, nem em documentos gerados, nem repassado a outra pessoa. Se uma tarefa exige compartilhar algo que só existe nessa seção, pergunte a Luciana antes de usar.

---

## Como manter atualizado

- **Toda sexta-feira (ou ao fim de um ciclo de trabalho):** revisar `CLAUDE.md` — o que ficou obsoleto sai, o que virou frequente entra.
- **Ao final de uma sessão de trabalho substantiva:** antes de encerrar, o Claude oferece proativamente um resumo rápido do que valeria registrar (pessoa nova mencionada, decisão tomada, prática que se repetiu) — não depende só do gatilho "lembra disso" partir de Luciana. Luciana aceita, ajusta ou dispensa a sugestão.
- **Ao aprender algo que quer repetir:** criar um arquivo em `melhores-praticas/` a partir do `_template.md`. Não deixar isso só na conversa — se não vira arquivo, se perde.
- **Ao mudar a estrutura deste repositório** (nova pasta, nova regra, nova convenção): registrar em `_meta/CHANGELOG.md`.
- **Nunca inflar o `CLAUDE.md`** — se uma informação parece "importante demais para não estar lá", provavelmente é porque virou uma preferência de trabalho (vai pro CLAUDE.md) ou porque merece virar uma prática documentada (vai pra `melhores-praticas/`). Detalhe e histórico sempre vão para `memory/`.

---

## Dúvidas frequentes

**"Isso é uma skill ou uma memória pessoal?"**
Se é um framework/processo que a Amazing PRO usa oficialmente (ex: ROMA, Destilador) → pertence a `amazing-skills`, não aqui. Se é "como Luciana gosta de trabalhar" ou "quem é quem no time de Luciana" → aqui.

**"Posso apagar coisas antigas?"**
Prefira mover para `memory/` em vez de apagar. Histórico tem valor — o que sai do `CLAUDE.md` não precisa sair do repositório.

**"Preciso pedir permissão pra editar isso?"**
Não. Este repositório é de Luciana. A única regra é manter a estrutura — para que outros repositórios do time sigam o mesmo padrão e possam ser auditados/consolidados no futuro.
