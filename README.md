# ELEVADOR_SONICO

📝 Descrição
Este projeto implementa um sistema de controle de elevador simples para 4 andares (térreo + 3 andares) utilizando o simulador EdSim51. O sistema permite a seleção de andares através de botões e fornece feedback visual do andar atual e estado da porta.

🛠️ Hardware Necessário
Entradas (conectar a P1):

P1.0: Botão do Térreo

P1.1: Botão do 1º Andar

P1.2: Botão do 2º Andar

P1.3: Botão do 3º Andar

Saídas (conectar a P2):

P2.0: LED do Térreo

P2.1: LED do 1º Andar

P2.2: LED do 2º Andar

P2.3: LED do 3º Andar

P2.4: LED da Porta Aberta

🚀 Funcionalidades
Controle completo de 4 andares

Sistema de abertura/fechamento de porta com temporização

Feedback visual do andar atual

Lógica que evita movimento desnecessário quando já está no andar solicitado

⚙️ Lógica de Operação
Inicialização:

Elevador começa no térreo (P2.0 ativo)

Porta fechada (P2.4 desligado)

Seleção de Andar:

Ao pressionar um botão:

Se já está no andar: abre e fecha a porta

Se em outro andar: fecha porta → muda andar → abre porta

Temporização:

Porta fica aberta por 2 ciclos de delay

Movimento entre andares usa 1 ciclo de delay

🧩 Estrutura do Código
MAIN: Inicialização e loop principal

ANDAR_X: Rotinas para cada andar (0 a 3)

MOVER_X: Lógica de movimento para cada andar

ABRIR_PORTA: Controle da porta do elevador

ATRASO: Sub-rotina de delay para temporização
