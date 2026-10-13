# PA — Encaminhamento conforme horários

Versão: **1.0.0**, de **12 de outubro de 2026**. Estado: **procedimento especificado; execução integrada ainda não validada**.

Usar somente quando o pedido for executar as funções devidas conforme a programação privada. O agendador externo inicia cada execução; o PA consulta o horário, as escolhas e o estado para decidir o trabalho daquela chamada. A habilidade não desperta sozinha, não fica continuamente ligada e não cria tarefas como efeito deste procedimento. Aplicar a [governança](../governance.md).

## 1. Duas formas de acionar o mesmo PA

| Configuração | Responsabilidade do agendador | Responsabilidade do PA |
|---|---|---|
| Funções explícitas por tarefa | Iniciar nos horários escolhidos com um pedido como “pesquisa acadêmica e oportunidades” | Executar somente as funções pedidas e configuradas |
| Um acionamento periódico com encaminhamento | Iniciar o PA na cadência escolhida | Identificar funções devidas e pendências elegíveis no instante da chamada |

Ambas usam a mesma habilidade e os mesmos módulos. O usuário escolhe a forma; ela não deve restringir o uso manual. Uma função pode ter ritmo diário e outra diversas execuções na mesma janela, sem reconstruir seus procedimentos.

Um pedido manual explícito como “execute agora a pesquisa acadêmica” não deve ser recusado porque chegou fora do horário. Aplicar o escopo pontual; não marcar automaticamente uma ocorrência agendada como entregue, salvo se a instrução ou a política de reaproveitamento abranger essa substituição. Um pedido explícito a funções determinadas não dispara o encaminhamento geral.

## 2. Configuração necessária

Registrar privadamente, em conversa e sem exigir códigos do usuário:

| Campo | Conteúdo |
|---|---|
| Forma de acionamento | Tarefas com funções explícitas ou encaminhamento periódico |
| Fuso | Referência inequívoca do perfil; horário de verão quando aplicável |
| Por função | Ativada ou não; dias; horário ou janela; frequência dentro da janela; destino e permissões já escolhidos |
| Limites da janela | Definir se o horário final inclui uma última ocorrência; janela não significa monitoramento contínuo |
| Instante desejado | Início do trabalho ou expectativa de resultado pronto; entrega exige considerar a duração |
| Atrasos e ausências | Tolerância; recuperar, consolidar ou registrar ocorrência perdida; limite de recuperação |
| Ordem de trabalho | Prioridade entre funções simultaneamente devidas e orçamento suficiente para leituras longas |
| Continuidade | Local do perfil e do estado, identidade por ocorrência e coordenação de execuções |
| Agendador efetivo | Cadência e minuto de início, ambiente, ferramentas disponíveis e entrega/notificação verificadas |

Horários de exemplo não são escolhas pessoais nem regras do pacote. Uma janela entre dois horários precisa também de uma frequência de consulta. Usar um único acionamento é opção de configuração; não reinterpretar tarefas já existentes ou duplicar seu trabalho sem conciliação autorizada.

## 3. Escolha das funções em cada chamada

1. Identificar o perfil, sua versão, a origem da chamada e o estado vigente. Obter o instante atual de fonte confiável do ambiente ou ferramenta de relógio e convertê-lo para o fuso configurado. Não usar a data escrita no documento, o horário de publicação de uma página ou uma lembrança da conversa como relógio. Se não houver hora confiável, não inventar quais ocorrências estão devidas.
2. Determinar ocorrências cujo início previsto já passou e cuja janela de execução ou recuperação ainda permite trabalho. Comparar intervalos e tolerâncias; não exigir igualdade exata entre hora real e horário previsto. Não executar antecipadamente uma ocorrência futura.
3. Consultar a identidade de cada ocorrência: perfil, função, data e instante previsto com fuso. Se já concluída, não repetir; se parcial, retomar somente o necessário; se execução anterior ainda estiver ativa ou seu efeito for incerto, aplicar a coordenação e verificação da governança. Um campo “em execução” não constitui trava real.
4. Carregar apenas os módulos devidos. Ordenar segundo as escolhas de prioridade, tempo disponível e pendências. Falha em uma função não impede outras independentes. Leitura longa não deve apagar nem marcar como concluídas as funções que ficaram pendentes.
5. Registrar resultado por função e ocorrência, etapas confirmadas, cobertura, pendências e entrega. Marcar conclusão apenas no alcance comprovado. Persistir o necessário antes de tratar a próxima chamada como continuação.
6. Se nada estiver devido, encerrar sem pesquisas, varreduras de contas ou relatório substantivo. Aplicar a política de notificações disponível no agendador; não prometer que uma resposta vazia suprime avisos da plataforma.

