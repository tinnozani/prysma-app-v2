# Notion Schema — Referência Sprint B

## Página: 1 :: sala de comandos
URL: https://www.notion.so/586c66f140dd8221b6f901b5393f2eed

### Estrutura da página (2 colunas):
- Coluna 1: ÂNCORA GLOBAL (TUD) — gallery view
- Coluna 2:
  - `}_ como está fluindo sua tríade central ::` → BASE DE PROJETOS (view 1)
  - `}_ como estão fluindo seus ciclos de sustentação ::` → BASE DE PROJETOS (view 2, em details/toggle)

---

## Base: ÂNCORA GLOBAL (TUD)
- collection ID: `024c66f1-40dd-8262-823f-072203f633e0`
- Campos principais:
  - `Âncora` (title) — nome da âncora
  - `TUD Total (h)` (formula) — total de horas TUD
  - `[UI] Resumo TUD` (formula) — resumo formatado para UI
  - `Soma Tríade (semana)` (rollup) — horas tríade na semana
  - `Soma Ciclos (semana)` (rollup) — horas ciclos na semana
  - `Max Tríade (semana)` (rollup) — máximo tríade
  - `Max Ciclos (semana)` (rollup) — máximo ciclos
  - `Qtd Tríade Ativa (num)` (formula) — quantidade projetos tríade ativos
  - `Qtd Ciclos Ativos (num)` (formula) — quantidade projetos ciclos ativos
  - `Horas TP Semanais` (rollup) — horas trabalho pessoal semanais
  - `Soma Diárias Vital` (rollup) — soma diárias vitais

---

## Base: BASE DE PROJETOS
- collection ID: `7c5c66f1-40dd-82f4-8e1e-87aecb2d6202`
- Campos principais:
  - `Projetos` (title) — nome do projeto
  - `Órbita` (select) — valores: "Núcleo Vital", "Tríade | Concepção", "Tríade | Tração", "Tríade | Cadência", "Sustentação", "Constelação de Ideias"
  - `Status` (select) — valores: "✨ hibernação", "🌕 ativo", "🔜 em breve", "💭 pausado", "✅ concluído"
  - `Painel • Categoria` (select) — valores: "tríade central", "sustentação", "tud disponível"
  - `Progresso %` (formula) — percentual de progresso
  - `TUD | %` (formula) — % do TUD alocado
  - `TUD | Horas` (formula) — horas TUD alocadas
  - `Horizonte` (text) — indicador principal do projeto
  - `Sinastria Criativa` (select) — "☌ Conjunção", "🔺 Trígono", "✨ Sextil", "⚔️ Quadratura", "☍ Oposição"
  - `Raios` (select) — raio 1 a 5
  - `Horas Semanais (round)` (formula) — horas semanais arredondadas

### Filtros para as linhas alternantes:
- **Tríade Central**: `Painel • Categoria = "tríade central"` AND `Status = "🌕 ativo"`
- **Ciclos de Sustentação**: `Painel • Categoria = "sustentação"` AND `Status = "🌕 ativo"`

---

## IDs das bases para queries via tRPC:
- ÂNCORA GLOBAL (TUD): `collection://024c66f1-40dd-8262-823f-072203f633e0`
- BASE DE PROJETOS: `collection://7c5c66f1-40dd-82f4-8e1e-87aecb2d6202`
