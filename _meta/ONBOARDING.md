# Onboarding — Roteiro de Entrevista de Personalização

> Este arquivo é lido pelo Claude quando a pessoa pede para "personalizar" ou
> "preparar" este repositório. Não é conteúdo para a pessoa ler — é o roteiro
> que você (Claude) segue para conduzir a entrevista.

## Como conduzir

- Um bloco por vez. Não despeje todas as perguntas de uma vez — isso é
  formulário, não conversa.
- Use a ferramenta de perguntas com opções sempre que a pergunta tiver
  respostas naturalmente fechadas (blocos 2 e 5). Use texto livre para tudo
  que for aberto (blocos 1, 3, 4, 6).
- Depois de cada bloco, já escreva o resultado no arquivo correspondente do
  repositório — commit direto, não precisa esperar o fim da entrevista
  inteira para salvar.
- Se a pessoa já tiver preenchido parte do `CLAUDE.md` (ex: "Quem sou" já
  tem algo além do placeholder), confirme em vez de perguntar do zero: "vi
  que você já é [X] — ainda é isso?"
- Se alguma resposta envolver informação sensível sobre terceiros (um
  atrito com colega, uma avaliação de desempenho, algo confidencial de
  cliente), pergunte se aquele trecho deve ficar marcado como
  `## 🔒 Privado` no arquivo — não decida sozinho qual conteúdo é sensível.
- Ao criar um perfil novo em `memory/pessoas/` ou `memory/projetos/`, sempre
  adicione a linha correspondente em `_index.md` no mesmo commit — perfil
  sem entrada no índice é invisível na prática.
- No fim, escreva uma entrada em `_meta/CHANGELOG.md` marcando a
  personalização inicial concluída, e dê à pessoa um resumo curto do que foi
  salvo + como usar o repositório no dia a dia (não repita a entrevista
  inteira, só o essencial). Esse resumo final segue a mesma lógica da
  prática de "encerramento de sessão" já registrada no `CLAUDE.md` — é a
  primeira vez que ela se aplica neste repositório.
- Governança: não toque em nenhum outro repositório do GitHub durante esse
  processo, mesmo que pareça relacionado.

## Bloco 1 — Identidade

Vai para `CLAUDE.md` → seção "Quem sou".

- Qual seu nome e cargo/squad na Amazing PRO?
- O que você faz no dia a dia, em uma ou duas frases? (não o cargo formal —
  o trabalho de verdade)
- Há quanto tempo você está nesse papel?

## Bloco 2 — Como você quer ser respondido

Vai para `CLAUDE.md` → seção "Preferências de trabalho". Este é o bloco
mais importante — é o que mais muda a experiência do dia a dia.

- Você prefere respostas curtas e diretas, ou completas e explicadas?
- Prefere listas/tópicos ou texto corrido?
- Quando a tarefa é ambígua, prefere que eu tome uma decisão razoável e
  siga em frente, ou que eu pergunte antes?
- Tem algum padrão de escrita de IA que te incomoda especificamente?
  (bajulação tipo "ótima pergunta!", excesso de ressalvas, respostas mais
  longas do que precisava, tom robótico, emojis em excesso, etc.)
- Português informal, formal ou técnico — qual o seu tom natural?

## Bloco 3 — Pessoas e projetos

Vai para `memory/pessoas/` e `memory/projetos/` (um arquivo por
pessoa/projeto, a partir do `_template.md`, com a linha correspondente
criada em `_index.md`), com as mais frequentes promovidas para as tabelas
em `CLAUDE.md`.

- Quais as 3 a 5 pessoas com quem você mais fala ou trabalha? Papel de cada
  uma e como prefere ser contatada.
- Em que projetos você está agora? Uma frase de contexto para cada.
- (Se relevante) Alguma dessas relações ou projetos tem histórico que vale
  reconstituir? Pode virar uma seção "Linha do tempo" no perfil, em vez de
  só o estado atual.

## Bloco 4 — Jeito de trabalhar

Vira arquivos em `melhores-praticas/`, a partir do `_template.md` — um
arquivo por prática, não um catch-all.

- Existe algum processo ou checklist que você repete sempre e queria que eu
  seguisse sem precisar reexplicar?
- Algum erro que já aconteceu (com IA ou com outra ferramenta) que você
  quer que eu evite?
- Algum formato que você usa com frequência — e-mail padrão, estrutura de
  relatório, template de resposta a cliente?

## Bloco 5 — Glossário

Vai para `memory/glossario.md`, com os termos mais usados promovidos ao
"Glossário rápido" do `CLAUDE.md`.

- Tem sigla, apelido ou termo interno do seu time que eu deveria saber
  decodificar sem perguntar?

## Bloco 6 — Fechamento

- Pergunte se a pessoa já tem histórico longo em outras conversas com o
  Claude — se tiver, sugira o fluxo opcional do `README.md` (extração de
  preferências de conversa antiga) como complemento, não substituto, desta
  entrevista.
- Escreva o resumo final e a entrada no `_meta/CHANGELOG.md`.
