# Prysma App — TODO

## Sprint 1: Fundações ✓

- [x] Schema do banco de dados: users, chat_sessions, chat_messages, weekly_credits, protocol_history, user_integrations
- [x] Migração SQL aplicada via webdev_execute_sql
- [x] Identidade visual espacial escura: CSS variables OKLCH, paleta, tipografia (Space Grotesk)
- [x] Configuração PWA: manifest.json, meta tags, ícones, tema escuro
- [x] Router tRPC: integrations (connectNotion, connectGoogle, getStatus, disconnect)
- [x] Router tRPC: créditos semanais (getWeekly, consume) — Cristais de Energia
- [x] Router tRPC: sessões de chat (create, list, archive, getMessages, addMessage)
- [x] Router tRPC: histórico de protocolos (history)
- [x] Layout PrysmaLayout com sidebar espacial e navegação mobile bottom bar
- [x] Tela de login com identidade Prysma (nebula-bg, logo prisma SVG)
- [x] Página Home / Sala de Comandos (ações rápidas, status integrações, sessões ativas)
- [x] Página Chat (lista de sessões, área de mensagens, arquivamento)
- [x] Página Biblioteca (12 protocolos, filtros por categoria, modal de detalhes)
- [x] Página Perfil (integrações Notion/Google, plano, Cristais de Energia)
- [x] Componente CrystalEnergy (indicador Sonnet vs Haiku, barra de progresso, tooltip compacto)
- [x] Testes Vitest: auth, integrations, credits, sessions, protocols (9 testes passando)
- [x] Checkpoint do Sprint 1

## Sprint 2: Motor de IA + Integrações

### Correções Acopladas do Sprint 1
- [ ] Login: trocar "}_ bem-vindo, navegador" por "}_ olá, comandante"
- [ ] Login: frase de suporte no padrão prysma_ (sem "bem-vindo")
- [ ] Home: ícone órbita semanal — trocar por planeta na identidade dos outros ícones
- [ ] Home: nota estelar no padrão prysma_ (sem linguagem formal)
- [ ] Padrão geral: sempre "olá" em vez de "bem-vindo/bem-vinda"

### Motor de IA (Sprint 2)

- [x] Tabela carta_de_navegacao criada no banco (identidade, missão, visão, TUD, projetos, energia)
- [x] Router tRPC carta: get e upsert
- [x] Router tRPC ai: chat com buildSystemPrompt por protocolo
- [x] System prompt do Kernel V7.2 injetado para todos os protocolos
- [x] System prompt especial para Carta de Navegação (11 turnos, ping-pong, fases A/B/C)
- [x] System prompt especial para Órbita Semanal
- [x] Roteamento Sonnet/Haiku por protocolo na interface de chat
- [x] Toggle de modelo (tática/profunda) no header do chat
- [x] Extração automática de dados da Carta de Navegação via JSON na resposta
- [x] Widgets da Sala de Comandos: Tríade, TUD, Ciclos
- [x] Banner de carta pendente quando onboarding não foi completado
- [x] Renderização de Markdown nas respostas do Navegador (Streamdown)
- [x] Auto-scroll para última mensagem
- [x] Textarea com auto-resize
- [x] Indicador de loading (dots animados) durante resposta da IA
- [ ] Lógica de consumo de créditos ao enviar mensagem para a IA
- [ ] Tool Calling: leitura/escrita no Notion (criar Nave, criar Missão, atualizar template)
- [ ] Tool Calling: leitura/escrita no Google Calendar (ler agenda, criar eventos)
- [ ] OAuth Notion: fluxo completo com provisionamento automático do template
- [ ] OAuth Google Calendar: fluxo completo com leitura de eventos

## Sprint 3: Integrações e Dashboard (futuro)

- [ ] Sala de Comandos com dados reais do Notion (TUD, Tríade, projetos ativos)
- [ ] Órbita Semanal com dados reais do Google Calendar
- [ ] Onboarding conversacional (Eclusa de Ar — 11 loops da Carta de Navegação)
- [ ] 2º Cérebro: captura rápida com triagem automática no Notion

## Sprint 4: UX, Polimento e Lançamento Alfa (futuro)

