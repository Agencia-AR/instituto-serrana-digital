---
project: Instituto Serrana Digital
document: Roteiro da Reunião de Descoberta
version: "1.0"
date: 2026-09-04
status: PROPOSTA — pronto para revisão do Adão antes de apresentar ao Instituto
gera: prompts/discovery-presentation.md
---

# Roteiro da Reunião de Descoberta — Instituto Serrana Digital

> **Gerado a partir de** `prompts/discovery-presentation.md`, lendo `docs/product/01-prd.md`,
> `docs/architecture/01-architecture.md`, `docs/discovery/01-meeting-plan.md`,
> `docs/design/01-penpot-brief.md`, `docs/architecture/03-integrations.md` e
> `docs/discovery/02-decisions-assumptions.md`.
>
> **Regra de condução:** nada aqui apresentado como fato confirmado do Instituto.
> Marcar sempre a natureza — `CONFIRMADO` (fonte pública), `PROPOSTA` (nossa direção),
> `PENDENTE` (depende deles). O protótipo é **instrumento de descoberta**, não entrega final.

---

## 0. Como usar este documento

- **Seções 1–4** — preparo e abertura.
- **Seção 5** — o minuto a minuto da versão de 60 min (a que será usada na reunião).
- **Seção 6** — o detalhamento tela a tela (fala + perguntas + decisão), fonte da seção 5.
- **Seção 7** — como falar de integrações sem prometer o que não está confirmado.
- **Seções 8–11** — o que precisa sair da reunião.
- **Seção 12** — a versão de 15 min (corredor / call rápida).
- **Seção 13** — Matriz da Apresentação (uma linha por tela).
- **Seção 14** — o que ajustar no protótipo Penpot **antes** da reunião (P0/P1/P2).

---

## 1. Objetivo da reunião

Uma reunião, duas funções ao mesmo tempo:

| Função | O que significa |
|---|---|
| **A) Apresentar a visão** | Mostrar, com um protótipo navegável concreto, o potencial da plataforma pública + administrativa e a experiência Santa Rita → Bolerata. Sair da conversa abstrata. |
| **B) Descobrir e decidir** | Validar hipóteses, coletar requisitos reais (operação de mesas, ferramentas atuais, usuários, financeiro) e transformar `PENDENTE` em `DECISÃO`. |

**Resultado esperado ao final:** escopo do MVP acordado, responsáveis definidos, lista de acessos/documentos a entregar, e data do próximo gate.

> A reunião **não começa do zero**: já existe uma proposta. Ela serve para lapidar, não para inventar.

---

## 2. Duração e formato

| Versão | Duração | Quando usar |
|---|---|---|
| **Completa** | 45–60 min + 15 min de conversa aberta | Reunião oficial de descoberta, com diretoria/equipe |
| **Curta** | 15 min | Alinhamento rápido, call de corredor, quando só há uma pessoa disponível |

- **Formato:** apresentação de tela compartilhada navegando o protótipo Penpot em modo apresentação, com uma pessoa conduzindo e uma anotando decisões na **Matriz de validação** (`docs/discovery/01-meeting-plan.md` §4).
- **Presencial de preferência.** Se remoto, gravar (com consentimento) para não perder nenhuma resposta de descoberta.
- **Material de apoio aberto em paralelo:** `docs/apresentacao-descoberta.html` (design system + telas + perguntas + checklist), para consulta e para deixar com o Instituto ao final.

---

## 3. Sequência de apresentação (visão macro)

```text
1. Contexto e visão            (por que existe, o que é)
2. Experiência pública          Home Santa Rita → Instituto → Projetos → Eventos
3. Bolerata                     página → temporada → edição → Sympla → 2 mapas de mesa
4. Plataforma administrativa    dashboard → CRM → atendimento → financeiro → projetos → RH
5. Integrações                  Sympla, WhatsApp (Meta baseline), Instagram, n8n, IA
6. Descoberta guiada            perguntas críticas que ficaram para o final
7. Decisões e próximos passos   escopo MVP, responsáveis, acessos, data do gate
```

Princípio de ritmo: **público primeiro** (encanta, alinha a narrativa), **admin depois** (mostra o valor operacional), **descoberta ao final** (quando eles já entenderam o produto e respondem melhor). Perguntas rápidas de validação vão sendo feitas ao longo do caminho; as perguntas longas ficam para o bloco 6.

---

## 4. Storytelling de abertura (2–3 min, fala sugerida)

