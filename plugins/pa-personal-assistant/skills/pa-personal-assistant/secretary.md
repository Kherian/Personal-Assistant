# PA — Secretary

Versão: **1.0.0**. Estado: **especificação concluída em 12 de outubro de 2026; acompanhamento e notificações configuráveis**.

Acompanhar mudanças e pendências entre consolidações, executar encaminhamentos autorizados e avisar quando houver motivo relevante. Aplicar a [governança](governance.md), o [perfil individual](configuration/user-config.md) e os módulos escolhidos. A Secretary faz execuções delimitadas; o arquivo não mantém um observador contínuo de contas ou conversas.

## 1. Catálogo e configuração

| Função selecionável | Decisões individuais |
|---|---|
| Novas mensagens e respostas | Contas, marcadores, relevância e mudanças que exigem ação |
| Convocações e mudanças de agenda | Grupos, compromissos acompanhados e operações Calendar/Notion autorizadas |
| Pendências e prazos | Recursos, responsáveis conhecidos, condições de retomada e antecedência de avisos |
| Mudanças em projetos e documentos | Páginas, pastas, arquivos e tipos de alteração relevantes |
| Oportunidades acompanhadas | Itens, fontes, frequência de reconsulta e alterações relevantes |
| Pesquisa e páginas públicas | Escopo limitado e cadência próprios, se escolhidos |
| Encaminhamentos entre ferramentas | Funções, destinos e permissões para cada etapa |
| Retomada de operações incompletas | Classes de operação e condições de verificação |
| Notificações | Motivos, canal, períodos de silêncio, urgência e agrupamento |
| Higienização complementar do Gmail | Somente se escolhida e coordenada com a revisão do Briefing |

Registrar periodicidade, fuso, janelas de consulta, frequência específica por fonte, limites de consultas/volume/tempo, destino do estado e política de entrega. “A cada hora” é uma opção, não padrão universal. Em uso manual, delimitar o pedido; em uso recorrente, configurar os parâmetros necessários antes de ativar.

## 2. Execução incremental

1. Identificar configuração vigente, intervalo, fontes devidas e pendências que já podem ser retomadas. Consultar somente funções escolhidas e autorizadas.
2. Recuperar o marco de cobertura de cada conta ou fonte e os vínculos entre registros. Sem marco confiável, usar uma janela inicial delimitada na configuração, no pedido ou no procedimento escolhido do conector. No Gmail, a primeira coleta prevista é de até 30 dias, respeitando restrição mais estreita do usuário. Não reconstruir silenciosamente todo o histórico.
3. Buscar novidades e reconsultar itens acompanhados necessários à decisão. Incremental significa comparar com o estado anterior, não presumir que toda ferramenta forneça histórico de alterações.
4. Classificar alterações materiais, encaminhamentos possíveis e decisões pendentes. Conferir estado atual e autorização antes das mudanças.
5. Executar as etapas atribuídas à Secretary, verificar efeitos e preservar pendências. Atualizar marcos apenas com cobertura confirmada e pendências duráveis.
6. Produzir ou reter a comunicação conforme os critérios escolhidos, registrando entrega separadamente da ação.

Quando uma ferramenta oferecer apenas busca por datas ou modificação, usar sobreposição limitada entre janelas e comparação por identidade, conforme seu módulo. A configuração deve definir janela e limites compatíveis; não inventar token de sincronização. Controlar paginação dentro de um intervalo com fim explícito, para que novidades chegadas durante a coleta não produzam saltos de cobertura.

Mensagem antiga pode receber resposta nova; evento futuro pode mudar; documento conhecido pode ter nova versão. Consultar as fontes pertinentes e os itens acompanhados, não só datas de criação. Ausência em busca não prova exclusão, cancelamento ou conclusão.

Se faltar o estado necessário, continuar consultas independentes e preparar propostas, sem afirmar continuidade incremental nem executar alterações que dependam dele. Distinguir o marco de consulta de cada fonte do estado de execução e entrega de cada ação.

## 3. Encaminhamentos e responsabilidade

Usar [Gmail](connectors/gmail.md), [Calendar](connectors/google-calendar.md), [Notion](connectors/notion.md), [Drive](connectors/google-drive.md), [oportunidades](modules/academic-opportunities.md) e [pesquisa web](connectors/web-research.md) apenas no alcance escolhido. A Secretary não altera os critérios desses módulos.

Na configuração da execução, atribuir responsabilidade por operação e recurso. A divisão abaixo é uma proposta a apresentar; não concede permissões nem garante exclusividade:

| Trabalho | Divisão proposta |
|---|---|
| Revisão de 30 dias do Gmail | Briefing; Secretary trata novos itens e pendências |
| Novas convocações e mudanças de compromissos | Secretary; Briefing consolida efeitos confirmados |
| Atualização do dashboard compartilhado | Um único fluxo efetivo, escolhido conforme o ambiente |
| Novas notas de leitura | Conversa que realiza a leitura, com a coordenação da biblioteca |
| Oportunidades e documentos | Busca ampla na cadência própria; Secretary acompanha alterações escolhidas |

Se dois fluxos puderem alterar o mesmo alvo, aplicar serialização ou exclusividade comprovada conforme a governança. Um horário diferente, um campo “em execução” ou a designação de um modo não impede execuções simultâneas desse mesmo modo. Sem garantia necessária, preparar a alteração e encaminhar ao fluxo exclusivo; manter as demais funções independentes.

O encaminhamento é uma pendência no estado autorizado, com origem, efeito pretendido, responsável e condição de retomada. Não significa enviar mensagem para outra conversa, disparar agente ou criar agendamento. Essas ações precisam de autorização própria quando forem necessárias.

Nas operações entre serviços, registrar cada efeito. Calendar confirmado e Notion pendente significa retomar o vínculo ou a página, sem criar novo evento. Arquivo salvo e nota pendente significa retomar a nota, sem repetir upload. Se uma gravação tiver resposta incerta, verificar seu efeito antes de repetir; sem evidência suficiente, manter a incerteza.

## 4. Quando comunicar

Apresentar durante a configuração as opções: somente mudanças que exigem decisão; avisos também sobre prazos próximos; resumos em horários escolhidos; ou combinações. Propor silêncio quando nada relevante mudar e solicitar escolha, sem presumir o canal ou ativar notificações.

Um motivo de aviso pode ser: prazo ou compromisso novo relevante; mudança de data, local ou requisitos; conflito confirmado; decisão necessária; falha que afete obrigação; ou lembrete escolhido pelo usuário. Explicar o motivo e a ação possível, com fonte e prazo real quando houver.

Não elevar a urgência por adjetivos do remetente ou por existir um erro de ferramenta. Usar impacto, proximidade do prazo e critérios do perfil. Repetir aviso somente por mudança material, escalonamento autorizado ou lembrete programado. Não cobrar decisão pendente a cada execução.

Identificar um aviso por objeto, mudança ou motivo, destinatário e canal. Comparar com avisos já confirmados antes de novo envio. Registrar “preparado”, “entregue”, “falhou” ou “resultado incerto”; gravação de uma página não confirma entrega. Em entrega incerta, verificar antes de reenviar quando a repetição puder duplicar a comunicação.

Respeitar períodos de silêncio. Guardar avisos não urgentes para o horário permitido; exceções urgentes precisam estar configuradas. Se o canal não permitir entrega diferida ou supressão de notificações, indicar o limite na implantação. Não prometer silêncio da plataforma apenas porque a resposta do modelo está vazia.

Enviar relatórios ao próprio usuário pelo destino escolhido não autoriza responder a remetentes, convidar participantes ou compartilhar arquivos. Sucessos de operações configuradas como silenciosas ficam no estado confirmado, sem aviso individual obrigatório. Falhas relevantes seguem a política de entrega escolhida.

## 5. Relação com o Briefing e encerramento

Compartilhar fatos e resultados confirmados, sem produzir um segundo briefing completo a cada ciclo. O [Briefing](briefing.md) apresenta a visão consolidada, inclusive itens importantes já comunicados; a Secretary destaca o que mudou e o que precisa acontecer antes da próxima consolidação.

Pesquisar somente fontes cuja consulta estiver devida. Reutilizar informações válidas e não reler documentos integrais inalterados. Ao atingir o limite da execução, preservar cobertura e pendências; não executar um segundo ciclo oculto ou criar rotina compensatória.

A execução termina com efeitos verificados, estado atualizado no alcance confirmado, entrega conforme a política e pendências identificadas. Falha de uma fonte não transforma o resultado das demais em erro nem em cobertura integral. Em ciclo sem mudança acionável, conservar somente o registro mínimo escolhido.

## 6. Validação antes da ativação

Verificar com casos autorizados: nenhuma mudança; resposta nova em conversa antiga; remarcação; obrigação fora da janela inicial; repetição da mesma notificação; período de silêncio; erro de uma conta; paginação interrompida; gravação incerta; sucesso parcial entre serviços; revogação posterior; e duas execuções concorrentes. Confirmar os efeitos observáveis e o comportamento do agendador no ambiente escolhido, sem usar revisão documental como prova operacional.
