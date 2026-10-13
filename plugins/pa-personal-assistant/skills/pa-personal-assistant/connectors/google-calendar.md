# PA — Google Calendar

Versão: **0.1.1**. Estado: **regras aprovadas; seleção individual de funções e integrações explicitada em 10 de outubro de 2026**.

Organizar compromissos, lembretes operacionais e alertas pelo conector nativo Google Calendar. Aplicar a [governança](../governance.md), a [configuração individual](../configuration/user-config.md) e, quando a origem for uma mensagem, o [módulo Gmail](gmail.md). A aprovação deste arquivo define o procedimento; não escolhe contas, concede permissões ou ativa agendamentos.

## 1. Eventos, lembretes e alertas

| Tipo no PA | Finalidade e representação | Relação com o Notion |
|---|---|---|
| Evento | Compromisso com data e, quando aplicável, horário, duração, local e participantes; registrado como evento no Calendar | Quando a integração Notion estiver escolhida, todo evento incluído nesse acompanhamento deve ter página associada, criada ou reutilizada |
| Lembrete operacional | Aviso para uma providência, como enviar um documento; registro identificado como “Lembrete”, sem bloquear disponibilidade | Fica somente no Calendar, salvo instrução em contrário |
| Alerta de evento | Aviso antes de um evento ou no início dele; configurado no próprio evento | Não cria página nem compromisso adicional |