- [ ] Refinamento visual completo
- [ ] Ícones PWA para iOS e Android
- [ ] Testes de usabilidade com primeiros Founders
- [ ] Integração com plataforma de pagamento (Hotmart/Kiwify)
- [ ] Lançamento Alfa

## Feedbacks Sprint 1 — Ajustes Visuais e Linguagem Prysma

- [x] Aplicar linguagem prysma_ em toda a interface (minúsculas, pontuações-código: ::, }_, {}, >>)
- [x] Home: trocar saudação por "}_ bom dia/tarde/noite, comandante 🖖🏼" com hora dinâmica
- [x] Home: data no formato "sala de comandos :: quinta-feira } 19 de março"
- [x] Home: renomear botões de ação com linguagem prysma_ (:: nova sessão, :: biblioteca, :: órbita semanal, :: integrações)
- [x] Home: ícone de órbita semanal (sol + planetas orbitando)
- [x] Home: seção de conexões ativas com label "}_ conexões ativas ::"
- [x] Home: renomear seção para "}_ últimas sessões"
- [x] Home: nota estelar do Prysma com CTA para configurar integrações (quando não conectado)
- [x] Home: navegação inferior com ícones corretos (OVNI=início, balão=navegador, livro=comandos, alienígena=perfil)
- [x] Biblioteca: categorias do Notion (início, rota, ação, revisão) com cores e ícones corretos
- [x] Biblioteca: categorizar protocolos pelas 4 categorias do Notion
- [x] Biblioteca: ocultar número do protocolo do Kernel
- [x] Biblioteca: remover protocolo "Atualizar Template" (descontinuado)
- [x] Biblioteca: usar títulos e descrições exatos do template Notion
- [x] Biblioteca: ocultar completamente o tipo de LLM usado
- [x] Indicador de créditos: renomear Sonnet → "energia profunda" e Haiku → "energia tática"

## Ajustes de Identidade

- [x] Renomear "Prysma" para "prysma_" em toda a interface visível (sidebar, login, título, manifest)

## Ajustes Finais UI — Pré-Sprint 2

- [ ] Home header: "}_ saudação, comandante 🖖🏼 / sala de comandos :: / ⮑ nome do usuário / data em itálico menor"
- [ ] Ícone órbita semanal: trocar por planeta Júpiter (mesmo traço dos outros ícones)
- [ ] Ícone início (nav): trocar OVNI por Sol
- [ ] Ícone perfil (nav): voltar para ícone padrão (User/UserCircle)
- [ ] Botões com colchetes [ ]: substituir por :: ou }_
- [ ] CrystalEnergy: trocar estrela esticada por ícone harmônico (Sparkles ou Star proporcional)
- [ ] Página Chat: aplicar padrão prysma_ (minúsculas, marcadores :: e }_)
- [ ] Página Perfil: aplicar padrão prysma_ em todos os textos
- [ ] Botão upgrade: inverter (fundo roxo, texto escuro) para mais destaque

## Ajustes Visuais — Pós Sprint 2

- [x] Home: ícone "orbita semanal" — aumentar para mesma proporção visual dos outros ícones de widget

## Sprint A — Ajustes de Interface e Linguagem (aprovado)

- [x] A1: Chat + Cristais de Energia: "tática" → modo foco / "profunda" → modo expansão
- [x] A2: Header: }_ boa tarde, comandante **tinno** 🖖🏼 (primeiro nome em negrito, sem seta ↳)
- [x] A3: Data com ano: quinta-feira } 19 de março de 2026
- [x] A4: Sidebar: "Essencial" → ":: essencial"
- [x] A5: Botão "atualizar ⫪" da Carta de Navegação vira botão visual real
- [x] A6: Widget Tríade: label "identidade" → "bússola ::"
- [x] A7: Widget TUD: label "prioridades" → "tud :: tempo útil disponível"
- [x] A8: Remover bloco "cristais da semana" (sonnet/haiku) do widget Ciclos
- [x] A9: Cristais de Energia: data de renovação no formato ":: energia renova domingo } dd/mm/aa às hh:mm"
- [x] A10: Títulos "conexões ativas" e "últimas sessões" com cor de destaque diferente
- [x] A11: Mais espaço entre blocos na Sala de Comandos

## Sprint B — Widgets com Dados Reais do Notion (aprovado)

