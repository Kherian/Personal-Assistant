# PA — Personal Assistant

Uma skill configurável para organizar informações, acompanhar pendências, estudar e pesquisar com os conectores nativos disponíveis no ChatGPT e no Codex.

**Cada pessoa escolhe o que utilizar.** O PA não vem com contas, interesses, sites, periódicos, destinos, horários ou permissões pessoais preenchidos. Instalar a skill disponibiliza seus procedimentos; a configuração individual define seu funcionamento.

Versão **1.2.1** · Documentação em português · [Licença MIT](LICENSE)

## O que o PA faz

| Função | Para que serve |
|---|---|
| **PA-Briefing** | Reúne prioridades, agenda, correspondência, projetos e os blocos escolhidos em uma visão do período. |
| **PA-Secretary** | Acompanha mudanças e pendências, prepara encaminhamentos e executa somente ações autorizadas, com avisos conforme o perfil. |
| **PA-Pesquisa Acadêmica / PA-Research** | Monitora fontes escolhidas, produz panorama de artigos, seleciona leituras aprofundadas e permite estudar verbetes de enciclopédias. |
| **PA-Oportunidades** | Busca e avalia chamadas, eventos, bolsas, vagas e outras oportunidades segundo critérios individuais, com fontes e prazos verificados. |

As funções são independentes. É possível usar apenas uma, combinar pesquisa e oportunidades em uma chamada ou configurar um acionamento periódico que execute as funções devidas. A biblioteca e as operações pontuais também podem ser usadas sem produzir um briefing completo.

## Integrações disponíveis

O PA usa ferramentas que já estejam disponíveis e autorizadas no ambiente. Não implementa conectores próprios, não fornece credenciais e não exige que todos os aplicativos sejam utilizados.

| Integração | Exemplos de funções selecionáveis |
|---|---|
| **Gmail** | Triagem, leitura progressiva, acompanhamento de obrigações e higiene seletiva. A revisão dos últimos 30 dias e o arquivamento dependem da configuração e das permissões. |
| **Google Calendar** | Agenda, eventos, lembretes operacionais, conflitos e recorrências. O módulo distingue lembrete operacional de alerta de evento e de tarefa nativa. |
| **Notion** | Dashboard adaptado à estrutura do usuário, áreas estáticas e dinâmicas, biblioteca por obra, notas de leitura, projetos e histórico. |
| **Google Drive** | Pesquisa, leitura, organização e operações escolhidas sobre arquivos, documentos, planilhas e apresentações. |
| **Pesquisa web** | Consulta a fontes públicas, notícias opcionais, literatura e oportunidades. |

Integrações entre serviços também são escolhas: por exemplo, registrar eventos no Notion ou vincular documentos do Drive a projetos. A leitura de uma conta não autoriza alterar seus dados. Envio, publicação, compartilhamento, exclusão e demais operações têm permissões próprias.

## Começar a usar

1. Instale a skill ou o plugin por uma das opções abaixo.
2. Peça: **“Use o PA para configurar meu assistente pessoal.”**
3. Escolha funções, aplicativos e fontes. O PA deve apresentar as opções em blocos curtos, aproveitando respostas já dadas.
4. Defina contas, destinos privados, critérios, frequências, limites, notificações e operações permitidas apenas para as funções escolhidas.
5. Teste uma execução manual. Depois, se desejar, configure o agendamento no ambiente em que ele realmente funcionará.

O [modelo de configuração](plugins/pa-personal-assistant/skills/pa-personal-assistant/configuration/user-config.md) é um roteiro público vazio. O perfil preenchido e o histórico operacional devem ficar em local privado escolhido pela pessoa, fora deste repositório e acessível ao ambiente de execução. Não é necessário editar Markdown para responder à configuração.

## Instalação

### Opção A — Skill global no Codex

Em um ambiente Codex que tenha a skill de instalação, peça:

> Use $skill-installer para instalar globalmente a skill do repositório Kherian/Personal-Assistant, no caminho plugins/pa-personal-assistant/skills/pa-personal-assistant. Use o diretório de skills do usuário deste ambiente e preserve uma instalação existente caso encontre uma.

