EN | [PT-BR](#PT-BR)

---

# Arithmetic and Logic Unit (ALU)

## 📋 Description

This project implements a complete **Arithmetic and Logic Unit (ALU)** in hardware using **Cyclone V FPGA** with **Intel Quartus Prime** design tools. The ALU is capable of performing arithmetic operations (addition, subtraction) and logical operations (AND, XOR, NOT) on multiple bits, with support for value comparison and 7-segment display visualization.

## 🔧 Features

### Arithmetic Operations
- **Addition**: 4 and 5-bit adders with carry propagation
- **Subtraction**: Subtractors implemented in ALU
- **Full Adders**: Basic blocks for complex arithmetic operations

### Logical Operations
- **AND bit-by-bit**: Boolean logical operations
- **XOR bit-by-bit**: Boolean logical operations
- **NOT complemented**: Signal inversion

### Auxiliary Components
- **Multiplexers (MUX)**: Operation and data selection (1, 4, 6 bits)
- **Comparators**: 2 and 4-bit comparison
- **Decoders**: Signal conversion
- **7-Segment Displays**: Result visualization (4 and 5 bits)
- **Zero Correctors**: Value adjustment and handling

## 📁 Project Structure

```
ALU/
├── AluFinal.bdf              # Main ALU entity
├── Alu_Adder.bdf             # Combined ALU + Adder module
├── ALU_BOOL.bdf              # Boolean logical operations
├── 
├── # Arithmetic Operations
├── adder4bits.bdf            # 4-bit adder
├── adder5bits.bdf            # 5-bit adder
├── Subtrator.bdf             # Subtractor
├── fulladder.bdf             # Full Adder (1 bit)
├── 
├── # Logical Operations
├── ANDbitabit.bdf            # AND bit-by-bit
├── Xorbitabit.bdf            # XOR bit-by-bit
├── not5.bdf                  # NOT 5 bits
├── inversorsinal.bdf         # Signal inverter
├── 
├── # Selection Components
├── Mux1bit.bdf               # 1 bit multiplexer
├── Mux4bits.bdf              # 4 bits multiplexer
├── Mux6bits.bdf              # 6 bits multiplexer
├── Mux_ALu.bdf               # MUX for operation selection
├── 
├── # Comparators
├── compa2.bdf                # 2-bit comparator
├── Compa24bits.bdf           # 2/4-bit comparator
├── COMPARADOR.bdf            # Main comparator
├── 
├── # Visualization
├── 7Segmentos4bits.bdf       # 7-segment display 4 bits
├── 7Segmentos5bits.bdf       # 7-segment display 5 bits
├── display.bdf               # Display module
├── 
├── # Quartus Project Files
├── alu.qpf                   # Project file
├── alu.qsf                   # Project settings
├── 
├── db/                        # Quartus database
├── incremental_db/            # Incremental compilation
├── output_files/              # Generated files
├── simulation/                # Simulation files
└── waveforms/                 # Test waveforms
```

## 🛠️ Tools and Technologies

| Tool | Version | Description |
|---|---|---|
| **Intel Quartus Prime** | 20.1.1 Lite Edition | IDE for design and compilation |
| **FPGA** | Cyclone V (5CSXFC6D6F31C6) | Implementation platform |
| **Language** | Block Diagram Format (BDF) | Visual circuit design |
| **Simulation** | ModelSim-Altera | Behavior verification |

## 📊 Technical Specifications

- **Data width**: 4 and 5 bits (depending on operation)
- **FPGA Family**: Cyclone V
- **Device**: 5CSXFC6D6F31C6
- **Operating temperature**: 0°C to 85°C

## 🚀 How to Use

### Prerequisites
- Intel Quartus Prime 20.1.1 or higher
- Cyclone V FPGA or compatible
- ModelSim-Altera for simulation (optional)

### Compilation
1. Open the `alu.qpf` project in Quartus Prime
2. Verify pin assignments in `alu.qsf`
3. Execute **Compile Design** to generate implementation files
4. Compiled files will be in `output_files/`

### Simulation
1. In Quartus Prime, go to **Tools → Run Simulation Tool → RTL Simulation**
2. Simulation files are in `simulation/`
3. View waveforms in `waveforms/`

### FPGA Programming
1. Generate programming file (`.sof` or `.pof`)
2. Use **Quartus Programmer** to load on the board
3. Check displays to confirm execution

## 📝 Main Components Explained

### Adder (Adder)
Implements binary addition with carry propagation. Supports 4 and 5 bits.
- Input: A, B (numbers to add)
- Output: Result, Carry

### Subtractor (Subtrator)
Performs subtraction using complementary logic.
- Input: A, B (number to subtract from A)
- Output: Result, Borrow

### Comparator (Compa)
Compares two binary numbers.
- Input: A, B
- Output: A>B, A=B, A<B

### Multiplexer (Mux)
Selects which operation will be executed based on selection lines.
- Input: Multiple operations
- Output: Selected result

### 7-Segment Display
Converts binary result to 7-segment display visualization.

## 📄 License

This project follows the Intel FPGA license provided with Quartus Prime.

---

# PT-BR

[EN](#Arithmetic-and-Logic-Unit-ALU) | PT-BR

# Unidade Lógica e Aritmética (ULA)

## 📋 Descrição

Este projeto implementa uma **Unidade Lógica e Aritmética (ULA)** completa em hardware usando **FPGA Cyclone V** com a ferramenta **Intel Quartus Prime**. A ULA é capaz de realizar operações aritméticas (adição, subtração) e lógicas (AND, XOR, NOT) em múltiplos bits, com suporte a comparação de valores e exibição em display de 7 segmentos.

## 🔧 Características

### Operações Aritméticas
- **Adição**: Somadores de 4 e 5 bits com propagação de carry
- **Subtração**: Subtratores implementados com ALU
- **Full Adders**: Blocos básicos para operações aritméticas complexas

### Operações Lógicas
- **AND bit a bit**: Operações lógicas booleanas
- **XOR bit a bit**: Operações lógicas booleanas
- **NOT complementado**: Inversão de sinais

### Componentes Auxiliares
- **Multiplexadores (MUX)**: Seleção de operações e dados (1, 4, 6 bits)
- **Comparadores**: Comparação de 2 e 4 bits
- **Decodificadores**: Conversão de sinais
- **Displays de 7 Segmentos**: Visualização de resultados (4 e 5 bits)
- **Corretores de Zero**: Ajuste e tratamento de valores

## 📁 Estrutura do Projeto

```
ALU/
├── AluFinal.bdf              # Entidade principal da ULA
├── Alu_Adder.bdf             # Módulo combinado ALU + Adder
├── ALU_BOOL.bdf              # Operações lógicas booleanas
├── 
├── # Operações Aritméticas
├── adder4bits.bdf            # Somador de 4 bits
├── adder5bits.bdf            # Somador de 5 bits
├── Subtrator.bdf             # Subtrator
├── fulladder.bdf             # Full Adder (1 bit)
├── 
├── # Operações Lógicas
├── ANDbitabit.bdf            # AND bit a bit
├── Xorbitabit.bdf            # XOR bit a bit
├── not5.bdf                  # NOT de 5 bits
├── inversorsinal.bdf         # Inversor de sinal
├── 
├── # Componentes de Seleção
├── Mux1bit.bdf               # Multiplexador 1 bit
├── Mux4bits.bdf              # Multiplexador 4 bits
├── Mux6bits.bdf              # Multiplexador 6 bits
├── Mux_ALu.bdf               # MUX para seleção de operação
├── 
├── # Comparadores
├── compa2.bdf                # Comparador 2 bits
├── Compa24bits.bdf           # Comparador 2/4 bits
├── COMPARADOR.bdf            # Comparador principal
├── 
├── # Visualização
├── 7Segmentos4bits.bdf       # Display 7 segmentos 4 bits
├── 7Segmentos5bits.bdf       # Display 7 segmentos 5 bits
├── display.bdf               # Módulo display
├── 
├── # Arquivos de Projeto Quartus
├── alu.qpf                   # Arquivo de projeto
├── alu.qsf                   # Configurações do projeto
├── 
├── db/                        # Banco de dados Quartus
├── incremental_db/            # Compilação incremental
├── output_files/              # Arquivos gerados
├── simulation/                # Arquivos de simulação
└── waveforms/                 # Formas de onda de teste
```

## 🛠️ Ferramentas e Tecnologias

| Ferramenta | Versão | Descrição |
|---|---|---|
| **Intel Quartus Prime** | 20.1.1 Lite Edition | IDE para design e compilação |
| **FPGA** | Cyclone V (5CSXFC6D6F31C6) | Plataforma de implementação |
| **Linguagem** | Block Diagram Format (BDF) | Design visual de circuitos |
| **Simulação** | ModelSim-Altera | Verificação de comportamento |

## 📊 Especificações Técnicas

- **Largura de dados**: 4 e 5 bits (conforme operação)
- **Família FPGA**: Cyclone V
- **Dispositivo**: 5CSXFC6D6F31C6
- **Temperatura de operação**: 0°C a 85°C

## 🚀 Como Usar

### Pré-requisitos
- Intel Quartus Prime 20.1.1 ou superior
- FPGA Cyclone V ou compatível
- ModelSim-Altera para simulação (opcional)

### Compilação
1. Abra o projeto `alu.qpf` no Quartus Prime
2. Verifique as atribuições de pinos em `alu.qsf`
3. Execute **Compile Design** para gerar os arquivos de implementação
4. Os arquivos compilados estarão em `output_files/`

### Simulação
1. No Quartus Prime, acesse **Tools → Run Simulation Tool → RTL Simulation**
2. Os arquivos de simulação estão em `simulation/`
3. Visualize as formas de onda em `waveforms/`

### Programação do FPGA
1. Gere o arquivo de programação (`.sof` ou `.pof`)
2. Use **Quartus Programmer** para carregar na placa
3. Verifique os displays para confirmar a execução

## 📝 Componentes Principais Explicados

### Somador (Adder)
Implementa a adição binária com propagação de carry. Suporta 4 e 5 bits.
- Entrada: A, B (números a somar)
- Saída: Resultado, Carry (vai-um)

### Subtrator (Subtrator)
Realiza subtração usando lógica complementar.
- Entrada: A, B (número a subtrair de A)
- Saída: Resultado, Borrow (complemento)

### Comparador (Compa)
Compara dois números binários.
- Entrada: A, B
- Saída: A>B, A=B, A<B

### Multiplexador (Mux)
Seleciona qual operação será executada baseado em linhas de seleção.
- Entrada: Múltiplas operações
- Saída: Resultado selecionado

### Display de 7 Segmentos
Converte resultado binário para visualização em display de 7 segmentos.

## 📄 Licença

Este projeto segue a licença Intel FPGA fornecida com o Quartus Prime.
