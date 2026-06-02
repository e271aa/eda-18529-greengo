# EDA GreenGo — Sistema de Gestão de Mobilidade Elétrica

Projeto académico desenvolvido no âmbito da cadeira de **Estruturas de Dados Avançadas (EDA)**.

Sistema completo de gestão para uma empresa de mobilidade elétrica fictícia, permitindo gerir meios de transporte, clientes, aluguéis e otimizar rotas através de algoritmos de grafos.

## Funcionalidades Principais

### Gestão de Meios de Transporte
- Inserir, remover e listar meios de mobilidade elétrica
- Acompanhar bateria e autonomia de cada veículo
- Persistência de dados em base de dados

### Gestão de Clientes
- Registar, atualizar e remover clientes
- Consultar histórico de aluguéis por cliente
- Validação de dados de contacto

### Sistema de Aluguéis
- Criar e gerir aluguéis de veículos
- Rastrear status de aluguéis ativo/completo
- Cálculo automático de custos

### Otimização de Rotas
- Implementação de **grafos** para análise de rotas
- Algoritmos de otimização de trajetos entre pontos
- Suporte para cálculo de distâncias

### Autenticação
- Sistema de login para administradores
- Controlo de acesso às funcionalidades

## Estruturas de Dados

O projeto utiliza múltiplas estruturas de dados fundamentais:

- **Listas ligadas** — gestão dinâmica de meios e clientes
- **Grafos** — representação e otimização de rotas
- **Base de dados** — persistência de registos em ficheiro

## Tecnologias e Linguagens

- **Linguagem:** C
- **Compilador:** GCC/MinGW
- **Plataforma:** Windows (utiliza `windows.h` e `conio.h`)
- **Estrutura:** Modular com separação entre headers (`include/`) e implementação (`src/`)

## Estrutura do Projeto

```
eda-18529-greengo/
├── src/                    # Ficheiros fonte (.c)
│   ├── main.c            # Programa principal e menus interativos
│   ├── meio.c            # Gestão de meios de transporte
│   ├── cliente.c         # Gestão de clientes
│   ├── aluguer.c         # Sistema de aluguéis
│   ├── grafo.c           # Implementação de grafos para rotas
│   ├── gestor.c          # Autenticação e administração
│   └── tools.c           # Funções auxiliares e utilitários
├── include/               # Ficheiros cabeçalho (.h)
│   ├── meio.h
│   ├── cliente.h
│   ├── aluguer.h
│   ├── grafo.h
│   ├── gestor.h
│   └── tools.h
├── bin/                   # Executáveis compilados
├── db/                    # Base de dados e persistência
├── doc/                   # Documentação do projeto
└── README.md              # Este ficheiro
```

## Compilação

### Pré-requisitos
- GCC/MinGW instalado
- Compilador compatível com C99+

### Comandos de Compilação

Compilar a versão completa:
```bash
gcc -o ./bin/GreenGo src/main.c src/gestor.c src/meio.c src/cliente.c src/aluguer.c src/tools.c src/grafo.c
```

Compilar versão de teste:
```bash
gcc -o ./bin/TESTE src/fase1.c src/cliente.c src/meio.c
```

## Execução

```bash
./bin/GreenGo
```

Após iniciar, utilize:
- **Setas** (↑↓) — Navegar no menu
- **Enter** — Selecionar opção
- **ESC** — Voltar/Sair

## Detalhes Técnicos

### Módulos Principais

#### `main.c` (538 linhas)
- Interface gráfica em modo consola
- Sistema de navegação por teclado
- Controlo de fluxo principal

#### `tools.c` (3382 linhas)
- Biblioteca de funções auxiliares
- Manipulação de strings e I/O
- Utilitários gerais

#### `grafo.c` (297 linhas)
- Implementação de estruturas de grafo
- Algoritmos de otimização de rotas

#### `aluguer.c` (353 linhas)
- Lógica de aluguéis
- Cálculo de custos

#### Módulos suplementares
- `cliente.c` (304 linhas) — Gestão de clientes
- `meio.c` (303 linhas) — Gestão de meios
- `gestor.c` (234 linhas) — Autenticação e controlo

## Base de Dados

O projeto utiliza ficheiros de persistência armazenados na pasta `db/` para manter dados entre execuções.

## Versões

- **Versão Pilot:** [eda-18529-greengo-pilot](https://github.com/e271aa/eda-18529-greengo-pilot) — Versão inicial com listas ligadas básicas
- **Versão Final:** [eda-18529-greengo](https://github.com/e271aa/eda-18529-greengo) — Versão completa com grafos, otimização e sistema de aluguéis

---

Desenvolvido por Ruben Martins · nº 18529
