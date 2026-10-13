# PA — Gmail

Versão: **0.2.1**. Estado: **regras aprovadas; catálogo de escolha individual explicitado em 10 de outubro de 2026**.

Organizar a correspondência por meio do conector nativo Gmail: leitura progressiva, higienização dos últimos 30 dias, identificação de obrigações, seleção de conteúdo relevante e encaminhamento de convocações. Aplicar a [governança](../governance.md) e a [configuração individual](../configuration/user-config.md). Este arquivo não autoriza operações nas contas por sua mera aprovação.

## 1. Configuração específica

Acrescentar as respostas abaixo à seção Gmail do perfil privado, quando esse conector for escolhido. Aproveitar contas e autorizações já registradas. Não exigir novamente a aprovação de uma política já concedida pelo usuário; esclarecer apenas parâmetros que faltarem.

Apresentar o catálogo abaixo antes dos parâmetros. Cada função pode ser escolhida ou dispensada e configurada sob demanda, no Briefing, na Secretary ou em combinação. As regras deste arquivo descrevem como executar as funções selecionadas; não ativam o conjunto para todos os usuários.

| Função selecionável | Escolhas a apresentar |
|---|---|
| Consulta e síntese de mensagens | Contas, marcadores, alcance, relevância e leitura progressiva |
| Higienização da caixa de entrada | Usar ou não; proposta de janela de 30 dias e proteções |
| Arquivamento de conteúdo encerrado | Critérios, exceções e confirmação por ação ou autorização persistente |
| Listas e fóruns | Quais acompanhar, o que resumir e quando sugerir exclusão |
| Obrigações e convocações | Vínculos, critérios e integrações escolhidas com Calendar e/ou Notion |
| Spam, Lixeira e auditorias ampliadas | Usar ou não, recortes, frequência e volume, independentemente da limpeza cotidiana |
| Oportunidades recebidas | Critérios de encaminhamento ao módulo responsável, quando selecionado e disponível |
| Anexos no Drive | Selecionar a [função correspondente do Drive](google-drive.md#5-anexos-projetos-e-resultados-produzidos), contas, filtros e destinos; não habilitar por escolher leitura de anexos |
| Operações adicionais | Escolher separadamente marcadores, estado de leitura, rascunhos, lixeira e envio, com suas permissões próprias |

Aplicar o registro por função da configuração comum. Preservar a janela e as políticas já escolhidas pelo mesmo usuário. Integração desabilitada não gera cobranças de destino ou sincronizações pendentes; dependência escolhida mas indisponível permanece delimitada.

| Informação | Proposta para configuração |
|---|---|
| Contas e modos | Escolher quais contas serão usadas por Briefing e Secretary |
| Escopo de leitura | Caixa de entrada por padrão, com consulta direcionada a Enviados para esclarecer respostas e participação, dentro da autorização de leitura; outros marcadores ou pastas conforme escolha ou contexto autorizado |
| Higienização | Mensagens recebidas nos últimos 30 dias e ainda na caixa de entrada |
| Revisão de Spam e Lixeira | Opcional, com frequência semanal sugerida; definir contas, janela de recebimento e limite de volume; leitura não autoriza restauração |
| Auditoria ampliada | Consulta ocasional de dois meses ou de outro recorte solicitado; não amplia a limpeza cotidiana |
| Arquivamento de conteúdo encerrado | Autorizar sob os critérios da seção 5 ou manter confirmação por ação |
| Proteções | Proteger estreladas; acrescentar remetentes, conversas ou marcadores indicados pelo usuário |
| Relevância | Definir prioridades, interesses, remetentes e tipos de obrigação pertinentes |
| Listas e fóruns | Indicar os que acompanha e os critérios de pertinência; não exigir uma lista exaustiva de antemão |
| Vínculos de participação | Registrar órgãos, grupos, comissões, papéis e tipos de evento abrangidos; considerar manifestações específicas do usuário sem inferir um vínculo permanente |
| Encaminhamento de convocações | Registrar a autorização correspondente e os destinos, quando os módulos Calendar e Notion forem configurados |
| Operações adicionais | Marcadores, estado de leitura, rascunhos, lixeira e envio têm permissões próprias |
| Limites por execução | Definir volume e chamadas compatíveis com o ambiente; não interpretar limite omitido como trabalho ilimitado |

Identificar as listas e fóruns relevantes durante a configuração individual. Nenhuma lista, interesse, vínculo ou autorização pessoal vem predefinida no pacote compartilhável.

## 2. Responsabilidade de cada modo

| Modo | Trabalho neste conector |
|---|---|
| PA-Briefing | Consolidar correspondências e pendências; revisar a janela móvel de 30 dias, reaproveitando leituras válidas; executar o arquivamento seletivo autorizado; reunir sugestões de exclusão e a revisão opcional de Spam e Lixeira quando prevista |
| PA-Secretary | Examinar mensagens novas no escopo selecionado, consultar respostas enviadas quando necessário e rever conversas com pendências; identificar mudanças, prazos e convocações; atualizar o progresso compartilhado |

Como divisão inicial, a higienização e o arquivamento automático pertencem ao Briefing. O Secretary pode registrar candidatos para essa revisão; não repete a varredura de 30 dias a cada execução nem arquiva o mesmo conjunto em paralelo. Uma mudança dessa divisão deve ser registrada explicitamente.

Ambos podem identificar o mesmo compromisso ou obrigação. Encaminhar um único item reconhecível pelos identificadores de origem; se já houver encaminhamento, atualizar sua informação em vez de gerar outro. A execução das alterações nos destinos será definida pelos respectivos módulos e pela coordenação aprovada.

A revisão semanal opcional de Spam e Lixeira pode integrar uma execução do Briefing quando estiver devida, com controle separado de cobertura. Uma auditoria de dois meses é ocasional e depende de solicitação ou configuração própria. Essas frequências descrevem o procedimento; não criam nem modificam agendamentos.

## 3. Janela de busca e cobertura

No início da execução, fixar o instante de referência. Para higienização, buscar mensagens recebidas nos 30 dias anteriores a esse instante, ainda na caixa de entrada. Incluir lidas e não lidas. A data de recebimento delimita a busca; a data do evento ou prazo determina seu encerramento.

Não expandir automaticamente a limpeza para mensagens mais antigas, itens arquivados, Spam ou Lixeira. É possível consultar mensagens anteriores da mesma conversa para compreender o contexto, dentro da autorização de leitura; isso não as torna alvos da limpeza.

Para o Secretary, partir da última coleta concluída por conta. Usar uma pequena sobreposição temporal para não perder mensagens nas bordas do intervalo e eliminar repetições pelos IDs. Sem marco anterior, usar uma primeira coleta limitada aos últimos 30 dias e identificá-la como inicial. Essa coleta não autoriza executar a higienização do Briefing.

Acompanhar também pendências já registradas, mesmo quando sua mensagem de origem sair da janela de 30 dias. Uma obrigação não se encerra por envelhecimento do e-mail. Buscar atualizações por conversa ou ID sem iniciar uma auditoria histórica geral.

Paginar até cobrir o recorte ou atingir o limite da execução. Registrar cobertura e pendências por conta. Consultas por recebimento não comprovam detecção de todas as alterações de marcadores em mensagens antigas; revalidar o estado atual dos alvos antes de modificá-los.

Manter por conta e escopo consultado o intervalo, a consulta, a cobertura concluída ou parcial e o ponto de retomada. O sucesso de uma conta não cobre outra; a consulta ao perfil não comprova acesso às mensagens. Distinguir consulta concluída sem resultados, amostra, erro e acesso indisponível. Não avançar o marco de uma busca que falhou. Diante de limite informado, registrar a pendência e continuar apenas o trabalho independente, conforme a governança.

Identificar os candidatos antes de alterar a caixa de entrada. A mudança de marcadores pode modificar o conjunto que está sendo paginado. Se houver interrupção ou alteração desse conjunto, não confiar cegamente em um cursor antigo: refazer a consulta delimitada e reconciliar os IDs já tratados. Na retomada, reavaliar a elegibilidade para arquivamento no instante atual.

### Revisão opcional de Spam e Lixeira

Quando autorizada, pesquisar explicitamente esses locais no recorte configurado, pois a busca comum pode excluí-los. Separar os resultados da higienização da caixa de entrada. Examinar possíveis mensagens relevantes, comprovantes e atualizações de assuntos já acompanhados, sem presumir que uma exclusão foi acidental ou reabrir automaticamente todas as obrigações encontradas na Lixeira.

Se a busca e a leitura individual divergirem quanto aos marcadores, registrar a inconsistência e conferir o estado antes de uma eventual alteração; não afirmar que o item continua em determinada pasta. E-mails semelhantes a correspondência legítima no Spam são candidatos a revisão, não evidência suficiente para restaurá-los.

A autorização de leitura não permite retirar do Spam, restaurar da Lixeira, bloquear remetentes ou excluir mensagens. Relatar somente itens recuperáveis pela interface; não prometer acesso a mensagens eliminadas definitivamente nem um histórico completo do que já esteve nesses locais.

## 4. Leitura progressiva e classificação

1. Começar pelos dados já retornados: conta, remetente, assunto, data, trecho inicial e marcadores. Não repetir uma consulta apenas para recuperar a mesma informação.
2. Ler o corpo quando ele for necessário para avaliar relevância, obrigação, data, participação ou descarte. Um assunto ou trecho isolado não basta para autorizar arquivamento.
3. Consultar a conversa para esclarecer respostas, prorrogações, cancelamentos, pendências e mudanças de participação. Verificar se a ferramenta trouxe a conversa completa ou somente suas mensagens recentes.
4. Ler anexos apenas quando mudarem a decisão. Se data, pauta ou obrigação depender de anexo não acessível, registrar a lacuna; não tratar a ausência de leitura como ausência de pendência.

| Classificação | Resultado esperado |
|---|---|
| Exige ação do usuário | Resumo da obrigação, prazo conhecido, fonte e próxima providência |
| Aguardando terceiro | Registro do que se espera e da conversa correspondente |
| Convocação ou compromisso | Informações verificadas para o encaminhamento da seção 7 |
| Conteúdo relevante sem ação imediata | Síntese proporcional à pertinência, preservando a referência |
| Encerrado e elegível para arquivamento | Aplicar integralmente os critérios da seção 5 |
| Candidato à exclusão | Apresentar proposta identificável; não executar pela classificação |
| Incerto | Explicar a dúvida que impede a decisão; manter o item pendente |

As classificações são operacionais e não criam marcadores no Gmail por si mesmas. Uma mensagem pode conter mais de uma obrigação. Não impor uma classificação única que esconda uma pendência.

Não interpretar o marcador automático de importância do Gmail como substituto dos interesses e prioridades do usuário. Não mudar o estado de leitura apenas porque o PA analisou a mensagem.

### Respostas, mudanças e estado das obrigações

Identificar quem escreveu cada resposta, separando o texto novo do histórico citado. Consultar Enviados de forma direcionada quando isso esclarecer uma pendência ou participação. Confirmações de terceiros, avisos automáticos de leitura e relatórios de assistentes de reunião não comprovam resposta substantiva, aceite ou comparecimento do usuário.

Agrupar respostas sem mudança relevante, como simples ciência ou confirmações de terceiros. Destacar alterações de data, local, pauta, documento, responsabilidade e manifestação do usuário. Não descartar uma resposta apenas por começar com “ciente”: ela pode conter informação nova. O resumo deve mostrar o que mudou desde a última análise, preservando a fonte.

Registrar o estado de cada obrigação pela evidência disponível, sem impor uma sequência obrigatória:

| Evidência | Estado que pode sustentar |
|---|---|
| Solicitação aplicável sem evidência de atendimento | A fazer ou a confirmar, conforme a completude do contexto |
| Envio pertinente comprovado por resposta substantiva ou recibo de formulário/submissão | Enviado; concluir apenas a etapa de envio correspondente |
| Solicitação recebida e ainda sujeita a decisão | Aguardando avaliação ou homologação |
| Comunicação explícita do responsável pelo resultado | Aprovado, homologado, recusado ou concluído, conforme o que foi comunicado |

Um recibo de proposta não comprova aprovação nem confirma a programação do evento. Um aviso de assinatura pendente não comprova documento assinado. Distinguir a conclusão de uma etapa do encerramento de todo o assunto; deixar de cobrar a etapa comprovadamente atendida e manter apenas o acompanhamento restante. Vincular cada mudança de estado à mensagem que a sustenta e à obrigação correspondente.

### Cópias, versões e notificações de aplicativos

Relacionar mensagens sobre o mesmo assunto por conta e IDs de mensagem/conversa; quando necessário, usar número do documento, órgão emissor, assunto, ano, identificador do evento ou URL do registro. Um encaminhamento pode chegar em outra conversa ou conta. Registrar as fontes associadas a um mesmo item, sem fundir obrigações distintas com base apenas em títulos parecidos.

Distinguir cópia de atualização: memorando reenviado não gera nova obrigação; retificação, pauta complementar ou prorrogação pode alterar a existente. Para cada informação em disputa, considerar a competência do emissor e a versão aplicável. Mensagem mais recente não prevalece apenas por ser mais recente, sobretudo se reproduzir informação antiga. Preservar divergências não resolvidas.

Tratar notificações de ClickUp, Calendar, Notion ou outros aplicativos como referências a registros existentes. Reutilizar seus identificadores para evitar o ciclo “registro criado → e-mail de notificação → novo registro”. Avisos antigos de atraso não comprovam o estado atual da tarefa; confrontar com a fonte pertinente e, quando necessário e autorizado, encaminhar a conferência ao conector responsável. Sem essa conferência, indicar a incerteza, sem anunciar que o aplicativo foi corrigido.

Notificações de aplicativos podem conter novas solicitações reais; avaliar a mudança antes de classificar. Distinguir tarefas demonstrativas de onboarding, publicidade, suporte, recibos e notificações operacionais. Não aplicar a mesma decisão a todas as mensagens de um domínio.

### Mensagens e anexos sensíveis

Em requerimentos de alunos e outros assuntos sensíveis, identificar a providência e a pertinência ao usuário antes de aprofundar a leitura. Ler anexos somente quando necessários à decisão autorizada. Não reproduzir diagnósticos, atestados ou documentos integrais no resumo geral ou em páginas amplamente acessíveis.

Para eventual encaminhamento ao Notion ou a outro destino, transmitir apenas a descrição mínima da ação, o prazo e a referência recuperável da mensagem, em local privado com acesso adequado e autorizado. A existência de uma página de evento ou de uma pendência não autoriza copiar todos os anexos relacionados. Se a restrição do destino não puder ser verificada, manter o encaminhamento sensível pendente.

## 5. Arquivamento seletivo

Arquivar automaticamente somente quando houver autorização aplicável e **todas** as condições abaixo forem atendidas:

- A mensagem continua no escopo autorizado de higienização e não está protegida.
- O convite, reunião ou prazo está comprovadamente encerrado, considerando data, horário e fuso pertinentes, quando necessários.
- Não há resposta, documento, prestação de informação ou outra providência pendente; não existe atualização conhecida que reabra ou prorrogue o assunto.
- O conteúdo necessário à continuidade do trabalho já foi registrado no destino autorizado, quando esse registro for necessário.
- A leitura oferece contexto suficiente e a operação escolhida afeta somente os itens autorizados.

**Prazo vencido não equivale a obrigação cumprida.** Uma chamada encerrada sem providência restante pode ser arquivada; uma cobrança ou entrega atrasada permanece pendente. Convite recebido hoje para evento encerrado ontem pode ser elegível, desde que passe pelos mesmos critérios.

Quando houver apenas uma data, sem hora, não presumir encerramento durante aquele dia. Se o fuso, o ano, a duração ou o significado da data mudarem a decisão e não puderem ser estabelecidos, manter a dúvida. Não deduzir encerramento a partir da idade do e-mail.

Preservar mensagens estreladas e as proteções individuais. Se a conversa tiver pendência relevante ou contexto incompleto, não arquivar automaticamente o item que a sustenta. Valor documental permanece relevante para a avaliação; arquivar não apaga a mensagem, mas não deve retirar da caixa de entrada algo ainda necessário ao acompanhamento.

Preferir alterar apenas as mensagens elegíveis, removendo exclusivamente o marcador de caixa de entrada pela ferramenta apropriada. Preservar os demais marcadores e o estado de leitura. Não substituir arquivamento por movimentação à Lixeira.

Só usar arquivamento de conversa inteira quando a leitura e o escopo cobrirem todas as mensagens que perderão o marcador de caixa de entrada e todas forem elegíveis. Quando houver mistura com conteúdo protegido, pendente ou fora da janela, não aplicar a operação à conversa inteira. Se a interface não permitir restringir a alteração com segurança, deixar a ação pendente.

Revalidar o alvo antes da gravação e tratar novas respostas ou alterações como informação capaz de mudar a decisão. A interface examinada não oferece garantia explícita de alteração condicional ao estado previamente lido; não anunciar proteção absoluta contra mudanças simultâneas. Operações por IDs de mensagens delimitam melhor o conjunto afetado.

Registrar os IDs alterados, o motivo e o resultado. Autorização persistente dispensa confirmação por ocorrência. A forma de comunicar ações bem-sucedidas segue a configuração individual.

## 6. Listas e fóruns

Avaliar conteúdo, assunto e pertinência; não classificar toda uma lista como descartável. Agrupar mensagens repetidas sobre o mesmo tema para produzir uma síntese, mantendo referências suficientes para recuperar os itens.

- **Relevante:** resumir o que importa aos interesses, vínculos ou trabalho do usuário; preservar a mensagem e eventual oportunidade ou obrigação identificada.
- **Possivelmente relevante:** indicar brevemente o motivo da dúvida; não tratar a pertinência incerta como autorização de descarte.
- **Sem relevância identificada, repetitivo ou promocional:** resumir por tema quando útil e incluir em sugestões de exclusão, com justificativa e itens identificáveis.

Uma sugestão de exclusão deve permitir conferir conta, remetente/lista, assunto ou tema, datas e mensagens abrangidas. Distinguir quantidade de mensagens de quantidade de conversas. Antes de executar uma exclusão posteriormente autorizada, conferir novamente proteções e novas informações relevantes.

Aprovar a rotina de resumos não autoriza exclusão, cancelamento de inscrição em listas ou bloqueio de remetentes. Essas operações exigem instrução própria e suporte da ferramenta.

## 7. Convocações e encaminhamento para outros módulos

Determinar a participação combinando órgão ou unidade, papel do usuário, tipo de evento e manifestações específicas presentes na conversa. Receber uma mensagem de um curso ou órgão não demonstra participação em suas assembleias. Diferenciar convocação aplicável, convite facultativo, divulgação geral e mensagem encaminhada apenas para conhecimento.

Não estender a exclusão das assembleias de uma unidade a todos os seus assuntos: ela pode encaminhar uma demanda de aluno pertinente ou um convite aceito pelo usuário. Da mesma forma, pertencer a um órgão não anula uma recusa expressa para determinada reunião. A confirmação de um evento isolado não cria vínculo permanente com a unidade.

Quando houver autorização automática para convocações de assembleias ou reuniões importantes às quais o usuário pertence, preparar o encaminhamento para Calendar e Notion sem pedir novamente aprovação da mesma política. Verificar a aplicabilidade e os dados necessários, sem exigir RSVP pessoal para toda convocação abrangida pela regra. Considerar a manifestação aplicável mais recente do usuário; uma recusa expressa impede tratar sua participação como confirmada, e uma mudança posterior exige reavaliação. Se já houver registro associado, encaminhar a atualização pertinente ao módulo responsável, sem excluir o registro automaticamente.

Para unidade sem vínculo registrado, convite facultativo ou participação ambígua, apresentar a informação sem gerar compromisso automaticamente. Uma confirmação expressa do usuário pode esclarecer a participação em um convite específico, inclusive de outra unidade; sua criação no destino continua dependendo da autorização aplicável. Uma convocação pessoal excepcional poderá ser encaminhada quando sua participação e autorização estiverem esclarecidas.

O encaminhamento deve conter, conforme disponível:

- Conta, IDs das mensagens/conversas e referências recuperáveis das fontes, com versão e identificadores de registros associados quando disponíveis.
- Órgão/grupo, título, tipo de convocação, papel do usuário e fundamento do vínculo ou da participação, incluindo manifestação expressa quando houver.
- Data, início, fim, fuso, local ou link, sem inventar valores ausentes.
- Pauta, materiais e providências relevantes, com referências aos anexos quando necessários.
- Indicação de nova convocação, alteração ou cancelamento, mudanças de participação e eventuais divergências entre fontes.
- Autorização aplicável, dados ainda incertos e estado de cada encaminhamento.

Gmail identifica e transmite a informação. Os módulos Calendar e Notion deverão verificar e executar suas próprias operações, incluindo prevenção de duplicação e o tratamento dos registros correspondentes. Enquanto esses módulos ou destinos não estiverem disponíveis e aprovados, manter o encaminhamento pendente; não anunciar evento ou página criados.

Criações automáticas bem-sucedidas de convocações elegíveis podem permanecer silenciosas, conforme autorizado. Ambiguidades e falhas materiais seguem a governança. Registrar um compromisso não autoriza enviar mensagem ao organizador, aceitar convite ou incluir convidados.

Oportunidades acadêmicas encontradas em mensagens podem ser encaminhadas ao módulo próprio, distinguindo convite pessoal, chamada aberta, divulgação informativa e oferta comercial. Registrar a pertinência ao perfil, a instituição ou organização responsável, a fonte, o prazo e os requisitos conhecidos; indicar dados que ainda dependem de verificação. Separar prazo de inscrição ou submissão da data do evento. O recebimento da oferta não comprova qualidade, elegibilidade nem interesse do usuário. O Gmail não substitui a verificação do módulo responsável, não aceita convites e não executa inscrições. Enquanto esse módulo estiver indisponível, manter a oportunidade identificada como pendente de avaliação.

## 8. Operações opcionais e limites

Aplicar marcadores apenas se escolhidos pelo usuário e autorizados para as mensagens correspondentes. Reutilizar nomes existentes quando adequados; não implantar uma taxonomia pessoal ou criar marcadores automaticamente por toda classificação.

Rascunhos podem ser preparados quando solicitados ou abrangidos pela configuração. Diferenciar texto sugerido no resultado de rascunho efetivamente criado no Gmail. Criar ou editar rascunho não autoriza enviá-lo.

Envio, resposta, encaminhamento e movimentação à Lixeira seguem autorizações próprias da governança. A ferramenta de exclusão examinada move mensagens à Lixeira; não apresentar essa ação como eliminação definitiva nem anunciar suporte a exclusão permanente não verificado.

Não criar filtros, regras automáticas do Gmail, novas inscrições ou integrações próprias como consequência da aprovação deste módulo. Caso sejam desejados, discutir sua finalidade e compatibilidade separadamente dentro da etapa apropriada.

## 9. Saída, estado e conclusão

Entregar ao modo solicitante apenas o que mudou ou precisa integrar sua consolidação: ações necessárias, pendências, conteúdo relevante, encaminhamentos, sugestões de exclusão e alterações confirmadas. Indicar conta, origem e prazo quando forem pertinentes ao item.

No estado operacional comum, manter os IDs necessários para reconhecer mensagens tratadas e relacionar fontes, obrigações e registros de destino; a última cobertura concluída por conta e escopo; os critérios aplicados; a evidência do estado de cada obrigação; e as ações ou decisões pendentes. Não copiar mensagens integrais quando referências bastarem. Uma nova resposta ou prorrogação exige reavaliação; uma classificação antiga não autoriza mudanças futuras indefinidamente.

Reaproveitar o que já foi lido e permanece válido. Ao revisar a janela de 30 dias, reavaliar mudanças e o vencimento de datas conhecidas; não reler integralmente todas as mensagens inalteradas apenas porque houve uma nova execução.

A etapa de Gmail só está concluída no recorte declarado quando a coleta foi coberta ou sua parcialidade foi explicitada, os itens foram tratados ou registrados como pendentes, e as alterações anunciadas tiveram resultado confirmado. Mensagens enviadas a outros módulos continuam pendentes até a confirmação do destino. Aplicar os estados e a política de retomada definidos na governança.

## 10. Compatibilidade examinada

Referência documental das interfaces: 9 de outubro de 2026. Conferir busca, leitura, rótulos e escopo de pastas por conta no ambiente de implantação. Um teste de leitura não valida operações de escrita, anexos, integração entre serviços ou execução agendada. Limites, paginação ou divergências entre busca e leitura individual devem ser registrados como cobertura parcial ou resultado a conferir. Manter dados pessoais, mensagens e IDs reais fora deste módulo compartilhável.

| Capacidade nativa examinada | Consequência para o procedimento |
|---|---|
| `search_emails` / `search_email_ids` | Consultas Gmail, filtro por IDs de marcadores e paginação; separar os IDs de mensagens dos de conversas |
| `read_email` e leitura em lote | Recuperar conteúdo quando necessário, respeitando limites da chamada |
| `read_email_thread` e leitura de conversas em lote | Retornam mensagens recentes até o limite solicitado; o padrão da leitura individual é 20, não garantia de conversa integral |
| `read_attachment` | Ler somente anexos identificados na mensagem e suportados; conteúdo inline truncado é apenas uma prévia |
| `batch_modify_email` | Alterar marcadores de mensagens específicas; permite delimitar a remoção de `INBOX` |
| `archive_emails` | Remove `INBOX` das mensagens atuais de cada conversa indicada; exige avaliar todo o alcance da operação |
| `delete_emails` | Move mensagens especificadas à Lixeira |
| `list_labels` | Consultar marcadores e contagens quando necessários; não paginar toda a caixa apenas para obter seus totais |

Para limites temporais precisos, a documentação Gmail admite `after:` e `before:` com segundos desde a época Unix; datas textuais têm interpretação de fuso própria da API. Fixar o intervalo, conferir a correspondência com os horários retornados e evitar lacunas nas bordas. A consulta não comprova leitura de toda a conversa. [Search and filter messages](https://developers.google.com/workspace/gmail/api/guides/filtering).

Marcadores aplicados ou removidos na conversa afetam suas mensagens existentes; uma alteração por mensagem delimita um conjunto diferente. Essa distinção sustenta a preferência por operações com alcance explícito. [Manage labels](https://developers.google.com/workspace/gmail/api/guides/labels).

Disponibilidade descrita e sucesso interativo em uma conta não comprovam acesso nas demais contas nem funcionamento no agendamento. Validar as capacidades necessárias no ambiente de execução autorizado após a definição dos destinos e dependências, sem depender de abrir manualmente o Work a cada rotina e sem presumir que os arquivos locais estarão disponíveis ali. A política documental não altera os agendamentos existentes.

## Revisão desta etapa

As diretrizes de higienização por 30 dias, arquivamento seletivo, tratamento de listas e encaminhamento de convocações preservam as decisões de origem. Esta revisão incorpora, por solicitação do usuário, as melhorias discutidas após a auditoria: participação por evento, leitura direcionada de Enviados, síntese de mudanças, estados sustentados por comprovantes, tratamento de cópias e notificações, revisão opcional de Spam e Lixeira, triagem de oportunidades e minimização de conteúdo sensível. Frequências, contas, destinos e permissões serão registrados no perfil individual; a atualização deste arquivo não ativa rotinas.

O pedido para avançar à próxima etapa aprovou esta versão do módulo. A etapa seguinte é discutir [Google Calendar](google-calendar.md); sua aprovação e suas permissões são independentes.
