# PA — Briefing

Versão: **1.2.0**. Estado: **especificação concluída em 12 de outubro de 2026; composição e execução configuráveis**.

Consolidar informações, compromissos e prioridades selecionados pelo usuário em um resultado legível e verificável. Aplicar a [governança](governance.md), o [perfil individual](configuration/user-config.md) e apenas os módulos pertinentes. Uma execução manual produz o briefing solicitado; não cria uma rotina.

## 1. Catálogo e escolhas

| Bloco ou função selecionável | O que configurar |
|---|---|
| Prioridades do período | Prioridades fixadas pelo usuário, critérios de sugestão e quantidade de destaques |
| Agenda e preparação | Calendários, horizonte, conflitos e materiais necessários |
| Correspondência e obrigações | Contas, escopos e assuntos relevantes no Gmail |
| Higienização do Gmail | Janela de 30 dias quando escolhida, frequência e operações autorizadas |
| Projetos e pendências | Recursos mapeados, fontes de estado, critérios de relevância e próximos passos |
| Oportunidades acadêmicas | Tipos, fontes, prazos e seleção conforme módulo próprio |
| Notícias | Temas, fontes, período e profundidade da pesquisa escolhida |
| Referência à pesquisa acadêmica | Link ou síntese breve do resultado próprio; incluir monitoramento neste fluxo somente se escolhido |
| Mudanças e materiais do Drive | Pastas, projetos, documentos e funções selecionadas |
| Dashboard e histórico no Notion | Destinos, regiões dinâmicas, retenção e operações permitidas |
| Decisões e falhas relevantes | Forma de agrupar aprovações pendentes e limitações de cobertura |

Escolher composição, ordem, extensão, dias e horários, fuso, horizonte de cada bloco, destino, notificações e política para períodos sem novidade. Não exigir todos os blocos. Horário e frequência do briefing não tornam diária toda busca: cada fonte tem sua cadência e limite próprios.

O perfil deve registrar limites proporcionais de tempo, consultas e volume por execução, ou uma política de uso do ambiente que os determine. Enquanto faltarem parâmetros para execução recorrente, concluir consultas pontuais delimitadas e manter a rotina por configurar. Não escolher um orçamento ilimitado nem um teto numérico sem base.

## 2. Preparação da execução

Identificar perfil e permissões vigentes, modo, instante da execução, fuso e intervalo do relatório. Separar intervalo de novidades, horizonte futuro da agenda, janela de higienização e datas de atualização de pesquisas menos frequentes.

Carregar o estado comum quando necessário à continuidade e às alterações. Verificar as pendências anteriores, os resultados confirmados da Secretary e a responsabilidade de escrita de cada operação. Reutilizar consultas atuais no alcance coberto; revalidar dados materiais à ação, como remarcação de compromisso ou prazo prestes a vencer.

Se perfil, estado ou recurso estiver inacessível, limitar o efeito à função afetada conforme a governança. Não supor permissões ou marcos de outra conversa. Fontes desabilitadas ficam fora da rotina; fontes escolhidas mas não consultadas devem manter seu estado real.

## 3. Coleta e encaminhamentos

| Conteúdo | Procedimento responsável |
|---|---|
| E-mails e listas | [Gmail](connectors/gmail.md): leitura progressiva, obrigações e arquivamento seletivo |
| Eventos e lembretes | [Calendar](connectors/google-calendar.md): agenda, conflitos, tipos e recorrências |
| Prioridades, projetos e notas | [Notion](connectors/notion.md): campos mapeados, conteúdo protegido e biblioteca |
| Arquivos e documentos | [Drive](connectors/google-drive.md): metadados, leitura e funções escolhidas |
| Chamadas e seleções | [Oportunidades acadêmicas](modules/academic-opportunities.md): evidência, elegibilidade e prazos |
| Notícias e páginas | [Pesquisa web](connectors/web-research.md): atualidade, procedência e cobertura |
| Resultado de pesquisa e artigos | [Pesquisa acadêmica](modules/literature-watch.md): função independente; reutilizar seu resultado quando a integração estiver escolhida |

Quando a higienização estiver selecionada, revisar os últimos 30 dias conforme o Gmail, reutilizando leituras válidas e reavaliando vencimentos e alterações. Não reduzir essa tarefa às mensagens novas desde a Secretary. Obrigações abertas continuam acompanhadas quando saem da janela. Spam e Lixeira só entram na revisão específica escolhida; não são escopo implícito de limpeza.

