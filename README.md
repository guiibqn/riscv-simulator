# 💻 Simulador de Processador RISC-V (RV32I)

Simulador modular construído em **C++** que emula o comportamento de baixo nível de um processador RISC-V. O projeto gerencia desde o ciclo de máquina (Fetch, Decode, Execute) até o mapeamento de memória RAM/VRAM e controle de barramentos.

Desenvolvido como projeto final para a disciplina de Organização de Computadores.

## 🛠️ Tecnologias Utilizadas
- **C++** (Lógica core e manipulação de bits)
- **g++ / MinGW** (Compilação)
- **Assembly RISC-V** (Testes e algoritmos)

## ✨ Principais Funcionalidades
- **Implementação da ISA RV32I:** Suporte completo às instruções aritméticas, lógicas, de desvio e registradores base do RISC-V.
- **Ciclo de Máquina Completo:** Simulação passo a passo de Busca (Fetch), Decodificação (Decode) e Execução (Execute).
- **Gerenciamento de Barramento (Bus):** Implementação de barramentos de 32 bits separados para Dados, Endereços e Controle.
- **Mapeamento de Memória:** Separação lógica entre RAM Principal, VRAM (Vídeo) e Periféricos de E/S.
- **Execução de Algoritmos Reais:** Leitura de arquivos binários (`prog.txt`) para execução de algoritmos complexos, como o cálculo da sequência de Fibonacci.

## 🏗️ Arquitetura do Projeto
O código foi estruturado de forma modular para espelhar os componentes físicos de um computador real:
- `/core`: Contém a lógica central da CPU, decodificação de instruções e registradores.
- `/memory`: Gerenciamento da memória RAM, mapeamento de endereços e Barramento (Bus).
- `/peripherals`: Simulação de entrada e saída (I/O).

## 🧠 O que aprendemos
Construir este simulador do zero foi um mergulho profundo em arquitetura de computadores. Os maiores aprendizados incluíram:
- Como manipular operações *bitwise* em C++ para decodificar instruções binárias.
- A mecânica exata de como a CPU interage com a memória através de barramentos limitados.
- O funcionamento do ciclo de *clock* e como os registradores mantêm o estado do programa.

## 🚀 Próximos Passos (Melhorias Futuras)
- Implementar suporte a **Memória Cache** (com políticas de substituição).
- Modificar a microarquitetura para suportar execução em **Pipeline**.
- Adicionar suporte a **Interrupções Externas** via teclado.

## ⚙️ Como Rodar o Projeto

Pré-requisito: Compilador `g++` (MinGW ou GCC) instalado.

1. Clone o repositório:
  ```bash
git clone [https://github.com/guiibqn/riscv-simulator.git](https://github.com/guiibqn/riscv-simulator.git)
```
2. Compile o código (exemplo via terminal):
```bash
g++ main.cpp -o maiN
```
3. Execute o simulador:
```bash
    .\main.exe
```

## Autores
Guilherme Augusto Boquimpani,
Felipe Francisco Ferreira de Lima
