# 📅 Gerenciador de Eventos

Aplicação web para gerenciamento de eventos pessoais com visualização em calendário semanal. Desenvolvida com React, TypeScript e Recoil para gerenciamento de estado.

## 🚀 Funcionalidades

- ✅ **Criar eventos**: Adicione novos eventos com descrição, data e hora de início e término
- 📅 **Visualização em calendário**: Visualize seus eventos em um calendário semanal interativo
- 🔍 **Filtro por data**: Filtre eventos por data específica
- ✓ **Marcar como completo**: Marque eventos como concluídos
- 🗑️ **Excluir eventos**: Remova eventos que não são mais necessários
- 🔄 **Arrastar e soltar**: Atualize a data/hora dos eventos arrastando-os no calendário

## 🛠️ Tecnologias Utilizadas

- **React 17** - Biblioteca JavaScript para construção de interfaces
- **TypeScript** - Superset do JavaScript com tipagem estática
- **Recoil** - Biblioteca para gerenciamento de estado
- **Kalend** - Componente de calendário para React
- **json-server** - Servidor REST mock para desenvolvimento
- **Moment.js** - Biblioteca para manipulação de datas
- **SCSS Modules** - Estilização com módulos CSS
- **Create React App** - Ferramenta para criação do projeto

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

- Node.js (versão 14 ou superior)
- npm ou yarn

## 🔧 Instalação

1. Clone o repositório:

```bash
git clone <url-do-repositorio>
cd trilha-react-3
```

2. Instale as dependências:

```bash
npm install
```

## 🎯 Como Executar

### Desenvolvimento

1. Inicie o servidor JSON (backend mock):

```bash
npx json-server --watch db.json --port 8080
```

2. Em outro terminal, inicie a aplicação React:

```bash
npm start
```

3. Acesse a aplicação em [http://localhost:3000](http://localhost:3000)

A página será recarregada automaticamente quando você fizer alterações no código.

### Build para Produção

Para criar uma versão otimizada para produção:

```bash
npm run build
```

Isso criará uma pasta `build` com os arquivos otimizados e prontos para deploy.

### Executar Testes

```bash
npm test
```

## 📁 Estrutura do Projeto

```
trilha-react-3/
├── public/                 # Arquivos estáticos
├── src/
│   ├── components/         # Componentes React
│   │   ├── Calendario/     # Componente de calendário semanal
│   │   ├── Card/           # Componente de card genérico
│   │   ├── Evento/         # Componente de evento individual
│   │   ├── Filtro/         # Componente de filtro por data
│   │   ├── Formulario/     # Formulário para criar eventos
│   │   └── ListaDeEventos/ # Lista de eventos filtrados
│   ├── interfaces/         # Definições TypeScript
│   │   ├── IEvento.ts      # Interface do evento
│   │   └── IFiltroDeEventos.ts
│   ├── state/              # Gerenciamento de estado (Recoil)
│   │   ├── atom.ts         # Atoms do Recoil
│   │   ├── hooks/          # Hooks customizados
│   │   └── selectors/      # Selectors do Recoil
│   ├── App.tsx             # Componente principal
│   └── index.tsx           # Ponto de entrada
├── db.json                 # Banco de dados mock (json-server)
└── package.json
```

## 🎨 Componentes Principais

### Formulario

Formulário para criação de novos eventos com campos para:

- Descrição do evento
- Data e hora de início
- Data e hora de término

### Calendario

Calendário semanal interativo que permite:

- Visualizar todos os eventos
- Arrastar eventos para atualizar data/hora
- Navegação entre semanas

### ListaDeEventos

Lista de eventos filtrados que exibe:

- Descrição e data do evento
- Checkbox para marcar como completo
- Botão para excluir evento

### Filtro

Componente para filtrar eventos por data específica.

## 🔄 Gerenciamento de Estado

O projeto utiliza **Recoil** para gerenciamento de estado:

- **Atoms**:

  - `listaDeEventosState`: Armazena a lista completa de eventos
  - `filtroDeEventos`: Armazena o filtro de data atual

- **Selectors**:

  - `eventosAsync`: Busca eventos do servidor JSON
  - `eventosFiltradosState`: Filtra eventos baseado na data selecionada

- **Hooks Customizados**:
  - `useListaDeEventos`: Retorna eventos filtrados
  - `useAdicionarEvento`: Adiciona novo evento
  - `useAtualizarEvento`: Atualiza evento existente

## 📡 API (json-server)

A aplicação utiliza json-server rodando na porta 8080. O arquivo `db.json` contém os dados dos eventos.

**Endpoints disponíveis:**

- `GET /eventos` - Lista todos os eventos
- `POST /eventos` - Cria novo evento
- `PUT /eventos/:id` - Atualiza evento
- `DELETE /eventos/:id` - Remove evento

## 🌐 Localização

O calendário está configurado para português brasileiro (pt-BR) através do arquivo `src/components/Calendario/localizacao/ptBR.json`.

## 📝 Scripts Disponíveis

- `npm start` - Inicia o servidor de desenvolvimento
- `npm run build` - Cria build de produção
- `npm test` - Executa os testes
- `npm run eject` - Ejeta a configuração do Create React App (irreversível)

## 🔍 Debug

O projeto inclui um componente `DebugObserver` que monitora mudanças no estado do Recoil durante o desenvolvimento.

## 📚 Aprendizados

Este projeto demonstra:

- Gerenciamento de estado com Recoil
- Integração de componentes de calendário
- Manipulação de datas em JavaScript/TypeScript
- Estruturação de projetos React com TypeScript
- Uso de SCSS Modules para estilização
- Integração com API REST mock

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## 📄 Licença

Este projeto é privado.