- [x] B1: Router notion.getTUD — lê ÂNCORA GLOBAL (TUD) via MCP e retorna campos de horas/slots
- [x] B2: Router notion.getProjetosTriade — filtra BASE DE PROJETOS por "tríade central" + ativo
- [x] B3: Router notion.getProjetosCiclos — filtra BASE DE PROJETOS por "sustentação" + ativo
- [x] B4: Widget TUD na Home: dados reais da ÂNCORA GLOBAL com barras de progresso (Tríade + Ciclos)
- [x] B5: Widget Bússola: mantém dados da carta_de_navegacao (sem mudança)
- [x] B6: Linhas alternantes (ocultar/expandir): Tríade Central e Ciclos de Sustentação com projetos reais
- [x] B7: Foto de perfil com upload S3 e crop 1:1 na página de Perfil

## Sprint C — Sidebar Gamificado + Plano de Voo (aprovado)

- [x] C1: Schema: tabela user_progress (fase atual, subfases concluídas, prysmas acumulados)
- [x] C2: Router trpc.progress.get — retorna fase atual e prysmas do usuário
- [x] C3: Router trpc.progress.unlock — desbloqueia próxima fase/subfase e concede 3 prysmas
- [x] C4: Sidebar reestruturado com hierarquia: início / :: chat / --- / :: implementação / --- / :: biblioteca
- [x] C5: Sidebar: botões travados com ícone de cadeado e tooltip explicativo
- [x] C6: Sidebar: barra de progresso da implementação (% de fases concluídas)
- [x] C7: Header superior direito: contador de Prysmas acumulados (✦ N prysmas)
- [x] C8: Página Plano de Voo com 5 fases em cards (liberada por padrão)
- [x] C9: Lógica de desbloqueio sequencial: cada fase libera a próxima ao ser concluída
- [x] C10: +3 Prysmas ao desbloquear cada fase/subfase (animação de conquista)

## Sprint D — 2º Cérebro + Consultoria + Páginas Restantes (aprovado)

- [x] D1: Schema: tabela brain_notes (userId, content, type: note/checklist/bullet, createdAt)
- [x] D2: Router trpc.brain.list, brain.create, brain.update, brain.delete
- [x] D3: Botão flutuante rosa (ícone cérebro) visível em todas as páginas via PrysmaLayout
- [x] D4: Drawer/modal do 2º Cérebro: lista de notas com editor inline (texto, checklist, marcador)
- [x] D5: Botão "direcionar ao Navegador" — envia notas para o chat com protocolo segundo_cerebro
- [x] D6: Popup de Consultoria Humana com descrição e link WhatsApp (wa.me)
- [x] D7: Rota /consultoria com página dedicada de Consultoria Humana
- [x] D8: Página stub Missões da Semana (/missoes) — travada, com CTA para concluir Plano de Voo
- [x] D9: Página stub Check-in Semanal (/checkin) — travada, com CTA para concluir Missões
- [x] D10: Página stub Revisão Trimestral (/revisao) — travada, com CTA para concluir Check-in

## Sprint F — Ajustes UX Sala de Comandos

- [x] F1: Mobile: contador de Prysmas alinhado harmonicamente com contador de energia no topo
- [x] F2: Substituir ⭐ por ícone Battery (pilha) no contador de energia
- [x] F3: Mobile: botão hambúrguer (3 linhas) no canto superior esquerdo abre/fecha sidebar
- [x] F4: Header: nome do usuário na mesma linha da saudação (}_ boa noite, comandante **tinno** 🖖🏼)
- [x] F5: Widget "órbita semanal" → "notificação de check-in" com on/off, popup dia+horário, push notification, travada até check-in desbloqueado
- [x] F6: Widget "biblioteca" travada até página Comandos ser desbloqueada
- [x] F7: Nova ordem das widgets: nova sessão → integrações → notificação check-in → biblioteca
- [x] F8: Carta de Navegação: botão "visualizar" abre página /carta com carta formatada + botão editar (só editável após desbloquear biblioteca)
- [x] F9: Logo Prysma no sidebar (desktop) vira link clicável para /
- [x] F10: Remover barras de porcentagem da barra lateral — deixar só contador de Prysmas
- [x] F11: 2º Cérebro: emoji 🧠 maior, tooltip "2º cérebro", popup centralizado e maior, editor livre tipo bloco de notas
- [x] F12: Tooltip no contador de Prysmas: "você já acumulou X prysmas"
- [x] F13: Service worker para push notification + cron de verificação de check-in agendado