> "O Instituto Serrana existe desde 2001 cuidando da memória, da cultura e do patrimônio do Serro. Hoje essa história está espalhada — um pouco no site, um pouco no Instagram, um pouco na Sympla, um pouco em planilhas e conversas de WhatsApp.
>
> A ideia da plataforma é simples de dizer e grande de fazer: **dar ao Instituto um lugar digital só dele**, que faça duas coisas.
>
> A primeira, para quem vê de fora: contar essa história de um jeito que emociona. A gente parte da base da escadaria da Igreja de Santa Rita e sobe, degrau por degrau, até a igreja — e nessa subida aparece o que o Instituto faz: memória, cultura, patrimônio, comunidade.
>
> A segunda, para quem trabalha por dentro: parar de perder informação. Toda venda da Bolerata, todo contato, toda despesa, todo documento num lugar só, com visão de quem comprou, quanto entrou, o que falta fazer.
>
> O que vou mostrar agora é uma **proposta visual** — um protótipo. Nada aqui está fechado. O objetivo de hoje é vocês reagirem: o que faz sentido, o que muda, o que falta."

**Não dizer:** "está pronto", "vai funcionar assim", "a Sympla permite isso" (sem confirmação), "a missão de vocês é X" (é proposta de redação).

---

## 5. Roteiro minuto a minuto — versão 60 min

| Min | Bloco | Objetivo | O que mostrar | Perguntas rápidas | Decisão esperada |
|---|---|---|---|---|---|
| 0–3 | **Abertura** | Contexto e enquadramento | Slide de capa + frase da visão | — | — |
| 3–5 | **Dois ambientes** | Explicar Portal Público + Plataforma Administrativa | Diagrama simples (2 caixas) | "Faz sentido separar o site de quem visita do sistema de quem trabalha?" | Confirmar os 2 ambientes |
| 5–12 | **Home Santa Rita** | Encantar; alinhar a narrativa de entrada | Scroll da home: base da escadaria → subida → chegada na igreja → identidade | "A sequência Memória · Cultura · Patrimônio · Comunidade está certa?" "Vocês têm foto/vídeo da escadaria e da igreja?" | Aprovar conceito da home; identificar quem fornece mídia |
| 12–17 | **Área institucional** | Mostrar como a história e a transparência ficam | Página Instituto (história, missão, valores, diretoria), Áreas de atuação, Transparência | "Quem aprova o texto institucional?" "Quais documentos podem ser públicos?" | Definir responsável por conteúdo; lista inicial de documentos públicos |
| 17–20 | **Projetos e Eventos** | Base reaproveitável para além da Bolerata | Lista de projetos + página de projeto + agenda de eventos | "Quais projetos entram no lançamento?" | Selecionar 2–3 projetos para o MVP |
| 20–22 | **Bolerata — página e temporada** | Identidade própria do evento | Hero da Bolerata (tema preto/dourado), grade da temporada | "A Bolerata tem identidade visual própria hoje? Logo, cores?" | Confirmar tratamento visual separado |
| 22–26 | **Bolerata — página de edição + jornada Sympla** | Como o visitante compra | Página de uma edição → CTA "Reservar/Comprar" → fluxo oficial Sympla | "Hoje a venda é 100% Sympla? Tem contrato e quem administra?" | Confirmar Sympla como fonte de venda na 1ª etapa |
| 26–33 | **Dois mapas de mesa** | O ponto mais sensível da operação | Mapa A (ilustrado, público) e Mapa B (operacional, numerado, com estados) | Bloco de perguntas da seção 8.4 (comercialização de mesa, setores, cortesias, bloqueios, planta oficial, check-in) | Entender como a mesa é vendida hoje; decidir se o mapa é só ilustrativo ou operacional no MVP |
| 33–40 | **Dashboard + Eventos (admin)** | Valor executivo: "o que está acontecendo agora" | Dashboard (próxima edição, ocupação, receita, pendências, falhas de integração) + tela de Eventos | "Quais números a diretoria acompanha hoje?" "Quem vê o quê?" | Lista dos 6–8 indicadores do MVP; perfis de acesso |
| 40–45 | **CRM + Atendimento** | Parar de perder contato e histórico | Pipeline (kanban), ficha 360º de um contato, tela de atendimento omnichannel com resumo por IA | "Quem responde WhatsApp hoje?" "Onde ficam os contatos?" | Confirmar canais do MVP (WhatsApp + Instagram + formulário) |
| 45–49 | **Financeiro + Projetos/Patrocínios** | Visão gerencial, sem substituir contabilidade | Financeiro por centro de custo (Instituto / Bolerata / projetos), previsto x realizado; prestação de contas de projeto | "Como as despesas são vinculadas a evento/projeto hoje?" "Tem contador? Ele terá acesso?" | Definir se financeiro entra no MVP e em que profundidade |
| 49–52 | **Integrações** | Enquadrar sem prometer | Diagrama: plataforma ↔ n8n ↔ Sympla / Meta / Instagram / e-mail / IA | "Vocês já têm Meta Business e número de WhatsApp comercial?" | Caminho oficial do WhatsApp = Meta Cloud API |
| 52–58 | **Descoberta guiada** | Fechar as perguntas críticas restantes | Voltar à lista de perguntas da seção 8 ainda em aberto | (todas as pendentes) | Transformar o máximo de `PENDENTE` em `DECISÃO` |
| 58–60 | **Fecho** | Combinar o próximo passo | Slide de próximos passos + lista de acessos | "Quem é o ponto de contato para nos passar os acessos?" | Responsável, prazo dos documentos, data do próximo gate |

