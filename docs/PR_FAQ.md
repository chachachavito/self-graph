# self-graph: Press Release & FAQ

## Press Release: Lançamento do self-graph

**Título:** self-graph: O sistema que entende como você pensa como dev
**Data:** 21 de Abril de 2026
**Local:** São Paulo, SP

O projeto **self-graph** redefine a forma como a senioridade e a identidade técnica são documentadas. Em vez de currículos estáticos ou portfólios subjetivos, o sistema utiliza LLMs para analisar projetos e gerar um grafo dinâmico de competências, padrões e evolução técnica ao longo do tempo.

Construído sobre uma arquitetura moderna com Next.js e Neon, o self-graph foca na ingestão de dados brutos para garantir que a inteligência do sistema evolua sem a necessidade de migrações constantes de schema. "O self-graph transforma projetos reais em um grafo vivo de como um desenvolvedor pensa, projeta e evolui ao longo do tempo", afirma Bruno Chaves, autor do projeto.

---

## FAQ (Perguntas Frequentes)

### 1. O que é o self-graph?
É um sistema de modelagem de identidade técnica que transforma análises de LLMs sobre múltiplos projetos em um grafo de conhecimento consultável.

### 2. Por que usar self-graph em vez do perfil do GitHub?
O GitHub mostra *o que* foi feito (código). O self-graph analisa *como* e *por que* foi feito, extraindo padrões arquiteturais e decisões de design que o código puro não revela.

### 3. Como o custo das LLMs é gerenciado?
A arquitetura impõe controle de custos por padrão, utilizando modelos econômicos (`mini`) para a maioria das tarefas e reservando modelos potentes apenas para análises profundas sob demanda.

### 4. Onde os dados são armazenados?
Os dados são armazenados em um banco de dados Postgres (Neon) com foco em campos JSONB, permitindo flexibilidade total para futuras re-análises.

### 5. Qual é o futuro do projeto?
Evoluir para uma engine de inteligência arquitetural que auxilie na tomada de decisão e no onboarding de novos desenvolvedores em ecossistemas complexos.
