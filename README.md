# MAAB — Operations Manager Dashboard

Dashboard interno de gestão operacional da **MAAB Consulting**, desenvolvido como aplicação web single-file (HTML + CSS + JS). Agrega em tempo real o estado de todos os projetos de internacionalização, a equipa de Account Managers, alertas, calendário semanal e métricas de performance.

---

## Funcionalidades

### Overview
Visão geral consolidada da operação — métricas de topo (projetos ativos, reuniões, contratos, revenue), alertas prioritários e checklist de tarefas da gestão.

### Gestão de Projetos
Painel completo por Account Manager com drill-down por projeto:
- Estado (Em curso, Em risco, Início, Pausa, Concluído)
- Progresso percentual e prazo
- Gráfico de atividade mensal (reuniões / cotações / contratos)
- Timeline de fases com KPIs e notas
- Feed de comentários e registo de atividade por projeto

### Account Managers
Perfis individuais de cada AM com métricas agregadas, pipeline de projetos atribuídos e notas internas.

### Mercados
Tabela de score por mercado MENA/GCC com indicadores de oportunidade e atividade.

### Calendário
Calendário semanal interativo com navegação por semana, adição de eventos e legenda por tipo (reunião, tarefa, prazo, alerta).

### Notas
Bloco de notas internas da gestão para registos rápidos.

---

## Tecnologia

| Camada | Detalhe |
|---|---|
| Frontend | HTML5 + CSS3 + JavaScript vanilla |
| Charts | [Chart.js 4.4.1](https://www.chartjs.org/) |
| Ícones | [Tabler Icons 3.0](https://tabler.io/icons) |
| Fonte | [DM Sans](https://fonts.google.com/specimen/DM+Sans) (Google Fonts) |
| Persistência | `localStorage` (dados guardados no browser) |
| Deploy | Single `.html` file — sem dependências de servidor |

---

## Como usar

### Opção 1 — Abrir localmente
Basta fazer download do ficheiro `maab_ops_dashboard.html` e abri-lo diretamente no browser. Não requer servidor, instalação ou build.

### Opção 2 — GitHub Pages
1. Ativa **GitHub Pages** no repositório (`Settings → Pages → Deploy from branch: main`)
2. Acede ao preview em `https://maabconsulting.github.io/maab-ops-dashboard/`

O ficheiro `index.html` encaminha automaticamente para `maab_ops_dashboard.html`, por isso a equipa pode usar o link curto do GitHub Pages para acompanhar a versão mais recente.

---

## Estrutura do ficheiro

```
maab_ops_dashboard.html
├── <head>          — meta, fonts, ícones, Chart.js
├── <style>         — design system completo (CSS variables, componentes)
├── <body>          — sidebar + views (Overview, Projetos, AMs, Mercados, Calendário, Notas)
└── <script>        — estado (localStorage), renderização, interações
```

---

## Dados e persistência

Todos os dados são guardados localmente via `localStorage`. O ficheiro inclui um dataset de demonstração com:

- 5 Account Managers
- 15 projetos (vários estados e setores)
- Alertas, tarefas, notas e eventos de calendário de exemplo

Para repor os dados de demonstração, limpa o `localStorage` do browser (`F12 → Application → Local Storage → Clear`).

---

## Contexto

Desenvolvido para uso interno da equipa da **MAAB Consulting** — consultora especializada em expansão internacional e exportação para mercados MENA e GCC para empresas portuguesas.

---

*MAAB Consulting · Uso interno*
