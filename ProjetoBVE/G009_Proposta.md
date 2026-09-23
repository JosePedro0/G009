# Proposta de consultoria — capacidade da operação de bunkering

**À Buena Vista Energy (BVE)**  
**Data:** 23 de setembro de 2026  
**Proponente:** Grupo G009  
**Situação:** minuta acadêmica para conferência com a carta-convite e aprovação do grupo.

| Nome completo | Número USP |
|---|---|
| Carla Sahuquillo | 18401953 |
| Chloé Brangerieau | 18420440 |
| Guilherme Teixeira Costa | 13725570 |
| José Pedro Coimbra | 15638527 |

## 1. Problema e objetivo

A operação de bunkering precisa conciliar pedidos de navios, janelas de atracação, disponibilidade e estoque das barcaças, deslocamentos e carregamento no terminal. A variabilidade desses elementos pode gerar filas, atrasos e perda de atendimentos. O estudo avaliará quais recursos e regras operacionais permitem ampliar em 20% a capacidade de atendimento da BVE, preservando um nível de serviço acordado.

Define-se capacidade como o maior volume médio diário entregue, em toneladas/dia, sustentável ao longo do horizonte avaliado, com pelo menos 95% dos pedidos elegíveis concluídos dentro de suas janelas e sem crescimento persistente da carteira pendente. O limiar de 95% é uma proposta para validação com a BVE. Manteremos constantes o perfil dos pedidos e os critérios de medição ao comparar cenários. A meta será C1 ≥ 1,20 × C0, em que C0 e C1 são as capacidades estimadas da configuração atual e da alternativa. O volume histórico realizado não será automaticamente considerado capacidade.

## 2. Escopo

Serão representados quatro processos: chegada e atualização de pedidos; abastecimento de navios pelas barcaças; retorno e carregamento das barcaças no terminal; planejamento e controle da operação (PCO). O estudo incluirá janelas, capacidades, estoques, tempos, filas, prioridades e indisponibilidades relevantes.

Serão comparados o cenário atual, uma regra alternativa de programação, uma alternativa de disponibilidade da frota e uma alternativa de capacidade de carregamento. As configurações serão definidas após o diagnóstico, sem pressupor a aquisição de recursos. Alterações combinadas serão limitadas às mais promissoras para respeitar o esforço disponível.

Ficam fora do escopo a implantação em produção, integração automática com sistemas, projeto de engenharia de instalações, negociação de contratos e otimização exata de grande porte. A reposição de combustível no terminal será uma entrada exógena quando houver dados; eventual hipótese de oferta ilimitada será declarada e submetida à análise de sensibilidade.

## 3. Método e indicadores

Será desenvolvido um modelo de simulação de eventos discretos. O processo descrito por Costa e Mesquita (2023), especialmente a seção 3, orientará a representação inicial, sujeita à confirmação das particularidades da BVE. A opção por simulação é uma decisão desta proposta, não uma reprodução do modelo de otimização do artigo.

As etapas compreendem diagnóstico, coleta e tratamento de dados, modelagem conceitual, implementação, verificação, validação e experimentação. Dados históricos distintos serão reservados à parametrização e à validação. Serão utilizados cenários comparáveis, replicações independentes e intervalos de confiança de 95%.

Os indicadores principais serão toneladas entregues por dia, percentual de pedidos atendidos no prazo, percentual não atendido, espera média e percentil 95, utilização das barcaças e dos recursos de carregamento, e evolução da carteira pendente. A análise identificará gargalos e condições necessárias à expansão, sem prometer antecipadamente a viabilidade dos 20%.

## 4. Entregas e cronograma

| Semanas | Atividade e marco | Horas da equipe |
|---|---|---:|
| 1–2 | Diagnóstico; modelo conceitual e solicitação de dados aprovados | 48 |
| 3–4 | Base tratada, hipóteses registradas e protótipo | 48 |
| 5–6 | Modelo implementado, verificado e validado | 48 |
| 7–8 | Experimentos de capacidade e comparação de alternativas | 48 |
| 9–10 | Sensibilidade, recomendações, relatório e apresentação | 48 |
| **Total** | **10 semanas** | **240** |

As entregas da consultoria serão modelo conceitual versionado, dicionário e base tratada dos dados autorizados, código reproduzível, relatório de verificação e validação, análise dos cenários e recomendação final. Os três documentos deste laboratório constituem a abertura do projeto, e não os resultados já executados da consultoria.

## 5. Equipe e orçamento

A equipe é composta por quatro integrantes, cada um com 6 horas semanais por 10 semanas, totalizando 60 horas por pessoa. As taxas abaixo são valores propostos para o exercício acadêmico, não cotações de mercado. Coordenação, reuniões e revisão estão incluídas.

| Papel principal | Integrante | Horas | Valor/hora | Subtotal |
|---|---|---:|---:|---:|
| Coordenação e análise operacional | A definir pelo grupo | 60 | R$ 120 | R$ 7.200 |
| Modelagem e simulação | A definir pelo grupo | 60 | R$ 110 | R$ 6.600 |
| Dados e parametrização | A definir pelo grupo | 60 | R$ 90 | R$ 5.400 |
| Validação e análise de cenários | A definir pelo grupo | 60 | R$ 100 | R$ 6.000 |
| **Total proposto** | **4 integrantes** | **240** | — | **R$ 25.200** |

Será utilizado software livre, sem previsão de despesas de viagem. Se o número de integrantes mudar, o esforço será recalculado por H = 60 × n, acompanhado de revisão do escopo e do preço. Valores contratuais, tributos e condições de pagamento dependeriam de formalização posterior.

## 6. Condições de execução e aceite

A BVE deverá disponibilizar dados e um interlocutor operacional até o fim da segunda semana. Lacunas serão registradas; hipóteses não verificáveis limitarão as conclusões. O aceite considerará rastreabilidade dos dados, reprodução dos experimentos, representação dos quatro processos e avaliação explícita da meta. A aprovação do modelo conceitual precederá a implementação. Esta minuta deverá ser confrontada com a carta-convite antes de sua emissão definitiva; após emitida, alterações comerciais serão formalizadas em nova proposta ou aditivo.

**Referência:** Costa, M. G.; Mesquita, M. A. (2023). *Minimizing total tardiness and makespan in ship fuelling operations in a maritime terminal*. Manuscrito disponibilizado na atividade.