> **Se estourar o tempo:** cortar 17–20 (Projetos/Eventos) e 45–49 (Financeiro) — são os blocos mais "para depois". Nunca cortar 26–33 (mapas de mesa) nem 52–58 (descoberta).

---

## 6. Roteiro detalhado por tela

Cada tela: **objetivo · o que mostrar · mensagem principal · fala sugerida · perguntas · decisão esperada**.

### 6.1. Home — experiência Santa Rita

- **Objetivo:** encantar e fixar a narrativa de entrada do portal.
- **O que mostrar:** o scroll completo — Estado 0 (base da escadaria, "Instituto Serrana — Cultura, memória e desenvolvimento no coração do Serro") → subida com os marcos Memória · Cultura · Patrimônio · Comunidade → Estado 5 (chegada frontal à igreja + identidade + CTAs). Mostrar também a versão `prefers-reduced-motion` (imagem estática + texto).
- **Mensagem principal:** "A home não é um banner — é uma pequena viagem que já diz quem é o Instituto antes de qualquer menu."
- **Fala sugerida:** "Quando alguém abre o site, começa aqui embaixo, na base da escadaria, com a igreja lá no alto. Conforme rola a página, sobe a escadaria — e cada trecho apresenta uma parte do trabalho de vocês. No topo, chega na igreja e aparece a identidade do Instituto e para onde ir: conhecer, apoiar, ver a Bolerata."
- **Perguntas:**
  - `PENDENTE` A sequência **Memória · Cultura · Patrimônio · Comunidade** representa bem a atuação? Falta ou sobra algo?
  - `PENDENTE` Vocês têm **fotografia e/ou vídeo** da escadaria e da igreja em boa resolução? Direitos de uso?
  - `PENDENTE` Existe alguma **restrição** sobre uso da imagem da Igreja de Santa Rita (é bem tombado / religioso)?
  - `PROPOSTA` O texto de chegada ("Preservar o passado. Mobilizar o presente. Construir novos caminhos.") funciona ou querem outra redação?
- **Decisão esperada:** conceito da home aprovado (sim/ajustes); responsável por fornecer mídia; ok para usar imagem da igreja.

### 6.2. Área institucional (Instituto · Áreas de atuação · Transparência)

- **Objetivo:** mostrar como história, missão e transparência ficam publicadas e mantidas pela equipe.
- **O que mostrar:** página "O Instituto" (história desde 2001, missão, visão, valores, diretoria, atuação); grade das Áreas de atuação; página de Transparência (estatuto, relatórios, atas, prestações de contas publicáveis); menção ao CMS (equipe edita sem depender de programador).
- **Mensagem principal:** "Tudo isso é editável por vocês. A gente entrega a estrutura; o conteúdo vive nas mãos do Instituto."
- **Fala sugerida:** "Essa parte conta a história do Instituto e mostra transparência — que para uma organização como a de vocês vale muito. O texto que está aqui é **rascunho nosso**, para vocês corrigirem. E a diretoria e os documentos vêm de vocês."
- **Perguntas:**
  - `PENDENTE` **Missão, visão e valores** — confirmar a redação oficial (a que está no protótipo é `PROPOSTA DE REDAÇÃO`).
  - `PENDENTE` Quem é a **diretoria atual**? Há foto e biografia curta?
  - `PENDENTE` Qual o **nome institucional exato** a exibir? E confirmam **"Instituto Serrana Digital"** como nome da plataforma?
  - `PENDENTE` Quais **documentos** podem ser públicos hoje (estatuto, atas, prestações de contas)? Quais nunca?
  - `PENDENTE` Quem **aprova** publicação de conteúdo? Existe fluxo (rascunho → revisão → aprovação)?
- **Decisão esperada:** responsável por conteúdo institucional; lista inicial de documentos públicos; confirmação de nomes.

### 6.3. Bolerata (página temática · temporada · página de edição)

- **Objetivo:** mostrar a Bolerata com **identidade própria** (preto / dourado / marfim), ligada mas distinta do tema institucional.
- **O que mostrar:** Hero da Bolerata (arte/foto, próxima edição, data, local, CTA); grade da temporada com todas as edições e situação; página de uma edição (data, horário, local, programação, artistas, acessibilidade, FAQ, patrocinadores, botão de reserva/compra).
- **Mensagem principal:** "A Bolerata é o primeiro grande caso de uso. Se funcionar bem para ela, funciona para qualquer evento futuro do Instituto."
- **Fala sugerida:** "A Bolerata ganha uma página com cara de evento — mais escura, mais elegante — mas dentro do mesmo site. Aqui o visitante vê a temporada inteira, entra numa edição, vê a programação e clica para reservar."
- **Perguntas:**
  - `PENDENTE` A Bolerata tem **identidade visual** hoje (logo, cores, tipografia)? Podem compartilhar?
  - `PENDENTE` Quantas **edições** tem a temporada atual/próxima? Já há datas e locais definidos?
  - `PENDENTE` Existe **material** (fotos, vídeos, arte) das edições anteriores para a galeria?
  - `PENDENTE` A programação/line-up costuma mudar perto da data? (impacta quem edita e com que antecedência)