A pasta completa da skill está em [plugins/pa-personal-assistant/skills/pa-personal-assistant](plugins/pa-personal-assistant/skills/pa-personal-assistant/SKILL.md). Para uma instalação manual local, copie essa pasta inteira para o diretório de skills do usuário; na organização atual documentada do Codex, `~/.agents/skills/pa-personal-assistant`. Não copie apenas `SKILL.md` e não substitua uma instalação existente sem revisar as diferenças.

O Codex detecta novas skills; se ela não aparecer, reinicie o aplicativo. A instalação global local vale para o usuário naquele computador, não instala automaticamente o PA na conta web nem em outros dispositivos. Veja a [documentação oficial de skills](https://learn.chatgpt.com/docs/build-skills).

### Opção B — Plugin pelo catálogo do repositório

O repositório também inclui um manifesto portátil e um catálogo de instalação. Em um cliente com a CLI do Codex disponível:

```sh
codex plugin marketplace add Kherian/Personal-Assistant
```

Depois, abra o diretório de plugins no aplicativo desktop, selecione a fonte **PA — Personal Assistant** e instale o plugin. Reinicie o aplicativo se necessário. Registrar o catálogo não equivale a concluir a instalação. Veja a [documentação oficial de distribuição](https://developers.openai.com/plugins/build/plugins).

Escolha uma das formas para evitar duas cópias da mesma skill no ambiente. A presença deste repositório no GitHub não significa publicação no diretório oficial de plugins. Disponibilidade na web e em workspaces depende dos recursos e políticas do ambiente e deve ser verificada separadamente.

## Exemplos de uso

- “Use o PA para configurar somente agenda e correspondência.”
- “Execute PA-Briefing conforme meu perfil.”
- “Execute PA-Secretary e informe apenas mudanças que precisem de atenção.”
- “Execute pesquisa acadêmica e oportunidades com as fontes que configurei.”
- “Configure um estudo periódico de verbetes; apresente as opções de fontes e frequência.”
- “Consulte minha biblioteca antes de reler este artigo e prepare uma nota conforme minhas permissões.”
- “Use o PA conforme minha programação e execute apenas as funções devidas agora.”

No Codex, a invocação explícita é `$pa-personal-assistant`. Em superfícies que usam um seletor de skills, selecione a habilidade instalada. A seleção implícita pode ocorrer conforme o pedido, mas não é uma garantia de acionamento em toda conversa.

## Pesquisa e estudo personalizados

Cada pessoa escolhe seus periódicos, enciclopédias, bases bibliográficas, repositórios, temas e projetos. Pode fornecer uma lista de links ou um OPML. Nenhuma fonte acadêmica ou área de interesse está selecionada no pacote.

O módulo permite combinar:

- **Estudo de verbetes:** leitura integral e explicação das questões, teses, definições, argumentos, objeções e referências, com histórico para evitar repetição.
- **Panorama de publicações:** análise dos abstracts disponíveis dos artigos novos no recorte acompanhado, com cobertura e lacunas informadas.
- **Leituras aprofundadas:** seleção por relevância e leitura integral quando acessível, com quantidade, frequência e profundidade definidas no perfil.

Os resultados identificam se houve leitura de metadados, abstract, parte do texto ou texto integral. Trabalhos sem acesso completo podem ser apresentados como candidatos ou sínteses limitadas conforme a política escolhida; nunca como leitura integral concluída. Preprints e artigos publicados são distinguidos, e versões da mesma obra são conciliadas.

Páginas públicas podem dispensar uma assinatura de leitor RSS. Feeds só são utilizados diretamente se a ferramenta conseguir lê-los; caso contrário, o PA pode usar páginas HTML verificadas. Isso não garante acesso gratuito ao texto integral nem cobertura completa de todas as fontes.

## Agendamentos

O PA não mantém um processo em execução nem cria rotinas ao ser instalado. O agendador externo inicia cada chamada. Há duas opções:

| Forma | Como funciona |
|---|---|
| **Funções explícitas** | Cada tarefa chama uma função ou um grupo de funções nos horários escolhidos. |
| **Acionamento periódico** | Uma tarefa chama o PA periodicamente; ele consulta horário, fuso, perfil e histórico para selecionar o que está devido. |

A frequência do acionamento limita os horários atendidos. Uma chamada por hora não ocorre em todos os minutos intermediários. Um único agendamento pode economizar espaços, mas não garante menor consumo de recursos. Leituras longas, atrasos e execuções sobrepostas exigem configuração e verificação.

Para funcionar sem depender do computador, a skill, o perfil, o estado e as ferramentas precisam estar disponíveis no ambiente de execução web. Uma pasta local, por si só, não satisfaz essa condição. Consulte o [procedimento de encaminhamento por horário](plugins/pa-personal-assistant/skills/pa-personal-assistant/modules/scheduled-routing.md) e a [documentação oficial de agendamentos](https://learn.chatgpt.com/docs/automations).

## Documentação

| Documento | Conteúdo |
|---|---|
| [SKILL.md](plugins/pa-personal-assistant/skills/pa-personal-assistant/SKILL.md) | Entrada da habilidade e encaminhamento das funções |
| [Configuração individual](plugins/pa-personal-assistant/skills/pa-personal-assistant/configuration/user-config.md) | Escolhas e permissões, sem dados pessoais preenchidos |
| [Governança](plugins/pa-personal-assistant/skills/pa-personal-assistant/governance.md) | Evidência, autorizações, coordenação, falhas e continuidade |
| [Briefing](plugins/pa-personal-assistant/skills/pa-personal-assistant/briefing.md) · [Secretary](plugins/pa-personal-assistant/skills/pa-personal-assistant/secretary.md) | Consolidação e acompanhamento |
| [Pesquisa acadêmica](plugins/pa-personal-assistant/skills/pa-personal-assistant/modules/literature-watch.md) · [Oportunidades](plugins/pa-personal-assistant/skills/pa-personal-assistant/modules/academic-opportunities.md) | Pesquisa, estudo e oportunidades |
| [Gmail](plugins/pa-personal-assistant/skills/pa-personal-assistant/connectors/gmail.md) · [Calendar](plugins/pa-personal-assistant/skills/pa-personal-assistant/connectors/google-calendar.md) | Correspondência e agenda |
| [Notion](plugins/pa-personal-assistant/skills/pa-personal-assistant/connectors/notion.md) · [Drive](plugins/pa-personal-assistant/skills/pa-personal-assistant/connectors/google-drive.md) · [Web](plugins/pa-personal-assistant/skills/pa-personal-assistant/connectors/web-research.md) | Biblioteca, arquivos e fontes públicas |
| [Auditoria e compatibilidade](AUDITORIA.md) | O que foi verificado e o que depende da implantação |

## Privacidade e manutenção

Este repositório contém instruções genéricas. Não envie perfis preenchidos, listas pessoais de fontes, mensagens, documentos privados, identificadores de contas ou credenciais em commits, issues ou pull requests. O arquivo `.gitignore` reduz inclusões acidentais, mas não substitui a revisão do que será publicado.

Para contribuir, abra uma issue ou pull request descrevendo a função ou problema com exemplos fictícios. Preserve a configuração individual, a consulta progressiva dos módulos e a distinção entre instrução, capacidade técnica e autorização. A fonte da skill fica em `plugins/pa-personal-assistant/skills/pa-personal-assistant`; mantenha manifesto, referências e documentação consistentes.

O PA é um pacote de instruções, não um serviço hospedado nem um conjunto de conectores próprios. Acesso às ferramentas, limites de uso, escrita em aplicativos e execução agendada precisam ser verificados em cada ambiente. A validação documental não comprova todas essas operações.

## Licença

Distribuído sob a [licença MIT](LICENSE). As permissões e condições estão no arquivo de licença. Serviços e conteúdos externos continuam sujeitos às suas próprias condições de uso.