Se faltarem perfil, relógio ou estado necessários, registrar o impedimento de encaminhamento sem presumir consentimento ou última execução. O trabalho pontual independente expressamente pedido pode continuar. Após interrupção longa, seguir a política de recuperação; não disparar automaticamente uma execução para cada hora perdida.

Mudança de fuso, horário de verão, versão da programação ou relógio regressivo exige preservar a identidade das ocorrências e evitar duplicação. Não usar apenas “dia do mês” ou a hora isolada como chave. Uma nova configuração não torna concluído um trabalho anterior nem reabre por si só ocorrências já entregues.

## 4. Cadência, horários e custo

A frequência do acionamento determina a resolução temporal. Se o agendador chama às 10h, 11h e 12h, o PA não recebe uma chamada às 10h30. Pode recuperar o trabalho às 11h somente se isso estiver previsto na tolerância escolhida; não deve esperar dentro de uma execução até 10h30 ou criar outra tarefa para esconder essa diferença.

| Objetivo ilustrativo | Alternativa a verificar |
|---|---|
| Todas as funções em horas inteiras compatíveis | Um acionamento por hora pode ser suficiente |
| Atender tanto 10h quanto 10h30 | Um acionamento a cada 30 minutos, ou recorrência que inclua ambos os instantes, se suportada |
| Evitar chamadas sem trabalho e preservar minutos diferentes | Tarefas separadas para funções ou grupos com a mesma frequência |
| Pesquisa longa sem atrasar acompanhamento frequente | Orçamento e ordem adequados, ou separação em tarefas quando o ambiente não oferecer isolamento suficiente |

Uma tarefa horária ao longo de 24 horas corresponde nominalmente a 24 chamadas diárias; a cada 30 minutos, a 48. Restringir a uma janela reduz chamadas conforme seus limites. Economizar espaços de agendamento não significa economizar execuções ou cotas: até uma chamada que só decide encerrar pode consumir recursos. Não fixar consumo ou quantidade de tarefas permitidas sem verificar as condições da conta.

O horário de uma ocorrência indica normalmente início solicitado, não garantia de que as leituras configuradas estarão concluídas e entregues naquele minuto. Ajustar a expectativa e a política de entrega com o usuário. Atrasos, duração, sobreposição e limites devem ser observados em teste, não inferidos do texto da habilidade.

## 5. Compatibilidade e implantação

A [documentação oficial de agendamentos](https://learn.chatgpt.com/docs/automations), consultada em 12 de outubro de 2026, descreve uso de skills por tarefas e intervalos em minutos para tarefas dentro de chats. Isso sustenta a possibilidade de acionar o PA periodicamente. A seleção por horário e o controle de ocorrências aqui descritos são um projeto do PA; a documentação não certifica sua execução integrada.

Verificar no ambiente escolhido: disponibilidade da skill, acesso ao perfil e ao estado, relógio, fontes, permissões, cadência pretendida, notificações e comportamento em sobreposição. Para independência do computador, não depender de arquivos que só existem localmente. Configuração de horário não dispensa autorização das ações de cada função.

Antes de ativar, experimentar chamadas com: nenhuma função devida; duas funções simultâneas; atraso tolerado; atraso além da janela; repetição após entrega; estado inacessível; execução anterior em andamento; virada do dia; mudança de fuso; leitura que ultrapassa o intervalo; e acionamento manual fora do horário. Conferir a primeira execução real e seus efeitos antes de declarar a rotina operacional.

Modelos de pedido, depois de preencher e verificar as referências privadas:

- **Encaminhamento periódico:** “Use o PA conforme minha programação individual. Confira o horário atual no meu fuso e o estado persistente; execute somente as funções devidas ou pendências elegíveis. Não repita ocorrências concluídas. Se nada estiver devido, encerre conforme minha política de notificações. Registre cobertura, resultados e pendências. Não crie nem altere agendamentos.”
- **Funções explícitas:** “Use o PA para executar pesquisa acadêmica e oportunidades conforme meu perfil. Produza os resultados próprios de cada função, aproveitando o estado existente. Não execute Briefing ou Secretary por consequência e não altere agendamentos.”

Estes textos não são agendamentos criados. Criar, alterar ou substituir tarefas depende de instrução específica; preservar as existentes durante desenvolvimento e revisão documental.