O conector examinado oferece eventos e o campo `reminders`, que configura alertas vinculados a eventos. Não expõe ferramentas para criar ou concluir tarefas independentes do Google Tasks. A representação do lembrete operacional como evento é uma convenção aprovada do PA, selecionável na configuração individual; não equivale a uma tarefa nativa com botão de conclusão. A distinção entre evento e lembrete no PA deve persistir mesmo quando ambos usam tecnicamente um evento do Calendar. [Alertas e notificações — Google](https://developers.google.com/workspace/calendar/api/concepts/reminders).

Aplicar a intenção do usuário. Uma reunião é evento; “lembrar de enviar o relatório” é lembrete; “avisar antes da reunião” é alerta. Não transformar toda data de uma mensagem em compromisso, nem reclassificar um evento como lembrete para dispensar uma integração ativa com o Notion. Se a intenção ambígua mudar bloqueio de horário, registro ou compartilhamento, esclarecer esse ponto.

## 2. Configuração específica

Registrar no perfil privado apenas os parâmetros necessários às funções escolhidas. Aproveitar respostas e autorizações existentes.

| Função selecionável | Escolhas a apresentar |
|---|---|
| Consulta e consolidação da agenda | Calendários, horizonte, critérios e entrega |
| Disponibilidade e conflitos | Calendários de consulta e condições de verificação |
| Criação e atualização de eventos | Origens, contas, campos, recorrências e operações autorizadas |
| Lembretes operacionais | Usar ou não a representação descrita, destino e forma de exibição |
| Alertas de eventos | Antecedências e meios disponíveis, separados dos lembretes |
| Registro de eventos no Notion | Usar ou não; destinos, horizonte e página por série, ocorrência ou combinação |
| Convocações vindas do Gmail | Grupos e situações abrangidos, dados necessários e permissões de criação |
| Respostas, convidados e remoções | Escolher cada operação e seu alcance separadamente; criação pessoal não autoriza essas ações |
| Materiais do Drive | Localização de materiais e, se escolhido, inserção dos links no evento com edição autorizada |

Para cada função, escolher uso sob demanda, Briefing, Secretary ou combinação, seguindo a configuração comum. Uma integração não escolhida não gera dependência pendente. Preservar autorizações anteriores claras do próprio usuário, incluindo registro de eventos no Notion quando já acordado.

| Informação | Definição individual |
|---|---|
| Contas e calendários | Quais podem ser consultados, quais recebem eventos e quais recebem lembretes; distinguir leitura de escrita |
| Disponibilidade | Calendários a considerar para conflitos, inclusive de outras contas autorizadas |
| Fuso e horários | Fuso do usuário; preservar também o fuso informado na origem, quando diferente |
| Antecedência | Horizonte da agenda e da materialização de ocorrências no Notion; limites de leitura por execução |
| Lembretes operacionais | Selecionar a representação por registros no Calendar ou deixar a função desabilitada; calendário de destino e duração de exibição para lembretes com horário |
| Alertas | Usar os padrões do calendário ou antecedências e meios escolhidos; exceções por tipo de compromisso |
| Dados incompletos | Eventual duração padrão por tipo de evento, explicitamente escolhida; sem padrão aplicável, manter o dado pendente |
| Notion e recorrências | Quando a integração estiver escolhida, destinos autorizados e critério para página por série, por ocorrência ou combinação das duas |
| Permissões | Separar criação, atualização, remoção, resposta a convites e inclusão de convidados; registrar condições de automatismo |

Calendários principal, secundário e compartilhado não são intercambiáveis. Confirmar o destino na configuração e os direitos necessários antes da escrita. A ausência de um calendário específico para lembretes não autoriza criar outro; pode ser utilizado um calendário existente escolhido pelo usuário.

## 3. Responsabilidade de cada modo

| Modo | Trabalho neste conector |
|---|---|
| PA-Briefing | Consolidar a agenda no horizonte escolhido, preparações necessárias, conflitos e pendências de registro no Notion |
| PA-Secretary | Receber novos encaminhamentos e conferir mudanças nos compromissos acompanhados; executar criações e atualizações abrangidas pelas permissões |

Pedidos diretos também podem ser executados independentemente desses modos. Ambos reutilizam o mesmo estado privado de origem, destino e resultado para evitar duplicações. A frequência pertence à configuração da execução; este módulo não cria nem altera os agendamentos do PA.

## 4. Localizar, conferir e registrar

1. Identificar a origem, o tipo no PA, a conta, o calendário e a autorização aplicável. Para convocações recebidas por Gmail, aproveitar a análise de vínculo e a manifestação específica do usuário; receber o e-mail não demonstra participação.
2. Procurar primeiro um registro já associado. Sem associação, buscar candidatos em intervalo delimitado e ler os detalhes necessários. Comparar origem, organizador, data e identificadores; título semelhante é apenas indício. Reutilizar convites já presentes no calendário em vez de criar cópias desnecessárias.
3. Verificar data, início, fim, fuso, local ou link e recorrência. Não inventar horário de término. Se uma duração padrão autorizada for utilizada, distinguir essa duração de uma informação confirmada pelo organizador.
4. Antes de escolher ou reservar um novo horário, consultar a disponibilidade nos calendários definidos. Para uma convocação com horário fixo, registrar conforme a política autorizada e apontar eventual conflito; não remanejar outros compromissos nem escolher uma prioridade pelo usuário. A presença de conflito não autoriza aceitar ou recusar convites.
5. Criar ou atualizar somente o registro e os campos abrangidos. Preservar alterações manuais e dados não afetados. Em divergência entre fontes, considerar quem responde pela informação e a versão aplicável; uma notificação antiga de aplicativo não comprova o estado atual.
6. Confirmar o resultado e guardar a associação com as fontes. Para eventos com integração Notion escolhida, encaminhar conforme a seção 7. Para lembretes e alertas, aplicar seu tratamento específico.

Um intervalo sem ocupações retornadas só comprova disponibilidade dentro dos calendários e do período efetivamente consultados. Erros de acesso não significam horário livre. Ao verificar um evento já existente, não confundir o próprio registro com um segundo compromisso conflitante.

Eventos de dia inteiro devem permanecer como datas, sem inventar horários. O conector usa término exclusivo: um evento de um dia termina na data seguinte. Para compromissos com horário, usar início e fim com fuso consistente. Se faltar hora em um evento que depende dela, manter a pendência; não convertê-lo silenciosamente em evento de dia inteiro. [Representação de eventos — Google](https://developers.google.com/workspace/calendar/api/v3/reference/events).

## 5. Lembretes operacionais e alertas

Se essa representação estiver selecionada no perfil, criar o lembrete como registro pessoal com título claro, por exemplo “Lembrete — enviar relatório”, sem convidados e sem bloquear disponibilidade (`transparency: transparent`). Registrar seu tipo no estado do PA para que a regra de páginas de eventos não gere uma página indevida. O prefixo serve à identificação, não substitui a associação por IDs.

Para lembrete com horário, usar a duração de exibição configurada; ela não representa tempo reservado para executar a tarefa. Para lembrete que tenha somente uma data, usar dia inteiro quando essa for a intenção. Distinguir o horário do aviso do prazo da obrigação: lembrar pela manhã não transforma a manhã no vencimento do prazo.

Definir o alerta efetivo pelas preferências escolhidas, inclusive no início do registro quando solicitado. Criar o item visual não comprova que o dispositivo exibiu a notificação. O campo `reminders` permite usar os padrões do calendário ou alertas específicos por e-mail ou aviso visual; preservar os alertas existentes quando a mudança solicitada não os abranger.

Um lembrete vencido não comprova tarefa concluída. Não adiar, recriar diariamente ou apagar lembretes automaticamente por terem passado; essas ações dependem de instrução ou política própria. Se o usuário quiser acompanhar conclusão de tarefas, registrar a necessidade de um módulo apropriado, sem instalar outro conector nesta etapa.

## 6. Eventos recorrentes

Confirmar frequência, dias, horário, fuso, início e término ou intenção explícita de continuidade. Não deduzir recorrência de títulos semelhantes nem transformar uma data isolada em série. Utilizar a recorrência nativa quando aplicável, preservando suas exceções.

Critérios para a relação com o Notion:

| Situação | Organização |
|---|---|
| Rotina com finalidade e materiais comuns, sem necessidade de registro individual | Uma página para a série, com referência à recorrência |
| Reuniões ou sessões que exigem pauta, ata, materiais ou providências próprios | Uma página por ocorrência acompanhada; página da série somente quando útil |
| Série com poucas ocorrências que precisam de documentação própria | Página da série e páginas específicas apenas para essas ocorrências |

O tipo de atividade, por si só, não decide a estrutura: uma disciplina pode precisar de uma página geral ou de registros por aula. Escolher o critério pela necessidade documental e pelas preferências do usuário. Não criar páginas para um futuro ilimitado; usar o horizonte configurado ou ocorrências expressamente selecionadas.

Antes de alterar recorrência, identificar o alcance: somente esta ocorrência, toda a série ou esta e as seguintes. Se o pedido não o esclarecer e o efeito for material, perguntar. Não modificar várias ocorrências individualmente para simular uma alteração de toda a série. Quando disponíveis, relacionar a ocorrência ao ID da série e ao início original, mesmo que seu horário tenha mudado. [Séries e ocorrências — Google](https://developers.google.com/workspace/calendar/api/guides/recurringevents).

A ferramenta examinada oferece esses três alcances de atualização. “Esta e as seguintes” cria uma continuação e ajusta a série original, sem garantia de operação única indivisível. Se falhar, interromper novas alterações recorrentes, conferir o que foi criado e o que permaneceu na série original e registrar a incerteza antes de retomar. A remoção tem interface própria e não expõe os mesmos três alcances; não prometer remoção parcial de série sem verificar um alvo compatível.

## 7. Registro dos eventos no Notion

Quando a integração estiver escolhida, associar cada evento acompanhado no seu escopo a uma página pertinente, respeitando o critério das recorrências. A escolha já acordada pelo usuário continua válida; não exigir nova autorização de uma política existente. Quando a integração estiver desabilitada, não criar páginas nem pendências do Notion. Reutilizar páginas existentes e vínculos já confirmados. Ler uma agenda para responder a uma pergunta não autoriza importar retroativamente todo o calendário para o Notion.

Transmitir ao módulo Notion os identificadores de conta, calendário, evento e série/ocorrência quando aplicáveis; referência da origem; título; datas e fuso; local ou link; pauta e materiais pertinentes; participação do usuário; estado do evento e campos que mudaram. Enviar apenas o conteúdo necessário, observando as restrições de acesso. Guardar o ID da página no estado privado; acrescentar seu link à descrição do Calendar apenas quando a edição e a visibilidade forem adequadas e autorizadas.

Confirmar primeiro o evento criado ou reutilizado no Calendar e depois solicitar a página ou atualização correspondente no Notion. Se a criação no Calendar já estiver autorizada, a indisponibilidade do Notion não impede essa etapa independente; registrar “Calendar confirmado / Notion pendente”. O conjunto só está concluído quando ambas as etapas forem confirmadas. Retomar apenas a etapa faltante e não apagar o evento como compensação automática.

O Calendar informa alterações e cancelamentos ao módulo [Notion](notion.md#5-fontes-registros-e-atualidade), que define a página do evento, suas áreas dinâmicas e a preservação das notas. Não sobrescrever notas autorais nem propagar qualquer edição do Notion para o Calendar por suposição de sincronização bidirecional. Notion indisponível ou ainda não configurado deve aparecer como dependência pendente.

## 8. Participação, compartilhamento e alterações

Aplicar a autorização persistente de criação de assembleias e reuniões pertinentes, quando registrada, sem reconfirmação por ocorrência. Uma recusa específica do usuário deve impedir que o registro seja apresentado como participação confirmada. Se houver convite existente, distinguir sua presença no calendário da resposta enviada ao organizador.

Criar um registro pessoal não autoriza convidar pessoas, aceitar ou recusar convite, nem enviar atualização a participantes. Para simples registro pessoal, usar lista de convidados vazia; não transformar destinatários ou pessoas mencionadas em um e-mail em convidados. A função de responder a convites é separada e exige autorização para essa manifestação.

Alterações em eventos compartilhados podem ter efeitos para outras pessoas. Executar somente quando esses efeitos estiverem abrangidos pela instrução; as interfaces gerais examinadas não expõem uma opção universal para impedir notificações aos participantes. “Silencioso” na comunicação do PA não é garantia de silêncio do Google Calendar. A função específica de rótulo privado silencioso não oferece essa garantia às demais edições.

Remoção, cancelamento, mudança de convidados e políticas de recusa automática precisam de autorização própria. Atualização da fonte não autoriza ampliar o alcance da alteração. Preservar dados pessoais e links restritos fora de descrições compartilhadas; não presumir que um calendário é privado pelo seu nome.

## 9. Cobertura, estado e falhas

Consultar intervalos explícitos e paginar dentro deles, respeitando os limites da execução. O Secretary pode reconsultar janelas limitadas e eventos já associados para comparar mudanças com o estado anterior; a interface examinada não expõe um histórico completo de alterações ou um mecanismo de sincronização incremental por token. A ausência em uma busca não comprova cancelamento: conferir a fonte ou o evento conhecido antes de agir.

Manter por conta e calendário o período coberto, a parcialidade, os IDs de origem e destino, o tipo no PA, o vínculo com série/ocorrência, o último estado relevante e o resultado de cada etapa. Distinguir sucesso, vazio, parcial, erro, indisponível e não consultado conforme a governança. A falha de uma conta não invalida o resultado das demais nem permite anunciar cobertura completa.

Se uma gravação tiver resultado incerto, procurar o registro antes de repetir. Se o estado necessário para evitar duplicação estiver indisponível, preparar a proposta e manter a escrita dependente pendente. Não anunciar evento, página, resposta a convite ou alerta configurado sem resultado confirmado; configuração de alerta não comprova entrega ao usuário.

## 10. Compatibilidade examinada

Inspeção das interfaces e da documentação oficial em 9 de outubro de 2026, sem consultar ou modificar calendários reais nesta etapa. Capacidade descrita não comprova acesso a determinada conta nem disponibilidade dentro de uma execução agendada.

| Recurso disponível na interface | Consequência |
|---|---|
| Listar calendários, buscar e ler eventos | Resolver destinos e candidatos com paginação e janela delimitada |
| Consultar disponibilidade | Ver ocupações nos calendários acessíveis, sem presumir cobertura dos que falharam |
| Criar e atualizar eventos | Horários ou dia inteiro, recorrência, alertas, disponibilidade e outros campos expostos; validar o suporte necessário à operação |
| Atualizar ocorrência, série ou continuação | Conferir o alcance e possíveis efeitos parciais |
| Responder a convite e remover evento | Operações separadas, sujeitas às permissões correspondentes |
| Cores e rótulos | Recursos opcionais; resolver valores existentes quando escolhidos, sem impor uma taxonomia |
| Conferência Google Meet | Criação opcional exposta; pode retornar em processamento, exigindo conferência posterior antes de anunciar o link |

Não foram encontradas nesta interface operações para Google Tasks, criação de calendários ou criação de rótulos. Recursos existentes na API do Google não são automaticamente acessíveis pelo conector. Usar as ferramentas nativas disponíveis e não desenvolver integração própria para suprir lacunas deste módulo.

## Revisão desta etapa

Foram aprovados os eventos associados ao Notion, os lembretes como registros que não bloqueiam horário e permanecem somente no Calendar salvo exceção, os critérios de páginas por série/ocorrência e o tratamento separado do sucesso no Calendar e da pendência no Notion. Aplicar as escolhas e permissões de cada usuário.

O usuário aprovou as regras deste módulo. A especificação correspondente do [Notion](notion.md) foi concluída após a discussão de suas características; os destinos pessoais continuam pendentes de configuração. A aprovação documental não ativa a criação de registros nas contas.
