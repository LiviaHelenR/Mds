# Relatório de Análise de Fluxograma da IARA

**Data da análise:** (preencher)  
**Analistas:** Livia Helen e Wanderson De Paula  
**Objetivo:** Verificar se o comportamento da IA está de acordo com o fluxograma definido.

---

## 1. Introdução

Este relatório compara o comportamento real da IA IARA com o fluxograma definido no documento "Fluxos do IARA". Cada etapa do fluxo foi analisada para verificar sua conformidade.

---


## 2. Análise Etapa a Etapa

| Etapa / Decisão | Comportamento Esperado | Comportamento Observado | Status |
|-----------------|------------------------|-------------------------|--------|
| Envia mensagem<div>de recepção</div> | Apartir de qualquer mensagem de texto enviada pelo manifestante, a IARA deverá se apresentar formalmente e questionar se o manisfestante deseja se identificar ou continuar como anônimo. | Cumpriu com o comportamento esperado descrito no fluxograma.|  :white_check_mark: Conforme  ⬜ Parcial  ⬜ Não Conforme |
| Manifestante&nbsp;<div>deseja&nbsp;<span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">se identificar?</span></div> | Caso o manifestante deseje identificar-se, a IARA deverá solicitar o CPF do manifestante.Caso o manifestante deseje permanecer anônimo a IARA deveria pedir o número de processo ou protocolo da demanda,sem apresentar outras opções.| Não cumpriu por completo com o comportamento esperado descrito no Fluxograma.Tendo em vista que,no caso do manifestante escolher indentificar-se a IARA cumpriu com o comportamento esperado.Todavia,no caso no qual o manifestante deseja permanecer anônimo,o comportamento esperado não ocorreu. Pois a IARA direcionou o usuário para uma etapa em que são apresentadas duas opções: 1. Consultar demanda 2. Solicitar informações.Contudo após o usuário escolher o que deseja o fluxo correu normalmente.|:white_check_mark: Parcial  ⬜ Conforme   ⬜ Não Conforme |
| Solicita o CPF | Caso o manifestante escolheu a opções de se identificar, a IARA deverá solicitar seu CPF. | Cumpriu com o comportamento esperado,descrito no fluxograma.| :white_check_mark: Conforme  ⬜ Parcial  ⬜ Não Conforme |
| CPF é válido? | Após o manifestante enviar seu CPF,ela deve averiguar se é um CPF válido.Caso seja válido,seguimos para a próxima etapa.Caso não seja válido,primeiramente, ela deve comunicar ao manifestante que o CPF informado não é válido e solicitá-lo novamente para reanálise.Caso o novo CPF ainda seja inválido ela deve questionar se o manifestante  quer permanecer anônimo,se ele não quiser a IARA deve perguntar se ele quer ser encaminhado a um especialista.Caso não queira ser encaminhado, o atendimento é encerrado.Caso queira, em tese a IARA deveria encaminha-lo para um atendente,porém essa implementação ainda não foi feita porquê depende da integração com a G4flags.Por fim,caso o manifestante deseje permanecer anônimo após as tentativas falhas de informar o CPF, a IARA deveria  pedir o número de processo ou protocolo da demanda,sem apresentar outras opções.| Não cumpriu por completo com o comportamento esperado,descrito no fluxograma por alguns pequenos detalhes.Pois,no caso do manifestante desejar permanecer anônimo após as tentativas falhas de informar o CPF, a IARA deveria  pedir o número de processo ou protocolo da demanda,sem apresentar outras opções.Entretanto, a IARA direcionou o usuário para uma etapa em que são apresentadas duas opções: 1. Consultar demanda 2. Solicitar informações.Todavia, após o usuário escolher o que deseja o fluxo correu normalmente  | :white_check_mark: Parcial ⬜ Conforme   ⬜ Não Conforme |
| Verifica se o<div>manifestante já</div><div>está cadastrado</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Deseja ser<div>transferido para</div><div>um(a) especialista?</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Encerra o<div>atendimento</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Transfere<div>para</div><div>atendente</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante já<div>está cadastrado?</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Exibe dados do<br>manifestante | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante<div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">deseja alterar</span></div><div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">algum dado?</span></div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Suposição | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Rotina não testada | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| <b>Suposição</b> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante&nbsp;<span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">deseja</span><div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">consultar uma demanda</span></div><div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">já cadastrada?</span></div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante deseja<div>solicitar informações ou cadastrar uma nova demanda</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Exibe as 5 últimas demandas registradas no SISGEP vinculadas ao manifestante com os seus números de processo ou protocolo, nome do assunto, data e hora de inclusão do registro, excetuando as já<div>apresentadas</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante deseja<div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">encerrar a pesquisa?</span></div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Será que não seria melhor perguntar primeiramente se o manifestante tem um número de protocolo? (Wesla deve saber melhor) | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Pede o número<div>de processo</div><div>ou protocolo</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante ainda<div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">possui demandas</span></div><div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">vinculadas?</span></div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante deseja<div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">escolher uma das</span></div><div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">demandas exibidas?</span></div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Nº de processo ou<div>protocolo é válido?</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Processo de<div>encerramento</div><div>do atendimento</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Transferência<div>para atendente ainda&nbsp;</div><div>não implementado, pois depende da integração com a G4flags</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Processo ou ação | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Escolha do usuário | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Checagem interna | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Rotina definida | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Nota ou observação | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Processo tramita no SPU? | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Exibe: Nº de protocolo, data de cadastro, assunto, situação atual, órgão atual, setor atual, descrição e <i>última tramitação</i> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| O Porto tinha alguma ressalva sobre o campo <i>última tramitação</i> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante deseja<div><span style="background-color: transparent; color: light-dark(rgb(0, 0, 0), rgb(255, 255, 255));">algo mais?</span></div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| IARA pergunta como pode ajudá-lo | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Manifestante explica em linguagem natural a nova demanda ou a informação que busca | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| IARA busca e apresenta todos os modelos de atendimento que se assemelham à descrição feita pelo manifestante | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| A descrição se assemelha<div>a pelo menos um modelo de</div><div>atendimento?</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| IARA pede para o manifestante explicar de forma mais detalhada | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Procura exibir o modelo de atendimento de <b>reclamação não atendida</b> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Um dos modelos de<div>atendimento satisfaz</div><div>o manifestante?</div> | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| IARA busca e apresenta todos os modelos de atendimento que se assemelham à todas as descrições feitas pelo manifestante | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Executa o fluxo do modelo de atendimento escolhido | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Seria bom dar a opção para o manifestante poder reclamar que a demanda consultada não foi atendida | (descrever) | (descrever) | ⬜ Conforme / ⬜ Parcial / ⬜ Não Conforme |
| Processo de encerramento do atendimento | (descrever) | (descrever) | :white_check_mark: Conforme / ⬜ Parcial / [ ]  Não Conforme |

---

## 3. Pontos de Não Conformidade

(Listar aqui as etapas que não estão de acordo com o fluxograma, explicando os problemas.)

---

## 4. Recomendações

(Inserir sugestões de ajustes na IA para alinhar seu comportamento ao fluxograma.)

---

## 5. Conclusão

(Resumo final da análise, destacando se a IA está majoritariamente conforme ou se necessita de revisões significativas.)

---