- **Decisão esperada:** tratamento visual separado aprovado; fonte da identidade da Bolerata; nº de edições no MVP.

### 6.4. Os dois mapas de mesa (o bloco mais importante da descoberta)

- **Objetivo:** entender **como a mesa é vendida hoje** e decidir o papel do mapa no MVP.
- **O que mostrar:**
  - **Mapa A — urbano ilustrado:** vista de cima estilizada do espaço real (rua, calçamento, casarões, palco, vegetação, mesas). Uso: apresentação pública, impacto, narrativa.
  - **Mapa B — planta operacional:** vista técnica com mesas numeradas, setores, capacidades, circulação, áreas técnicas, bloqueios, acessibilidade e **estados visuais** (Disponível / Pendente / Vendida / Cortesia / Bloqueada / Check-in). Uso: equipe e administração.
- **Mensagem principal:** "O mapa bonito é para o público se situar. O mapa técnico é a ferramenta de quem opera. Os dois compartilham os mesmos estados de mesa."
- **Fala sugerida:** "Enquanto a venda estiver na Sympla, o estado oficial de cada mesa — vendida, disponível — vem de lá. O nosso mapa reflete esse estado; ele não substitui a Sympla nessa primeira fase."
- **Perguntas (bloco de descoberta — reservar tempo):**
  - `PENDENTE` Como cada mesa é **comercializada** hoje? É um item único na Sympla, ou são ingressos por cadeira?
  - `PENDENTE` Existem **setores** (frente/fundo, coberto/descoberto, preços diferentes)?
  - `PENDENTE` A **capacidade** por mesa varia? Cadeiras extras?
  - `PENDENTE` Como são tratadas **cortesias** e mesas de **patrocinador**?
  - `PENDENTE` Existem mesas **bloqueadas** (não comercializáveis)? Quem decide?
  - `PENDENTE` Existe **planta oficial** do espaço, ou medidas? Foto de cima? O layout **muda por edição**?
  - `PENDENTE` Como é feito o **check-in** hoje na porta?
  - `PENDENTE` Como é o **atendimento de quem quer comprar mesa** (WhatsApp? telefone? pessoalmente)?
  - `PENDENTE` Como funciona **cancelamento / troca de mesa**?
- **Decisão esperada:** modelo real de venda de mesa documentado; decisão se o Mapa B é **operacional** (edição de estados na plataforma) ou apenas **espelho** da Sympla no MVP; se há planta oficial a obter.

### 6.5. Dashboard administrativo

- **Objetivo:** provar valor executivo — "abro e sei o que está acontecendo e o que precisa de atenção".
- **O que mostrar:** primeira dobra com próxima edição, ocupação (%), receita bruta/líquida, despesas, resultado, pedidos recentes, fila de atendimento, **falhas de integração**, tarefas, atividade recente. Evitar gráfico decorativo.
- **Mensagem principal:** "Não é um dashboard de enfeite. Cada bloco aqui ou mostra um número que importa ou aponta um problema para resolver."
- **Fala sugerida:** "A ideia é a diretoria abrir isso antes de uma reunião e já ter o retrato: quanto vendeu, quanto ocupou, o que falhou, o que está pendente."
- **Perguntas:**
  - `PENDENTE` Quais **números** a diretoria acompanha hoje, e onde (planilha? Sympla? não acompanha)?
  - `PENDENTE` Quem **usa** o dashboard — diretoria, produção, os dois?
  - `PENDENTE` "Resultado" (receita − despesa) pode ser visível para todos os perfis, ou é restrito?
- **Decisão esperada:** lista de 6–8 indicadores do MVP; quem enxerga valores financeiros.

### 6.6. CRM e atendimento

- **Objetivo:** mostrar como a plataforma para de perder contato e histórico.
- **O que mostrar:** pipeline em kanban (Novo → Atendimento → Interesse → Edição selecionada → Link enviado → Aguardando compra → Compra identificada → Pós-venda → Check-in → Relacionamento futuro); ficha 360º de um contato (papéis acumulados: comprador, participante, doador, patrocinador...); tela de atendimento omnichannel (fila, conversa, contato ao lado, resumo por IA, respostas rápidas, transferência para humano, notas internas).
- **Mensagem principal:** "A mesma pessoa que compra mesa este ano pode ser patrocinadora no ano que vem. A plataforma trata como **uma pessoa só**, com histórico."
- **Fala sugerida:** "Hoje, quando alguém pergunta no WhatsApp sobre a Bolerata, essa conversa provavelmente some. Aqui ela vira um contato no funil, com histórico, e a IA ajuda resumindo e sugerindo resposta — mas **quem responde é sempre uma pessoa** nas decisões que importam."
- **Perguntas:**
  - `PENDENTE` Quem **responde WhatsApp / Instagram** hoje? Quantas pessoas?
  - `PENDENTE` Onde ficam os **contatos** hoje (agenda do celular, planilha, Sympla)?
  - `PENDENTE` Quem pode **movimentar o CRM** / ver todos os contatos?
  - `PENDENTE` Vocês topam **IA sugerindo respostas** (com revisão humana)? Algum limite?
