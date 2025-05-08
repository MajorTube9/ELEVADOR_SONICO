# ELEVADOR_SONICO

📋 Descrição
Sistema de controle de elevador inteligente para 4 andares (térreo + 3 andares) no EdSim51, com:
✅ Botões externos (chamada de andar)
✅ Botões internos (seleção dentro do elevador)
✅ Feedback visual (LEDs indicando andar atual e status da porta)

🖥️ Configuração de Hardware
Entradas
🔘 Botões Externos (Porta P1) → Chamar elevador para um andar:

P1.0 → Térreo

P1.1 → 1º Andar

P1.2 → 2º Andar

P1.3 → 3º Andar

🔘 Botões Internos (Porta P3) → Seleção de destino dentro do elevador:

P3.0 → Térreo

P3.1 → 1º Andar

P3.2 → 2º Andar

P3.3 → 3º Andar

Saídas (Porta P2) → Indicadores visuais:
P2.0 → LED Térreo

P2.1 → LED 1º Andar

P2.2 → LED 2º Andar

P2.3 → LED 3º Andar

P2.4 → LED Porta Aberta

⚡ Funcionalidades Aprimoradas
✔ Dupla entrada de comandos (dentro e fora do elevador)
✔ Priorização inteligente (se já estiver no andar, só abre/fecha a porta)
✔ Temporização ajustável (2 ciclos para porta, 1 ciclo para movimento)
✔ Economia de movimento (evita deslocamentos desnecessários)

🔄 Lógica de Operação
1. Estado Inicial
Elevador no térreo (P2.0 ativo)

Porta fechada (P2.4 desligado)

2. Modos de Ativação
Botão externo (P1) → Chama o elevador para o andar

Botão interno (P3) → Seleciona o destino

3. Comportamento
Se já estiver no andar solicitado:

Abre → Espera 2 ciclos → Fecha a porta

Se estiver em outro andar:

Fecha a porta → Move-se → Abre a porta

🏗️ Estrutura do Código
MAIN → Loop principal e inicialização

ANDAR_X → Lógica específica para cada andar

MOVER_X → Transição entre andares

ABRIR_PORTA → Controle da porta

ATRASO → Temporização

Melhoria:
Agora o sistema verifica tanto P1 (externo) quanto P3 (interno) para decidir o movimento, tornando-o mais realista! 🚀




![Image](https://github.com/user-attachments/assets/904e4a1c-f8ca-44c3-b4e7-c4993824f463)