Executar alterações apenas quando houver função escolhida, dados suficientes, autorização aplicável e coordenação de escrita. Isso inclui o arquivamento seletivo e o registro de convocações abrangidos por políticas persistentes. Uma operação automática autorizada não precisa de nova confirmação rotineira. Se o Briefing não for o executor designado, preparar ou reutilizar o encaminhamento durável para esse fluxo, sem executá-lo em duplicidade.

Eventos acompanhados recebem registro no Notion quando a integração estiver escolhida, com tratamento de recorrência do Calendar. Lembretes operacionais ficam no Calendar salvo opção expressa. Separar o sucesso de cada serviço e retomar somente a parte pendente.

A pesquisa acadêmica tem acionamento e relatório próprios. Executar o Briefing não inicia por consequência o estudo de verbete, o panorama de periódicos ou as leituras longas. Se a integração estiver escolhida, incluir link ou síntese breve do resultado já produzido com sua data e cobertura. Só executar a pesquisa neste mesmo fluxo quando isso estiver explicitamente configurado, aplicando seu módulo e evitando duplicação. Preservar configurações anteriores de outros usuários que já tenham escolhido pesquisa dentro do Briefing; a nova função não migra rotinas por conta própria.

## 4. Síntese e apresentação

Como proposta de organização, oferecer: prioridades fixadas e sugestões justificadas; agenda e preparação; decisões e prazos; novidades dos blocos escolhidos; cobertura e pendências. A ordem final pertence ao usuário. Respeitar as características do dashboard quando ele for o destino.

Cada destaque deve responder, no nível de detalhe escolhido: o que importa, por que importa, data ou prazo, estado conhecido, próxima ação possível e fonte. Vincular o registro de origem ou destino confirmado. Não reproduzir mensagens inteiras ou notas de leitura no briefing quando uma síntese com link resolver.

Proteger a diferença entre prioridade escolhida pelo usuário e prioridade sugerida pelo PA. Não mudar uma decisão pessoal ou compromisso por inferência de urgência. Um prazo vencido pode representar pendência aberta; não o tratar automaticamente como trabalho concluído.

Agrupar o mesmo item recebido por fontes diferentes e conciliar divergências relevantes. Distinguir novidade, atualização de item conhecido, lembrete programado e ação já realizada. Algo avisado pela Secretary pode constar na visão consolidada, mas deve aparecer como já comunicado, sem novo alerta urgente pelo mesmo fato.

Não preencher blocos vazios com recomendações genéricas. Informar ausência de itens no escopo efetivamente consultado quando isso ajudar a interpretar o resultado. Identificar dados reutilizados de uma consulta anterior e sua atualidade, sem apresentá-los como verificados agora.

## 5. Entrega, histórico e conclusão

Entregar no destino escolhido. Atualizar somente regiões e campos autorizados do Notion e aplicar sua política de retenção. O resultado atual, o histórico conservado e o estado para retomada têm funções distintas; salvar um não confirma os demais.

Registrar separadamente conteúdo preparado, gravação confirmada, entrega ou notificação confirmada e etapas pendentes. Usar uma identidade de resultado por perfil, período e destino para reconhecer uma reexecução. Não tratar confirmação de gravação como prova de notificação entregue.

Aplicar a política escolhida para briefing sem novidades: resumo mínimo, apenas atualização do destino ou ausência de notificação. A Secretary silenciosa não impõe silêncio ao briefing diário, nem o contrário. Quando notificações forem controladas pelo agendador, conferir suas capacidades antes de prometer supressão de avisos.

O relatório deve permitir reconhecer a cobertura das fontes selecionadas, com estados da governança e limites materiais. Um briefing útil pode ter cobertura parcial; não chamar essa execução de completa. A execução está concluída no alcance informado quando o resultado e os efeitos anunciados estiverem confirmados e suas pendências estiverem preservadas.

## 6. Verificação antes da ativação

Validar composição escolhida, reutilização de dados, janela de 30 dias, obrigação antiga ainda aberta, conta indisponível, mudança de data, integração desabilitada, preservação de prioridades humanas e reexecução sem duplicação. Verificar também entrega parcial e falha de notificação após gravação bem-sucedida. Testar somente operações e alvos autorizados.

Importar instruções anteriores do usuário somente quando forem fornecidas ou estiverem acessíveis no contexto autorizado, comparando seu alcance com as escolhas atuais. Não presumir conteúdo de anexos ou conversas não consultados.