- **Decisão esperada:** canais do MVP (WhatsApp + Instagram + formulário confirmados); política de uso de IA no atendimento (`AI-002` do PRD apresentada).

### 6.7. Financeiro e projetos / patrocínios

- **Objetivo:** mostrar visão **gerencial** (não contábil) por centro de custo.
- **O que mostrar:** financeiro com centros de custo (Instituto, Bolerata, projetos, eventos, administração, patrocínios); contas a pagar/receber, anexos de comprovante, previsto x realizado; página de projeto com orçamento, patrocinadores, contrapartidas, entregas e prestação de contas.
- **Mensagem principal:** "Isso **não substitui a contabilidade**. É a visão de gestão: quanto a Bolerata custou, quanto sobrou, o que ainda falta pagar."
- **Fala sugerida:** "Cada despesa e cada receita fica amarrada a um evento ou projeto. No fim da Bolerata, vocês têm o resultado real dela sem montar planilha."
- **Perguntas:**
  - `PENDENTE` Como as **despesas são vinculadas** a evento/projeto hoje?
  - `PENDENTE` Existe **contador**? Ele terá **acesso** à plataforma (perfil só leitura de relatórios)?
  - `PENDENTE` Vocês emitem **NFS-e**? Qual município/sistema? (não vamos automatizar sem validar)
  - `PENDENTE` Existem **editais / convênios** com regras de prestação de contas específicas?
  - `PENDENTE` Como **patrocinadores** recebem relatório hoje?
- **Decisão esperada:** financeiro entra no MVP? Em que profundidade (só lançamento manual + centro de custo, ou também importação de extrato)?

---

## 7. Integrações — como explicar

Roteiro de fala para o bloco de integrações (52 min). **Enquadramento honesto, sem promessa.**

| Integração | Como apresentar | O que NÃO dizer |
|---|---|---|
| **Sympla** | "É e continua sendo a fonte oficial de venda e ingresso na primeira etapa. A plataforma **lê** os dados da Sympla — pedidos, participantes, valores, check-in — e organiza tudo no CRM, no dashboard e no financeiro." | Não afirmar que a Sympla deixa criar pedido, segurar mesa ou fazer checkout pelo nosso site. A documentação pública atual **não garante** isso. |
| **WhatsApp** | "O caminho **oficial** é a API do WhatsApp da Meta (Cloud API) — estável e dentro das regras. A plataforma é feita para trocar de provedor sem reescrever nada." | Não apresentar Evolution / megaAPI como o plano. São **alternativas** avaliadas, com aceite de risco (podem operar em modo não oficial, sujeito a bloqueio). |
| **Instagram** | "Mensagens do Instagram entram na mesma fila de atendimento, junto com o WhatsApp." | Não prometer recursos além de mensagens/DM sem confirmar conta profissional + Meta Business. |
| **E-mail** | "Notificações, confirmações e comunicação transacional. Provedor a definir." | — |
| **n8n** | "É o 'encanamento' que liga a plataforma aos serviços externos e roda tarefas agendadas (sincronizar Sympla, follow-up). Regras críticas de dinheiro e permissão **não** ficam nele." | — |
| **IA** | "Ajuda no atendimento — resume conversa, classifica, sugere resposta, cuida de FAQ. Nunca decide sozinha sobre desconto, reembolso, preço ou nota fiscal." | Não vender "IA autônoma". É assistente com humano no comando. |

**Perguntas do bloco:**
- `PENDENTE` Vocês já têm **conta Meta Business** e um **número de WhatsApp comercial** dedicado?
- `PENDENTE` A conta de **Instagram** é profissional/comercial e está ligada a uma página?
- `PENDENTE` Qual **e-mail** o Instituto usa para comunicação oficial? Domínio próprio?
- `PENDENTE` Existe **contrato Sympla** ativo, e quem tem acesso de produtor / token de API?

---

## 8. Perguntas de descoberta — consolidado

Todas as perguntas, agrupadas. Levar impressas / na Matriz de validação. Marcar estado antes (`CONFIRMADO`/`PROPOSTA`/`PENDENTE`), registrar feedback, decisão, responsável e prazo.

### 8.1. Institucional
1. Nome institucional exato a exibir.
2. Confirmar "Instituto Serrana Digital" como nome da plataforma.
3. Missão, visão e valores — redação oficial.
4. Diretoria atual (nomes, fotos, bios).
5. Quais áreas de atuação merecem destaque.
6. Quais projetos entram no lançamento.
7. Quem aprova conteúdo e qual o fluxo de aprovação.
8. Quais documentos podem ser públicos.
9. Quem administra o domínio `institutoserrana.org` e há interesse no `.org.br`.

