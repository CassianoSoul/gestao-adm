# Mesa de Triagem

Jogo de arcade de escritório para jovens aprendizes. O jogador leva cada documento ao departamento certo (Financeiro, RH, Jurídico, Logística ou Compras) antes que o prazo acabe e aprende como funciona a área administrativa durante a partida.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | Estrutura das telas (início, jogo, fim e janela de mentoria/guia). |
| `style.css` | Visual, tema claro/escuro e responsivo. |
| `conteudo.js` | Departamentos e os 35 documentos do jogo. |
| `licoes.js` | Textos de ensino: lições por área, dicas de carreira e frases do "No dia a dia". |
| `jogo.js` | Regras, pontuação, níveis, pausa, mentoria e guia. |

Para jogar, abra o `index.html` no navegador. Para publicar, envie a pasta inteira para qualquer hospedagem de site estático. Não precisa instalar nada.

## Como o aprendizado aparece no jogo

- **Depois de cada acerto:** uma frase "No dia a dia" explica o que o departamento faz com aquele tipo de documento.
- **Depois de cada erro:** uma dica explica por que o documento pertence a outro departamento.
- **A cada 6 documentos:** a Hora da Mentoria pausa o jogo e apresenta uma lição (a área ADM, cada departamento e dicas de carreira como sigilo/LGPD, conferência, prazo e organização digital).
- **Botão Guia (sempre visível):** abre o guia de todas as áreas e pausa o tempo.
- **No fim da partida:** lista os documentos errados com botão "Estudar" que abre o guia do departamento.

## Como editar o conteúdo

- Trocar ou incluir documentos: edite a lista `DOCS` em `conteudo.js` (título, departamento `d`, campos `f` e a dica de erro `tip`).
- Mudar as lições, dicas e frases: edite `licoes.js` (`LESSONS`, `FATOS` e a ordem em `MENTOR_ORDER`).
- Ajustar a dificuldade: em `jogo.js`, `DOCS_PER_LEVEL` e a função `currentDuration`.

## Detalhes técnicos

- HTML, CSS e JavaScript puros, sem bibliotecas.
- As fontes vêm do Google Fonts. Sem internet, o jogo usa fontes do sistema e continua funcionando.
- O recorde fica salvo no navegador (`localStorage`, chave `mesa-triagem-recorde`). Se o armazenamento estiver bloqueado, o jogo funciona sem salvar.
- Funciona com mouse, toque e teclado (teclas 1 a 5). Respeita a preferência de movimento reduzido do sistema.
