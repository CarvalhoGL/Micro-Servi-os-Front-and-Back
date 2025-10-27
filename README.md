# Hall da Farma - Sistema de Gamificação

## 🏆 Visão Geral

O **Hall da Farma** é um sistema de gamificação desenvolvido para a **Eurofarma** que visa incentivar a participação dos colaboradores em programas de desenvolvimento e capacitação. O sistema utiliza um modelo de pontuação baseado em atividades educacionais, promovendo um ambiente de aprendizado contínuo, reconhecimento e competição saudável.

### Objetivos Principais:
- **Engajar colaboradores** em programas de treinamento.
- **Implementar sistema competitivo saudável**.
- **Fornecer métricas** de participação e desempenho.
- **Promover aprendizado contínuo e reconhecimento**.

---

## ✨ Funcionalidades

### 👥 Gestão de Participantes
- **Adicionar novos participantes**
- **Editar nomes existentes**
- **Remover participantes individualmente**
- **Remover todos os participantes**

### 🎮 Sistema de Atividades
Categorias disponíveis:
- 📚 **Cursos** (100-150 pontos base)
- 💻 **Webinars** (80-90 pontos base)
- 💊 **Pílulas de Conhecimento** (25-30 pontos base)
- 📁 **Áreas Dedicadas** (60-70 pontos base)

### ⭐ Sistema de Pontuação com Bônus
Regras de Bônus:
- **+10%** por atividade adicional no mesmo tópico.
- **+15%** por categoria diferente no mesmo tópico.
- **+20%** por atividades em sequência (até 7 dias).

### 🏆 Sistema de Ranking
- Top 100 participantes
- Atualização semanal automática
- Reset trimestral (a cada 3 meses)
- Persistência de dados no **localStorage**

---

## 🛠 Tecnologias

### Frontend
- **React.js 18.2.0** - Framework JavaScript
- **CSS3** - Estilização e design responsivo
- **HTML5** - Estrutura semântica

### Ferramentas de Desenvolvimento
- **Visual Studio Code** - IDE
- **Git** - Controle de versão
- **npm** - Gerenciador de pacotes

### Armazenamento
- **localStorage** - Persistência local de dados

### Ferramentas de Apoio
- **Figma** - Prototipagem e design
- **Trello** - Gestão de tarefas
- **Slack** - Comunicação da equipe

---

## 🚀 Instalação

### Pré-requisitos
- **Node.js 14+**
- **npm** ou **yarn**

### Passos para Execução

1. **Clone o repositório**:
    ```bash
    git clone [url-do-repositorio]
    ```

2. **Acesse a pasta do projeto**:
    ```bash
    cd hall-da-farma
    ```

3. **Instale as dependências**:
    ```bash
    npm install
    ```

4. **Execute o projeto**:
    ```bash
    npm start
    ```