### 8.2. Ferramentas atuais
10. Sympla — contrato, plano, token, responsáveis.
11. WhatsApp — número(s), Meta Business, API usada hoje.
12. Instagram / Facebook — contas, tipo, quem opera.
13. E-mail — provedor, domínio.
14. Planilhas — quais processos vivem em planilha hoje.
15. Financeiro — que sistema/planilha, quem opera.
16. Contabilidade — contador interno ou externo, o que ele precisa.
17. NFS-e — município, sistema, modelo fiscal.
18. Armazenamento de arquivos hoje (Drive, e-mail, papel).
19. Banco e conciliação — como é feito.

### 8.3. Bolerata / mesas
20–31. Bloco completo da seção 6.4 (comercialização, setores, capacidade, cortesias, patrocinadores, bloqueios, planta, mudança de layout, check-in, cancelamento, atendimento de interessados).

### 8.4. Administrativo / usuários
32. Quem usa o dashboard.
33. Quem vê o financeiro / valores.
34. Quem pode editar evento.
35. Quem responde WhatsApp / Instagram.
36. Quem movimenta o CRM.
37. Quem publica conteúdo.
38. Contador terá acesso (perfil leitura).
39. Existe fluxo de aprovação hoje.
40. Quais relatórios são obrigatórios.
41. Quais indicadores a diretoria acompanha hoje.

### 8.5. Projetos e prestação de contas
42. Tipos de projeto.
43. Editais / convênios envolvidos.
44. Documentos exigidos na prestação de contas.
45. Como despesas são vinculadas.
46. Como contrapartidas são controladas.
47. Como patrocinadores recebem relatórios.
48. Quais dados de projeto precisam ser públicos.

---

## 9. Decisões que devem sair da reunião

Meta: fechar o Discovery Gate D1 (`docs/product/02-roadmap-mvp.md` §4). Sai da reunião com:

| # | Decisão | Estado alvo |
|---|---|---|
| 1 | Nome e posicionamento da plataforma | `DECISÃO` |
| 2 | Conceito da Home Santa Rita (aprovado ou ajustes claros) | `DECISÃO` |
| 3 | Tratamento visual separado da Bolerata | `DECISÃO` |
| 4 | Escopo do MVP — o que entra e o que fica para depois | `DECISÃO` |
| 5 | Papel do mapa de mesa no MVP (operacional x espelho) | `DECISÃO` |
| 6 | Sympla como fonte de venda na 1ª etapa (confirmação do Instituto) | `DECISÃO` |
| 7 | Caminho oficial do WhatsApp = Meta Cloud API | `DECISÃO` |
| 8 | Canais de atendimento do MVP | `DECISÃO` |
| 9 | Financeiro no MVP — sim/não e profundidade | `DECISÃO` |
| 10 | Perfis de acesso (quem vê o quê) — versão inicial | `DECISÃO` |
| 11 | Responsável por conteúdo institucional | `DECISÃO` |
| 12 | Ponto de contato do Instituto para o projeto | `DECISÃO` |
| 13 | Decisão sobre domínio (`institutoserrana.org` x `.org.br`) | `DECISÃO` ou `PENDENTE` com dono |
| 14 | Data do próximo gate | `DECISÃO` |

Toda `PROPOSTA` que virar `DECISÃO` precisa: validação do responsável + data + atualização de `docs/discovery/02-decisions-assumptions.md` + ajuste do PRD se impactado (`02-decisions-assumptions.md` §5).

---

## 10. Documentos e acessos a solicitar

Entregar a lista por escrito ao final da reunião, com um responsável e um prazo.

**Documentos**
- [ ] Estatuto social atual
- [ ] CNPJ e cartão CNPJ
- [ ] Ata de eleição da diretoria atual
- [ ] Missão, visão e valores — texto oficial
- [ ] Relatórios de atividades / prestações de contas publicáveis
- [ ] Contrato ou plano da Sympla
- [ ] Planta / medidas do espaço da Bolerata (ou foto aérea)
- [ ] Identidade visual da Bolerata (logo, cores, fontes), se houver
- [ ] Fotos e vídeos: escadaria, Igreja de Santa Rita, edições anteriores da Bolerata
- [ ] Lista de projetos com descrição e status
- [ ] Modelo atual de controle financeiro (planilha exemplo, anonimizada)

**Acessos**
- [ ] Painel Sympla (perfil de produtor) e/ou token de API
- [ ] Conta Meta Business + WABA + número de WhatsApp
- [ ] Conta de Instagram (profissional) e página vinculada
- [ ] Acesso ao registro do domínio `institutoserrana.org`
- [ ] E-mail institucional para envio transacional
- [ ] Contato do contador (e o que ele precisa enxergar)

