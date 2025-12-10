# Simulador de Processador RISC-V (C++)

Simulador modular da arquitetura **RISC-V** desenvolvido em **C++**. O projeto emula o comportamento de baixo nível de um processador, gerenciando o ciclo de instruções, memória e barramentos.

Desenvolvido para a disciplina de **Organização de Computadores**

## Estrutura do Projeto

O código foi organizado de forma modular para simular os componentes físicos:

- **core/**: Contém a lógica da CPU e decodificação de instruções.
- **memory/**: Gerenciamento de memória RAM e Barramento (Bus).
- **peripherals/**: Simulação de entrada e saída (I/O).

## Funcionalidades Implementadas

- **Ciclo de Instrução Completo:** Busca (Fetch), Decodificação (Decode) e Execução (Execute).
- **Execução de Algoritmos Reais:** Capaz de executar códigos em Assembly RISC-V, como o cálculo da sequência de **Fibonacci** (incluso nos arquivos de teste).
- **Leitura de Binários:** Carrega arquivos de texto (`prog.txt`) simulando a memória de instruções.

## Como Compilar e Rodar

Pré-requisito: Compilador `g++` (MinGW ou GCC).

1. Clone o repositório:
   ```bash
   git clone [https://github.com/guiibqn/riscv-simulator.git](https://github.com/guiibqn/riscv-simulator.git)
2. Compile o código (exemplo via terminal):
    ```bash
   g++ main.cpp -o main
3. Execute o simulador:
    ```bash
    .\main.exe
4. (Execução alternativa) Execute o simulador com saída no terminal e saída em txt:
    ```bash
    ./main.exe | Tee-Object -FilePath "relatorio_simulacao.txt"

## Autores
Guilherme Augusto Boquimpani,
Felipe Francisco Ferreira de Lima
