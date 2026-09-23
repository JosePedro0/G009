# Solicitação de dados — projeto BVE

**Destinatário:** Buena Vista Energy — operação, PCO e gestão de dados  
**Solicitante:** Grupo G009  
**Data:** 23/09/2026  
**Referência:** modelo conceitual v0.1

Solicitamos preferencialmente 12 meses consecutivos de dados, incluindo períodos de pico, até o final da segunda semana. A disponibilidade e o período definitivo serão acordados com a BVE. Entregar tabelas CSV UTF-8, com dicionário, identificadores relacionáveis, unidades e horários com fuso explícito. Identificadores de navios podem ser pseudonimizados. Não são necessários dados pessoais de tripulantes.

**P:** parametrização; **V:** validação. Os responsáveis abaixo são áreas sugeridas, a confirmar.

| ID/processo | Dados e campos solicitados | Unidade/granularidade | Período/frequência | Finalidade e vínculo com o modelo | Área sugerida |
|---|---|---|---|---|---|
| D01 — Demanda | pedido_id, navio_id, classe, produto, quantidade, ponto, criação, confirmação, prazo comercial, janela inicial | Uma linha por pedido; t; data/hora | 12 meses; por pedido | P: chegadas, volumes, prioridades e janelas | Comercial/PCO |
| D02 — Demanda | pedido_id, instante da atualização, previsão anterior/nova, atracação e saída reais, cancelamento e motivo | Uma linha por atualização; data/hora | 12 meses; por evento | P: incerteza e reprogramação; V: janelas efetivas | Agência/PCO |
| D03 — Frota | barcaça_id, capacidade útil por produto/compartimento, vazão efetiva, velocidade, compatibilidade, calendário | Cadastro por barcaça; t, t/h, km/h | Cadastro e vigências | P: recursos heterogêneos e restrições | Operação |
| D04 — Abastecimento | pedido_id, barcaça_id, saída, chegada, preparação, início/fim de bombeamento, liberação, quantidade entregue, interrupções e motivo | Uma linha por etapa/evento; t; data/hora | 12 meses; por serviço | P: tempos; V: entregas, espera e pontualidade | Operação |
| D05 — Navegação | origem_id, destino_id, barcaça_id, partida, chegada, distância, restrições de trânsito e condição ambiental | Uma linha por viagem; h, km | 12 meses; por viagem | P: matriz de tempos e variabilidade | Operação |
| D06 — Terminal | berço_id, bomba_id, compatibilidades, compartilhamentos, vazões, horários, tempos de preparação/liberação | Cadastro por recurso; t/h, h | Cadastro e alterações | P: capacidade e contenção no carregamento | Terminal |
| D07 — Carregamento | carga_id, barcaça_id, berço_id, bomba_id, chegada à fila, início/fim das etapas, produto, quantidade | Uma linha por etapa/carga; t; data/hora | 12 meses; por carga | P: duração e política; V: filas e ocupação | Terminal |
| D08 — Estoques | terminal/barcaça_id, produto, estoque, reposição, retirada, perdas/ajustes e capacidade útil | Por movimentação e saldo diário; t | 12 meses; por movimento | P: balanços, oferta e recarga; V: conservação | Terminal/estoques |
| D09 — Disponibilidade | recurso_id, falha/manutenção, início, fim, motivo, condição climática, bloqueios e regras de retomada | Uma linha por indisponibilidade; h | 12 meses; por evento | P: falhas e calendários; V: disponibilidade | Manutenção/operação |
| D10 — PCO | instante, versão da programação, pedidos e barcaças alocados, sequência, prioridade, reservas, alterações, justificativas | Uma linha por decisão; data/hora | 12 meses; por revisão | P: política atual, frequência e horizonte; V: aderência | PCO |
| D11 — Estado inicial | instante de referência, posição/estoque por barcaça, serviços em curso e término esperado, filas, estoque do terminal, pedidos pendentes | Fotografia sincronizada; t; data/hora | Início de cada período reproduzido | P: inicialização sem sistema artificialmente vazio | PCO/terminal |
| D12 — Resultados históricos | data, volume entregue, pedidos elegíveis, pontuais, perdidos e cancelados, esperas, ocupação por estado | Diário/semanal; t, h, % | 12 meses; separado por período | V: comparação independente e conciliação com eventos | Gestão operacional |
| D13 — Regras e cenários | regras de janela, prioridade, fracionamento, recarga, estoque mínimo, serviço mínimo aceito, alternativas viáveis e limites | Documento e parâmetros com vigência | Situação atual e mudanças propostas | P/V: confirmar hipóteses, capacidade e critérios de aceite | Gestão/PCO |

Reservaremos um bloco cronológico para validação, sem utilizá-lo no ajuste; a divisão considerará sazonalidade e volume disponível. Informar lacunas, alterações de sistemas e critérios dos indicadores. Valores ausentes devem permanecer identificados, sem serem convertidos em zero. Conferiremos duplicidades, integridade entre identificadores, sequência temporal e balanços de massa. Na ausência de registros, solicitaremos entrevista e amostragem operacional, documentando a incerteza correspondente. A definição de compatibilidade, janela física e prazo comercial deve acompanhar as tabelas para evitar interpretações diferentes.
