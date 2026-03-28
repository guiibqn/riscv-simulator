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

## 👩🏽‍💻 O Processo de Desenvolvimento
Comecei o projeto focando no coração do simulador: a CPU. Estruturei o ciclo básico de **Busca (Fetch), Decodificação (Decode) e Execução (Execute)** para que o processador conseguisse ler uma instrução simples e processá-la.

Em seguida, o desafio foi implementar a ISA RV32I completa, garantindo que todas as operações aritméticas, lógicas e de desvio (branches) manipulassem corretamente os 32 registradores internos. 

Com a CPU funcionando, o próximo passo foi arquitetar a Memória RAM. Precisei criar um mapeamento rígido para separar a RAM Principal (onde ficam os dados e a pilha), a VRAM (área de vídeo) e o espaço reservado para periféricos.

Por fim, para unir tudo, desenvolvi o Barramento (Bus). Essa foi uma fase crítica, pois precisei garantir que a comunicação de Dados, Endereços e Sinais de Controle entre a CPU e a Memória ocorresse de forma sincronizada e sem vazamento de dados. 

Documentar e testar cada um desses módulos separadamente com algoritmos em Assembly (como Fibonacci) foi o que garantiu o sucesso da simulação.

## 📚 O Que Eu Aprendi
Durante este projeto, saí da teoria da faculdade e mergulhei em desafios complexos de engenharia de software e baixo nível.

🧠 **Manipulação de Bits (Bitwise Operations):**
- **Lógica Avançada:** Aprendi a utilizar máscaras de bits (bit masking) e deslocamentos (shifts) em C++ para extrair *opcodes*, *funct3* e *funct7* de instruções binárias de 32 bits de forma extremamente eficiente.

🏗️ **Arquitetura e Fluxo de Dados:**
- **Visão Sistêmica:** Entender na prática como um gargalo no barramento afeta a CPU me deu uma visão muito mais clara sobre otimização de software e alocação de memória. 

🧮 **Tradução de Baixo para Alto Nível:**
- **Ponteiros e Referências:** Aprimorei muito meu domínio em C++ ao gerenciar o estado da memória e dos registradores, simulando o comportamento exato de um hardware físico via código.

⚙️ **Modularização de Código:**
- **Clean Code em C++:** Como o projeto cresceu rápido, aprendi a separar responsabilidades (CPU, Memory, Bus) em classes e módulos distintos, tornando o código escalável para adicionar novas instruções no futuro.

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
Dica: Para salvar a saída da execução em um arquivo de texto, utilize: ```bash ./main.exe | Tee-Object -FilePath "relatorio_simulacao.txt"```

## Autores
Guilherme Augusto Boquimpani,
Felipe Francisco Ferreira de Lima