**Definições de pessoas**
- [ ] Ponto de contato principal do Instituto
- [ ] Aprovador de conteúdo
- [ ] Responsável pelo financeiro
- [ ] Responsável pela operação da Bolerata

---

## 11. Próximos passos (slide de fecho)

1. **Ata da reunião** com todas as decisões e pendências — enviada em até 2 dias úteis.
2. Atualização de `docs/product/01-prd.md` e `docs/discovery/02-decisions-assumptions.md` com o que virou decisão.
3. Refinamento do protótipo Penpot conforme feedback (Fase 1 do roadmap §5).
4. Recebimento dos documentos e acessos listados na seção 10.
5. Congelamento do escopo do MVP e priorização do backlog.
6. Agendamento do **próximo gate** (revisão do protótipo refinado + início da fundação técnica).

---

## 12. Versão curta — 15 minutos

| Min | Bloco | Foco |
|---|---|---|
| 0–2 | Abertura | A frase da visão + "isto é uma proposta, quero a reação de vocês". |
| 2–5 | Home Santa Rita | Scroll da home, do pé da escadaria à igreja. Pergunta: a narrativa está certa? |
| 5–9 | Bolerata + mapas | Página da edição → CTA Sympla → os dois mapas de mesa. Pergunta-chave: como a mesa é vendida hoje? |
| 9–12 | Admin em 1 tela | Dashboard: ocupação, receita, pendências, falhas. "Tudo num lugar, sem planilha." |
| 12–15 | Fecho | 3 perguntas obrigatórias (venda de mesa · quem responde WhatsApp · quem aprova conteúdo) + combinar acessos e próximo passo. |

**As 3 perguntas que não podem faltar na versão curta:**
1. Como cada mesa da Bolerata é vendida hoje (item único na Sympla ou por cadeira)?
2. Quem responde WhatsApp/Instagram hoje e onde ficam esses contatos?
3. Quem aprova o conteúdo institucional e quais documentos podem ser públicos?

---

## 13. Matriz da Apresentação

| Ordem | Tela / Slide | Objetivo | Mensagem | Demonstração | Pergunta ao Instituto | Decisão esperada |
|---|---|---|---|---|---|---|
| 1 | Capa + Visão | Enquadrar | "Um lugar digital só do Instituto: encanta por fora, organiza por dentro." | Slide | — | — |
| 2 | Dois ambientes | Explicar arquitetura de uso | "Site de quem visita ≠ sistema de quem trabalha." | Diagrama 2 caixas | Faz sentido separar? | Confirmar 2 ambientes |
| 3 | Home Santa Rita | Encantar / narrativa | "A home é uma subida da escadaria até a igreja." | Scroll completo + versão reduced-motion | Sequência certa? Têm mídia? Restrição de imagem da igreja? | Conceito aprovado; dono da mídia |
| 4 | Instituto / Transparência | Conteúdo e credibilidade | "Estrutura nossa, conteúdo de vocês, editável." | Página Instituto + Transparência + CMS | Missão oficial? Diretoria? Documentos públicos? Quem aprova? | Responsável por conteúdo; docs públicos |
| 5 | Projetos e Eventos | Base reaproveitável | "Serve para a Bolerata e para tudo que vier depois." | Lista + página de projeto + agenda | Quais projetos no lançamento? | 2–3 projetos do MVP |
| 6 | Bolerata — página/temporada | Identidade do evento | "Cara de evento, dentro do mesmo site." | Hero + grade da temporada | Bolerata tem identidade visual? Quantas edições? | Tema separado aprovado |
| 7 | Bolerata — edição + Sympla | Jornada de compra | "Reserva pela Sympla; a plataforma organiza o resto." | Página da edição → CTA → fluxo Sympla | Venda é 100% Sympla? Contrato? Quem administra? | Sympla = fonte de venda 1ª etapa |
| 8 | Mapa A — ilustrado | Situar o público | "Mapa bonito para o visitante se localizar." | Mapa urbano estilizado | Layout muda por edição? | Papel do Mapa A no MVP |
| 9 | Mapa B — operacional | Ferramenta da equipe | "Mapa técnico com estados de mesa; respeita a Sympla." | Planta numerada + estados + painel lateral | Bloco completo de venda de mesa (setores, cortesias, bloqueios, planta, check-in) | Modelo real de venda; Mapa B operacional x espelho |
| 10 | Dashboard | Valor executivo | "Abro e sei o que acontece e o que precisa de atenção." | Primeira dobra do dashboard | Que números a diretoria vê hoje? Quem vê o quê? | 6–8 indicadores; acesso a valores |
| 11 | CRM + Atendimento | Não perder contato | "Uma pessoa só, com histórico, em todos os canais." | Pipeline + ficha 360º + atendimento omnichannel + resumo IA | Quem responde hoje? Onde ficam os contatos? IA sugerindo resposta, ok? | Canais do MVP; política de IA |
| 12 | Financeiro + Projetos | Visão gerencial | "Não substitui contabilidade; mostra o resultado real por evento/projeto." | Financeiro por centro de custo + prestação de contas | Como vinculam despesa hoje? Tem contador? NFS-e? | Financeiro no MVP? Profundidade |
| 13 | Integrações | Enquadrar sem prometer | "Sympla lê; WhatsApp oficial Meta; IA assiste, humano decide." | Diagrama plataforma ↔ n8n ↔ serviços | Têm Meta Business e número? Token Sympla? | WhatsApp = Meta Cloud API |
| 14 | Descoberta guiada | Fechar pendências | "Agora que vocês viram tudo, as perguntas que faltam." | Lista de perguntas em aberto | Todas as `PENDENTE` restantes | Máximo de `PENDENTE` → `DECISÃO` |
| 15 | Próximos passos | Combinar o gate | "Ata, refinamento, acessos, próximo encontro." | Slide de próximos passos + lista de acessos | Quem é o ponto de contato? | Responsável, prazos, data do gate |