5. **Acesse no navegador**:
    [http://localhost:3000](http://localhost:3000)

---

### Estrutura dos Arquivos
    hall-da-farma/
    ├── public/
    │   ├── index.html
    │   └── favicon.ico
    ├── src/
    │   ├── components/
    │   │   ├── Header/               # Cabeçalho da aplicação
    │   │   ├── ParticipantManager/   # Gerenciador de participantes
    │   │   ├── ParticipantCard/      # Cartão individual
    │   │   ├── ActivityButtons/      # Botões de atividades
    │   │   ├── RankingSection/       # Seção do ranking
    │   │   └── RankingList/          # Lista do ranking
    │   ├── hooks/
    │   │   ├── useParticipants.js    # Hook para participantes
    │   │   └── useRanking.js         # Hook para ranking
    │   ├── services/
    │   │   ├── pointsCalculator.js   # Calculadora de pontos
    │   │   └── storageService.js     # Serviço de armazenamento
    │   ├── data/
    │   │   └── activitiesData.js     # Dados das atividades
    │   ├── utils/
    │   │   └── constants.js          # Constantes do sistema
    │   ├── App.js                    # Componente principal
    │   ├── App.css                   # Estilos globais
    │   └── index.js                  # Ponto de entrada
    └── package.json

### 🔧 Documentação Técnica

## Arquitetura do Sistema
    
    [Usuário] → [Interface React] → [Gestão de Estado] → [LocalStorage]
         ↓              ↓                  ↓                  ↓
      Adiciona      Visualiza          Calcula           Persiste
      Participante  Ranking            Pontos            Dados
         ↓              ↓                  ↓                  ↓
    [Formulário] → [RankingList] → [PointsCalculator] → [StorageService]
    Componentes Principais

## Componentes Principais
# 1. App.js
Componente raiz que gerencia a estrutura principal da aplicação e providers.

# 2. useParticipants.js
Hook customizado para gerenciamento completo de participantes:
CRUD de participantes

Cálculo de pontuação

Persistência de dados

# 3. PointsCalculator.js
Serviço especializado em cálculo de pontos com regras de bônus:

pontosTotais = pontosBase × (1 + bônusTópico + bônusCategoria + bônusSequência)

# 4. StorageService.js
Serviço de persistência utilizando localStorage.


## Modelos de Dados

    Participante
    {
      id: Number,
      name: String,
      points: Number,
      activitiesCompleted: Array,
      lastActivityDate: String (ISO),
      joinDate: String (ISO)
    }
---
    Atividade Completada
    {
      activityId: Number,
      name: String,
      category: String,
      topic: String,
      pointsEarned: Number,
      basePoints: Number,
      bonus: Number,
      date: String (ISO),
      bonusDetails: Array
    }

### 📊 Relatório do Projeto
## Metodologia de Desenvolvimento

# Fase 1 - Levantamento de Requisitos (1 semana)
Análise de necessidades da Eurofarma

Definição de categorias de atividades

Estabelecimento de regras de pontuação

# Fase 2 - Prototipagem (1 semana)
Wireframes e mockups

Definição da arquitetura técnica

Validação com stakeholders

# Fase 3 - Desenvolvimento (2 semanas)
Implementação frontend

Desenvolvimento da lógica de negócio

Integração com sistemas existentes

# Fase 4 - Testes e Validação (1 semana)
Testes de usabilidade

Validação de regras de negócio

Ajustes finais

## Estimativa de Custos
# Equipe e Esforço:
Desenvolvedor Full Stack Pleno: 120 horas × R$ 85,00/h = R$ 10.200,00

UX/UI Designer: 40 horas × R$ 75,00/h = R$ 3.000,00

Analista de Negócios: 20 horas × R$ 90,00/h = R$ 1.800,00

Total Mão de Obra: R$ 15.000,00

# Infraestrutura (anual):
Hospedagem: R$ 2.400,00/ano

Domínio: R$ 50,00/ano

Monitoramento: R$ 1.200,00/ano

## Custo Total do Projeto: R$ 18.650,00

### Lições Aprendidas
# Pontos Positivos:
Arquitetura modular e componentizada

Experiência do usuário intuitiva

Performance otimizada

Código limpo e documentado

## Pontos de Melhoria:
Escalabilidade com localStorage

Segurança de dados

Funcionalidades analíticas

Integração com backend

## Impacto e Viabilidade
# O projeto demonstra viabilidade técnica e financeira significativa, oferecendo:
ROI positivo através do aumento de engajamento

Redução de custos com plataformas externas

Arquitetura moderna e sustentável

Fácil integração com sistemas existentes

### 🎯 Próximos Passos
## Melhorias Planejadas
Backend Integrado com API REST

Dashboard administrativo com relatórios

Sistema de notificações

Integração com LMS existente

Recursos de acessibilidade

Expansão de Funcionalidades
Badges e conquistas

Sistema de metas individuais

Relatórios analíticos avançados

Integração com sistemas de RH

### 👥 Equipe

# Desenvolvido por: Gabriel Lopes Magon Carvalho, Luiz Carlos Sartoreli Neto, Miguel Fraquilino Castro Leite, Matheus Bustamante Battiato 
Empresa: Eurofarma
Programa: Enterprise Challenge - FIAP
Data de Conclusão: [27/10/2025]

### 📞 Suporte

Para dúvidas técnicas ou sugestões de melhoria, entre em contato através dos canais oficiais da Eurofarma.

### 📄 Licença

Este projeto é desenvolvido para uso interno da Eurofarma. Todas as tecnologias utilizadas possuem licenças open-source.

# Dependencies
node_modules/
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Production builds
build/
dist/

# Environment variables
.env
.env.local
.env.development.local
.env.test.local
.env.production.local

# IDE
.vscode/
.idea/

# OS
.DS_Store

Thumbs.db