## Sprint G — Plano Final (aprovado)

### G01-G05: Correções de UX
- [x] G01: Tooltip "você já acumulou X prysmas" aparece abaixo do ícone, sem cortar
- [x] G02: Devolver barra de evolução da implementação no sidebar (desafixada, scroll junto)
- [x] G03: Mobile: botão X para fechar sidebar não sobrepõe o contador de Prysmas
- [x] G04: Chat: barra de envio de mensagem com texto verticalmente centralizado
- [x] G05: Mobile: logo prysma_ aparece no header do sidebar

### G06-G10: Plano de Voo Redesenhado
- [x] G06: Botões de fase em cards rosa preenchidos (não inline)
- [x] G07: Fases concluídas permanecem abertas para revisão (vídeos acessíveis)
- [x] G08: Subfases internas dentro de cada fase (vídeo + conteúdo + botão concluído)
- [x] G09: Cada subfase concluída = +1 Prysma (além dos +3 ao concluir a fase)
- [x] G10: Barra alternante (ocultar/expandir) para conteúdo complementar por subfase

### G11-G18: Painel Admin /admin
- [x] G11: Rota /admin protegida por role admin
- [x] G12: Editar título e descrição de cada fase
- [x] G13: Escolher ícone da fase (paleta de ~20 ícones Lucide)
- [x] G14: Anexar vídeo por subfase (URL YouTube/Vimeo com embed automático)
- [x] G15: Anexar comandos sugeridos por subfase (botões que pré-preenchem o chat)
- [x] G16: Editor TipTap por subfase (negrito, itálico, H1/H2/H3, linha separadora)
- [x] G17: Adicionar ou remover fases e subfases livremente
- [x] G18: Botão "concluído" por subfase e por fase com confirmação

### G19: 2º Cérebro com TipTap
- [x] G19: Integrar TipTap no editor do 2º Cérebro (BrainFloating)

## Ajuste Final

- [x] Sidebar: atalho "dúvidas" abaixo de Sala de Comandos com botão "como começar no prysma" → abre chat com protocolo de onboarding

## PWA — Instalação como App

- [x] Gerar ícones PWA em todos os tamanhos (72, 96, 128, 144, 152, 180, 192, 512)
- [x] Atualizar manifest.json com lista completa de ícones (any + maskable)
- [x] Atualizar apple-touch-icon.png e favicon.png com logo oficial
- [x] Verificar que todos os arquivos estão acessíveis via servidor (200 OK)

## Sprint H — Correções e Melhorias

- [x] H1: Apple-touch-icon corrigido definitivamente (PNG correto servido no domínio publicado)
- [x] H2: 2º Cérebro como página completa (/cerebro) em vez de popup
- [x] H3: 2º Cérebro: opção de checklist na barra de edição
- [x] H4: Admin Plano de Voo: campo de link de vídeo por subfase
- [x] H5: Admin Plano de Voo: acesso admin funcionando corretamente
- [x] H6: Admin Plano de Voo: editar texto e tipo dos botões (comando ou link externo)
- [x] H7: Admin Plano de Voo: bloco de conteúdo complementar com título expansível para o usuário
- [x] H8: Admin Plano de Voo: ampliar para 20+ ícones disponíveis por fase
- [x] H9: Admin Plano de Voo: campo para personalizar o título do botão rosa da fase

## Sprint I — Tema e 2º Cérebro

- [x] I1: Botão premium no Perfil alterado para "em breve ::"
- [x] I2: 2º Cérebro como página inteira real (rota /cerebro, fundo 100% preto, sem popup)
- [x] I3: Toggle de tema claro/escuro no Perfil

## Sprint J — 2º Cérebro UX

- [x] J1: Editor do 2º Cérebro full width (experiência Evernote/bloco de notas)
- [x] J2: Botão "salvar nota" sem quebra de linha no mobile
- [x] J3: Botão flutuante 🧠 como toggle entrada/saída do 2º Cérebro

## Sprint K — Correções

- [x] K1: Restaurar subtítulo "}_ tire da cabeça agora." no 2º Cérebro
- [x] K2: Corrigir duplicidade do header mobile no PrysmaLayout