---

## 14. Alterações necessárias no protótipo antes da reunião

Classificação: **P0** obrigatório · **P1** importante · **P2** opcional.

### P0 — obrigatório (sem isto a reunião não roda bem)

- [ ] **Home Santa Rita navegável em modo apresentação** — os 6 estados do storyboard (`docs/design/01-penpot-brief.md` §9), com transições, e a **variante `reduced-motion`** (imagem estática + texto).
- [ ] **Página de edição da Bolerata** com CTA "Reservar / Comprar" levando visualmente ao "fluxo oficial Sympla" (tela-conceito, sem integração real).
- [ ] **Mapa A (ilustrado)** e **Mapa B (operacional)** — pelo menos um layout de exemplo cada, com os 6 estados de mesa visíveis no Mapa B e o painel lateral de detalhe da mesa.
- [ ] **Dashboard administrativo** — primeira dobra com os blocos de `DASH-001` (próxima edição, ocupação, receita bruta/líquida, despesas, resultado, pedidos, atendimento, falhas de integração, tarefas, atividade).
- [ ] **CRM** — board kanban com as etapas de `CRM-001` + **ficha 360º** de um contato de exemplo (`CRM-003`).
- [ ] **Tela de atendimento omnichannel** — fila + conversa + contato ao lado + bloco "resumo por IA" (`MSG-002`).
- [ ] **Todos os textos institucionais marcados como rascunho** no protótipo (marca-d'água / etiqueta "PROPOSTA DE REDAÇÃO") para não serem lidos como oficiais.
- [ ] **Design System aplicado de forma consistente** nos dois temas (institucional e Bolerata) — paletas de `01-penpot-brief.md` §4 e §5, tipografia §6.

### P1 — importante (melhora muito, mas dá para contornar)

- [ ] Página "O Instituto" e página "Transparência" com conteúdo de exemplo realista.
- [ ] Grade da **temporada** da Bolerata com 3–4 edições e estados (aberta / esgotada / encerrada).
- [ ] Tela de **Eventos** (admin) — lista + página de um evento com programação/equipe/custos.
- [ ] **Financeiro** — visão por centro de custo com previsto x realizado (dados de exemplo).
- [ ] **Mobile** das telas-chave: Home Santa Rita simplificada, página da Bolerata, dashboard, atendimento, mapa.
- [ ] Página de **projeto** com orçamento, patrocinadores e prestação de contas.
- [ ] **Login** administrativo (tela simples, com menção a MFA para perfis sensíveis).

### P2 — opcional (se sobrar tempo)

- [ ] Galeria da Bolerata por edição.
- [ ] Tela de **Relatórios** (lista dos relatórios de `RPT-001`).
- [ ] **Pessoas / RH** — lista de equipe/prestadores vinculada a contatos.
- [ ] **Documentos** com vínculo a projeto/evento/financeiro.
- [ ] Página de **Patrocínio** (pública) com níveis de cota.
- [ ] Animação de detalhe no hero (partículas de luz subindo a escadaria) — só se não atrasar o P0.

---

## 15. Riscos de condução da reunião

| Risco | Mitigação |
|---|---|
| Instituto tratar o protótipo como "sistema pronto" | Repetir na abertura e a cada bloco: "isto é proposta / rascunho". Etiquetas no protótipo. |
| Conversa travar em detalhe visual (cor, fonte) cedo demais | "Anotado — a identidade a gente lapida depois; hoje quero validar fluxo e escopo." |
| Bloco de mesas consumir a reunião inteira | Time-box de 7 min + registrar o resto por escrito para follow-up. |
| Prometer capacidade da Sympla sem confirmação | Roteiro da seção 7. Se perguntarem "dá para vender pelo site?": "Depende do que o contrato de vocês com a Sympla libera — está na nossa lista de perguntas." |
| Sair sem responsável definido | Último slide não fecha até ter um nome para "ponto de contato" e um prazo para os acessos. |
| Decisões ditas e não registradas | Uma pessoa dedicada à Matriz de validação durante toda a reunião. |