## Sprint L — Tema Claro

- [x] L1: Corrigir tema claro para alterar fundo de todo o app (não apenas textos)

## Sprint M — Tema Claro Refinado

- [x] M1: Fundo branco (#ffffff) nas páginas, sidebar (#f8f8f7) no tema claro
- [x] M2: Bloco de prysmas acumuladas com mesmo padrão visual dos cristais de energia
- [x] M3: Blocos (nova sessão, biblioteca, bússola, TUD, etc.) com cor harmônica no tema claro
- [x] M4: Textos dos botões "como está fluindo..." sem quebra de linha no mobile
- [x] M5: Padrão do tema claro aplicado no Plano de Voo e demais páginas

## Sprint N — Tema Claro Definitivo (sem degradê)
- [x] N1: CSS: fundo branco puro #ffffff, sidebar #f8f8f7, bloco prysmas #ecedf0 — tudo chapado, zero degrêadê
- - [x] N2: Sala de Comandos — blocos sem degrê, cor chapada harmônica com ícone- [x] N3: Plano de Voo — padrão claro sem degrêadê- [x] N4: Navegador (prysma.ia) — padrão claro sem degrêadê
- [x] N5: Missões — padrão claro sem degrêdê
- [x] N6: Check-in — padrão claro sem degrêdê
- [x] N7: Revisão — padrão claro sem degrêdê
- [x] N8: Biblioteca — padrão claro sem degrêdê- [x] N9: Demais páginas (Perfil, 2º Cérebro, Admin, etc.) — padrão claro sem degrêadê
- [x] N10: Textos "como está fluindo sua tríade" e "ciclos" sem quebra no mobile
- [x] N11: Botão dúvidas — remover "como começar no prysma" e redirecionar para comando //como começar no prysma

## Sprint O — Tema Claro: Harmonia de Cores

- [x] O1: Adicionar overrides de prysma-faint, sonnet-faint, haiku-faint, prysma-dim no :root:not(.dark) para harmonia no tema claro

## Sprint P — Tema Claro: Correção Definitiva

- [ ] P1: Sobrescrever --color-prysma-faint/dim/sonnet/haiku no :root:not(.dark) com sintaxe correta do Tailwind 4
- [ ] P2: Corrigir bloco de prysmas acumuladas (escuro no modo claro)
- [ ] P3: Corrigir botão selecionado do sidebar (escuro no modo claro)
- [x] P4: Corrigir categorias da biblioteca (escuras no modo claro)

## Sprint Q — Tema Claro: Últimos ajustes

- [x] Q1: Home.tsx — item de sessão migrado de bg-space-mid/40 para bg-muted/50 (semântico, responde ao tema)
- [x] Q2: Biblioteca.tsx — CATEGORY_CONFIG migrado de oklch hardcoded para variáveis semânticas (prysma-faint, haiku-faint, sonnet-faint, muted)
- [x] Q3: Biblioteca.tsx — ProtocolCard migrado de bg-space-dark/60 para bg-card (semântico)
- [x] Q4: Biblioteca.tsx — DialogContent migrado de bg-space-dark para bg-popover (semântico)
- [x] Q5: Biblioteca.tsx — blocos de detalhe do protocolo migrados de oklch hardcoded para variáveis semânticas

## Sprint R — Fundo exato #f6f6f7 nas widgets

- [x] R1: Criada variável CSS --card-widget (#f6f6f7 no claro, oklch(0.13) no escuro) com token Tailwind bg-card-widget
- [x] R2: StatusCard (Home) usa bg-card-widget
- [x] R3: ProtocolCard (Biblioteca) usa bg-card-widget

## Sprint S — Admin no Plano de Voo

- [x] S1: Owner (Tinno Zani) já está com role=admin no banco (confirmado via SQL)
- [x] S2: Botão ":: modo edição" no Plano de Voo (visível só para admin) que alterna entre view usuário e painel admin inline com links rápidos por fase

## Sprint T — Admin + Gerenciamento de Dados LGPD

- [x] T1: Botão "voltar ao plano de vôo" no Admin.tsx
- [x] T2: Procedures backend: clearChats, resetPrysmas, clearAllData, deleteAccount (dataRouter)
- [x] T3: Seção "gerenciamento de dados" no Perfil com 3 operações + AlertDialog de double check
- [x] T4: Link "excluir conta prysma" discreto no Perfil com double check LGPD

## Sprint U — Fix contador prysmas + reiniciar prysma

- [x] U1: Corrigir resetPrysmas/clearAll — zerar userProgress.prysmasEarned+completedPhases+currentPhase E invalidar progress.get+flight.getProgress
- [x] U2: Renomear "limpar todos os dados prysma" para "reiniciar prysma" com novo texto de double check completo
- [x] U3: Travas do Plano de Voo vêm de userPhaseProgress (deletado pelo reset) — confirmado operante
- [x] U4: clearAllUserData agora reseta onboarding, carta, prysmas, progresso e fases — estado de novo usuário garantido

## Sprint V — Reordenação de travas + revisão trimestral temporal

- [x] V1: Reordenar PHASE_UNLOCK_ORDER: plano_voo → missoes_semana → checkin_semanal → comandos → revisao_trimestral
- [x] V2: Trava temporal de 3 meses para revisão trimestral (baseada em user.createdAt)
- [x] V3: Data prevista de desbloqueio visível abaixo do botão revisão trimestral na sidebar
- [x] V4: Toast ao click no botão revisão trimestral com mensagem e data prevista
- [x] V5: ProtocolCard revisão trimestral travado na Biblioteca com title, opacidade, data prevista e toast ao click

## Sprint W — Fix desbloqueio de fases

- [x] W1: Diagnosticado: dois sistemas paralelos (userPhaseProgress vs userProgress.completedPhases) nunca conectados
- [x] W2: handleCompletePhase agora chama progress.unlock após flight.complete, mapeando índice da fase para slug da sidebar
- [x] W3: Toast de desbloqueio com 800ms de delay após conclusão de fase ("missões da semana desbloqueadas! ✨")

## Sprint X — UX Plano de Voo + Popup de Desbloqueio

- [x] X1: Contador de prysmas na header sempre visível (mesmo com 0 prysmas) — tooltip adaptativo
- [x] X2: Botões de fase no Plano de Voo em lista vertical (flex-col, w-full) com ícone e título da fase
- [x] X3: Componente UnlockPopup criado com logo Prysma, }_ parabéns!, e item desbloqueado
- [x] X4: IMPLEMENTATION_PHASES corrigido (comandos fase 4, revisao_trimestral fase 5) — mensagens aleatórias eliminadas

## Sprint Y — Gatilhos precisos de desbloqueio + UX Plano de Voo

- [x] Y1: Sidebar — nova ordem: plano_voo → missoes_semana → checkin_semanal → revisao_trimestral (implementação) → comandos (biblioteca)
- [x] Y2: Gatilho missoes_semana: 100% das fases concluídas (willBeComplete >= totalPhases)
- [x] Y3: Gatilho checkin_semanal: primeiro envio com protocolId=missoes_semana no chat
- [x] Y4: Gatilho comandos: primeiro envio com protocolId=checkin_semanal no chat
- [x] Y5: Popup revisão trimestral: só aparece após 3 meses (trava temporal mantida)
- [x] Y6: Plano de Voo — PhaseDetail movido para dentro do loop, expande logo abaixo do botão clicado
- [x] Y7: Contador de prysmas no mobile header também sempre visível (removida condição prysmasTotal > 0)

## Sprint Z — Fix prysmas + popup chat + UX comandos

- [x] Z1: Corrigido cálculo de prysmas — unlockNextPhase usa sql`prysmasTotal + 3` (incremento, não sobrescreve)
- [x] Z2: completeSubphase também atualiza prysmasEarned no userProgress
- [x] Z3: Removido emoji ❎ do toast de fase concluída no PlanoDeVoo.tsx
- [x] Z4: MissoesDaSemana.tsx passa cmd=escolher+missoes+da+semana na URL do chat
- [x] Z5: CheckinSemanal.tsx passa cmd=iniciar+checkin+da+semana na URL do chat
- [x] Z6: routers.ts retorna unlockedPhaseId (nextPhaseId) no response do chat
- [x] Z7: Chat.tsx exibe UnlockPopup quando unlockedPhaseId retorna (com 800ms de delay)
