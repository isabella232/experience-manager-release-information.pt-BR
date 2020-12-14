---
title: AEM 6.2 Cumulative Fix Pack
description: 'null'
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '19954'
ht-degree: 19%

---


# AEM 6.2 Notas de versão do Cumulative Fix Pack{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Informações da versão {#release-information}

| **Produto** | Adobe Experience Manager |
|---|---|
| **Versão** | 6.2 |
| **Versão** | [Cumulative Fix Pack 6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **Pré-requisitos** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **Disponibilidade geral** | 06 de junho de 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

A Adobe apresentou um modelo de entrega única para lançar correções. Em vez de lançar hot fixes para problemas individuais, o Adobe agora lança um Cumulative Fix Pack (CFP) todos os meses (sujeito à aprovação em verificações de qualidade). Um CFP é um pacote de conteúdo agregado com várias correções. Os CFPs incluem principalmente correções de erros, mas também podem incluir Pacotes de recursos. Elas têm as seguintes vantagens em relação às versões de hotfixes individuais:

* Natureza cumulativa (por exemplo, um CFP contém correções entregues em CFPs anteriores)
* Maior garantia de qualidade
* Instalação simplificada (o usuário instala um CFP como pacote único e sem dependências, exceto no caso do pacote de serviço mais recente)

Para obter mais informações sobre o CFP e outros tipos de versões, consulte [Veículo de versão de manutenção](https://docs.adobe.com/content/docs/pt/aem/6-2/deploy/maintenance-release-vehicle-definitions.html).

## Sobre a versão {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 é o último Cumulative Fix Pack para AEM 6.2 e é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilidade geral de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

>[!CAUTION]
>
>Aplicar o CFP sem validar a compatibilidade entre os pacotes de recursos instalados pode resultar em falha do sistema ou perda de configurações personalizadas, o que pode exigir a restauração do backup para solucionar.

>[!NOTE]
>
>* Um novo pacote Sling `discovery-  api` Johnzon 1.0.0 está incluído AEM Cumulative Fix Pack 6.2 SP1-CFP10. Além disso, um usuário de serviço sling-Discovery é adicionado com privilégios de Leitura e Gravação para o nó */var/Discovery* no repositório CRX.
   >
   >
* O pacote de e-mail de apache commons **org.apache.commons/commons-email/1.5** foi adicionado substituindo **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
   >
   >
* A Adobe recomenda implantar o CFP por meio da pasta de instalação para clientes que tenham um grande número de usuários AEM instância.

>



## Problemas incluídos {#issues-included}

Esta seção lista todos os problemas e hotfixes incluídos no CFP atual.

Além disso, este CFP inclui hotfixes fornecidos em [pacotes de correção cumulativos anteriores](#previous).

### Integração {#integration}

* Oferecendo suporte a várias melhorias na personalização da definição de metas de Campanha. NPR-29163: Hotfix do CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler entra em um loop infinito e causa atualizações para nós em instâncias de publicação. NPR-28561: Hotfix do CQ-4263096

### DAM - Geral {#dam-general}

* Não é possível exibir/ocultar o botão de replicação para usuários não administradores em pastas de dam específicas. NPR-29026: Hotfix do CQ-4265361

###  Vulnerabilidade{#vulnerability}

* A estrutura de proteção do CSRF não está funcionando com formulários fundamentais do AEM. NPR-28612: Hotfix do GRANITE-22231

### Forms {#forms}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package}

>[!NOTE]
>
>Para clientes do AEM Forms, é essencial instalar o pacote complementar do AEM Forms após instalar qualquer Service Pack, Cumulative Fix Pack ou Feature Pack do AEM.

>[!NOTE]
>
>Os pacotes complementares do AEM Forms ajudam a alinhar a funcionalidade dos AEM Service Packs e dos Cumulative Fix Packs. Portanto, é imperativo instalar AEM pacote complementar de formulários após instalar qualquer AEM Service Pack, Cumulative Fix Pack ou Feature Pack.

#### Formulários adaptáveis {#adaptive-forms}

* Problemas de usabilidade com o componente de script para dispositivos iOS 12.1. NPR-29082: Hotfix do CQ-4261765

#### Forms - Segurança de documentos {#forms-document-security}

* A verificação de todas as assinaturas em um PDF usando o PDF Advanced Electronic Signatures (PAdES) lança InvalidOperationException. NPR-27848: Hotfix do CQ-4244837

#### Forms - Correspondência {#forms-correspondence}

* Ao visualizar a carta como PDF, o campo de texto colocado na página principal não honra o valor inserido da guia de dados ou do vínculo de dados especificado. NPR-29239: Hotfix do CQ-4266856.

#### Forms - Comunicação interativa {#forms-interactive-communication}

* Quando um caractere apóstrofo é adicionado, os campos pré-preenchidos na letra aparecem como caracteres ASCII em vez de alfabetos regulares. NPR-28863: Hotfix do CQ-4262900

### Instalador do Forms JEE {#forms-jee-installer}

* Nenhuma nova correção do AEM Forms no instalador do Forms JEE.

## Correções e Feature Packs incluídos em Fix Cumulative Packs anteriores {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Os principais destaques deste Cumulative Fix Pack são:

* Suporte habilitado para MS Translator API v3.0 para AEM 6.2
* Mensagem de registro adicionada após a instalação bem-sucedida do pacote para todos os SPs, CFPs e HFs.

### Assets {#assets}

* Não é possível renomear a pasta DAM se a permissão Editar ACL estiver ausente. NPR-27555: Hotfix do CQ-104652
* A ferramenta do editor de predefinições de imagens não responde na versão 6.2.1 CFP 17 e posterior. NPR-28147: Hotfix do CQ-4261041

### Sites {#sites}

* O Verificador de links não conclui o trabalho, fica preso aos links que não respondem. NPR-27373: Hotfix do CQ-4256030
* O arquivo de segmento não é carregado corretamente devido a um caminho raiz adicional que quebra o caminho do segmento. NPR-28014: Hotfix do CQ-4260332

### Integração {#integration-1}

* O cancelamento da herança do LiveCopy não funciona corretamente em container direcionados. NPR-28129: Hotfix do CQ-4259813
* As ações cq :não são consideradas para um componente direcionado. NPR-27616: Hotfix do CQ-4257497

* A exibição de ícone para quebra de herança não é coerente. NPR-27671: Hotfix do CQ-4257779

### Felix {#felix}

* Os detalhes do componente do console da Web falham com 500 após a instalação do CFP 18 na instância AEM 6.2 SP1. NPR-28350: Hotfix do CQ-4261095

### Tradução {#translation}

* Ative o suporte para o serviço MS Translator no AEM 6.3 após a atualização do MS Translator para a API v3.0. NPR-28123: Hotfix para CQ-4259096

### IU - Foundation {#ui-foundation}

* O Calendário de Sites OOTB mostra datas incorretas. NPR-28392

### Granite {#granite}

* O dicionário não é invalidado para pacotes de recursos que usam sling:basename. NPR-27624

### Sustentação {#sustenance}

* Os registros de atividades do gerenciador de pacotes devem ser extraídos em um arquivo de registro separado. NPR-27323: Hotfix do Granite-14866
* Uma frase/texto/linha(s) de registro padronizada(s) no error.log a ser exibido quando a instalação for concluída. NPR-27835
* O plug-in de pacote granite está escolhendo a dependência de uma versão mais recente de org.apache.sling.i18n. Hotfix do CQ-4263245
* O pacote com.adobe.cq.com.adobe.cq.ui.commons é excluído ao instalar o CFP mais recente após 6.2SP1-CFP15. Hotfix do CQ-4258808

### Forms {#forms-1}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-1}

#### Formulários adaptáveis {#adaptive-forms-1}

* Vulnerabilidade de injeção XML com o AEM Forms. NPR-27843: Hotfix do CQ-4257315

### Instalador do Forms JEE {#forms-jee-installer-1}

* Nenhuma nova correção do AEM Forms no instalador do Forms JEE.

### Pacotes OSGI e de conteúdo incluídos {#osgi-bundles-and-content-packages-included}

O texto seguinte documentos a lista dos pacotes OSGI e dos pacotes de conteúdo incluídos no CFP.

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP19

[Obter arquivo](assets/do-not-localize/cfp19_osgi_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP19

[Obter arquivo](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Os principais destaques deste Cumulative Fix Pack são:

* Adição de suporte no DAM CommandLineProcess para eliminar o processo de longa duração.
* Foi corrigido um vazamento de sessão em ReplicationEventListener.
* Adição do suporte de redirecionamento ao componente da página principal.

### Ativos {#assets-1}

* Processos Camera Raw ficam presos durante períodos de ingestão maciça que eventualmente bloqueiam todo o processamento do fluxo de trabalho. NPR-26990: Hotfix do NPR-23860
* A funcionalidade de download aproveita a AEM Assets por meio do servlet de download de ativos, permitindo que usuários anônimos baixem todos os ativos. NPR-27054, Hotfix para CQ-4254732
* Caracteres especiais aparecem quebrados na linha de assunto dos modelos de e-mail no AEM. NPR-26470: Hotfix do CQ-4252368

### Sites {#sites-1}

* Devido ao comportamento incorreto da classe ConfigPostProcessor, suspender a imagem pai remove cq : Tipo de mixagem do LiveRelationship a partir da página secundária. NPR-26745: Hotfix do CQ-4254163
* Adicione o suporte de redirecionamento ao componente principal da página. NPR-26576: Hotfix do CQ-110529
* Migre o hub de contexto para jquery 3. NPR-26956: Hotfix do CQ-4255472
* Os campos de entrada de âncora aparecem fora da seção visível dos navegadores na caixa de diálogo até serem maximizados. NPR-26852: Hotfix do CQ-4255019
* Copie a colagem do texto inserindo &lt;br> indesejado no fragmento Conteúdo. NPR-26660: Hotfix do CRTE-151
* O siteadmin clássico não renderiza a lista no painel direito de algumas páginas. NPR-27247: Hotfix do CQ-4251621
* (Interface clássica) As tentativas de mover/renomear páginas geram um erro, &quot;Ocorreu um erro ao mover a página&quot;. NPR-27179: Hotfix do CQ-4235907

### Integração {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever passa por toda a árvore para coletar as marcas disponíveis. NPR-27060: Hotfix do CQ-4255790

### WCM - Componentes do Foundation {#wcm-foundation-components}

* Problema de funcionalidade de pesquisa com o componente de lista do Foundation. NPR-26817: Hotfix do CQ-4250324

### Plataforma {#platform}

* Devido ao traço em caracteres especiais, o Publisher está com problemas para limpar o cache. NPR-27199: Hotfix do CQ-4242790

### Granite {#granite-1}

* A Validação de pacote não valida pacotes incluídos no CFP/SP. NPR-26775: Hotfix do Granite-22825

### Replicação {#replication}

* vazamento de Sessão JCR no ReplicationListener. NPR-27063: Hotfix do CQ-4232088

### Forms {#forms-2}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-2}

* Nenhuma nova correção do AEM Forms no pacote complementar do Forms.

### Instalador do Forms JEE {#forms-jee-installer-2}

* Nenhuma nova correção do AEM Forms no instalador do Forms JEE.

#### Pacotes OSGI e de conteúdo incluídos {#osgi-bundles-and-content-packages-included-1}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP18

[Obter arquivo](assets/do-not-localize/62cfp18updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2 SP1-CFP18

[Obter arquivo](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Os principais destaques deste Cumulative Fix Pack são:

* Adição de suporte a URLs sem extensão do site em at-integration.js
* Removido o importador de sondagem S7 da configuração do serviço em nuvem S7.
* Alterações na visualização do audiência para suportar a estrutura de pastas para implementação de vários locatários.
* Atualizar para jqueryui   clientlib v1.12.1.

### Ativos {#assets-2}

* Iniciar workflows da interface do usuário do ativo requer que o usuário tenha permissões de gravação/exclusão/modificação. NPR-25688: Hotfix do CQ-4250140
* Os botões Publicar e Cancelar publicação permanecem visíveis mesmo para os usuários sem permissões de &quot;replicação&quot;. NPR-25094
* (Fluxo de trabalho) O fluxo de trabalho do Ativo de tag inteligente não é processado pela configuração de proxy AEM. NPR-25915: Hotfix do CQ-4248202
* Remova o importador de sondagem S7 da configuração do serviço em nuvem S7. NPR-25239: Hotfix do CQ-95236

### Sites {#sites-2}

* Workflows iniciados pelo Editor -> Informações da página contêm o caminho de contexto na carga. NPR-26389: Hotfix do CQ-76804
* (Verificador de links externos) Links https inválidos são exibidos como links válidos. NPR-25541: Hotfix do CQ-4201333
* (Interface clássica) Ao criar uma página independente em uma live copy, a página é criada como uma live copy. NPR-25610: Hotfix do CQ-4249801
* Problemas com recursos de publicação associados ao componente Importador de design quando uma página é ativada. NPR-25638: Hotfix do CQ-102532
* A barra de ferramentas Rich Text do RTE cobre lista selecionada. NPR-25165: Hotfix do CQ-4248948
* Migre o contexthub para jquery 3. NPR-25059: Hotfix do Granite-19902
* Para componentes parsys aninhados, sempre o primeiro (com caminho menos aninhado) design satisfatório é aplicado de vários componentes disponíveis. Para obter mais informações, consulte [Resolução do caminho de design](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html). NPR-25250: Hotfix do CQ-4246276

### Integração {#integration-3}

* Usando a integração de público alvo OTB, a definição de metas de um componente renderiza a página inteira em vez de um componente direcionado vazio. NPR-25273: Hotfix do CQ-4248003
* Quebrar a herança no modo de definição de metas ainda mostra o componente como direcionado com a herança não quebrada no modo de edição. NPR-25324: Hotfix do CQ-4248162
* Quando uma personalização é definida em uma página e uma audiência é resolvida, a experiência correspondente é exibida no modo de edição. NPR-25731: Hotfix do CQ-4249465
* URL do teaser incorreta ao usar AEM com um caminho de contexto não padrão. NPR-25971: Hotfix do CQ-4250953
* Renderização em branco ao usar o optout. NPR-25295: Hotfix do CQ-4246792
* As experiências excluídas do ambiente do autor nunca são removidas do site de publicação na ativação da página. NPR-24869: Hotfix do CQ-4247832

### DAM - Cliente DM {#dam-dm-client}

* (Chrome, Firefox) O VideoPlayer ignora cliques do mouse em dispositivos habilitados para toque. Hotfix do CQ-4247370

### Plataforma {#platform-1}

* Permita configurar o número máximo de tentativas ao adquirir/liberar um pacote. NPR-25328: Hotfix do Granite-22376
* Log incorreto em caso de erros de replicação. NPR-25308: Hotfix do CQ-4249402
* A instalação do Forms AEM 6.2 Forms CFP8 para CFP14 faz com que o Apache POI falhe. NPR-25053: Hotfix do Granite-21771

### Granite {#granite-2}

* O processo de sincronização do usuário está falhando com a exceção OakConstraint0022. NPR-25729: Hotfix para Oak-7428

### Communities {#communities}

* cq -social-as-provider bundle não start com as versões mongo driver 3.x. NPR-26271: Hotfix do CQ-4252710

### IU - Foundation {#ui-foundation-1}

* Atualizar para jqueryui   clientlib v1.12.1. NPR-25090: Hotfix para Granite-21981, CQ-4248897

* (Omnisearch): A propriedade &#39;Title&#39; está vulnerável a scripts entre sites (XSS) em Sites. NPR-24994: Hotfix do Granite-19933

### Forms {#forms-3}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-3}

#### Formulários adaptáveis {#adaptive-forms-2}

* Codificação incorreta ao enviar dados do Formulário adaptativo. NPR-25539

#### Forms - Gerenciamento {#forms-management}

* Ativos de formulário não relacionados relatados como referências ao publicar a página. NPR-26167: Hotfix do CQ-4251004

### Forms - Instalador JEE {#forms-jee-installer-3}

#### Segurança de documentos {#document-security}

* A variável é preenchida como Lista de tipo de dados, o subtipo é string, mas obtemos um erro &quot;não é possível forçar o objeto&quot;. NPR-26194: Hotfix do CQ-4252287
* Não é possível acessar as configurações de marca d&#39;água após a instalação do 6.2-SP1-CFP15. NPR-26130: Hotfix do CQ-4250984

### Pacotes OSGI e de conteúdo incluídos {#osgi-bundles-and-content-packages-included-2}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP17

[Obter arquivo](assets/do-not-localize/62cfp17updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP17

[Obter arquivo](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Os principais destaques deste Cumulative Fix Pack são:

* Adição de suporte STARTTLS no Day CQ Mail Service.
* Corrigido o alinhamento dos ícones do ContextHub no perfil.
* Correções na funcionalidade mostrar/ocultar do componente suspenso.
* Atualize para a versão mais recente do Jackson 2.8.11

### Ativos {#assets-3}

* Não é possível iniciar um fluxo de trabalho a partir de uma visualização de lista. NPR-24393: Hotfix do CQ-4245788
* (Firefox/Chrome) Não é possível baixar ativos na página Compartilhamento de ativos. NPR-24523: Hotfix do CQ-4224408
* Melhoria da qualidade padrão da pré-visualização de vídeo no AEM. NPR-24148: Hotfix do CQ-4244310

### Integração {#integration-4}

* Quando um componente é direcionado para a instância de publicação, a oscilação é exibida mostrando a experiência padrão antes da experiência direcionada. NPR-23992: Hotfix do CQ-4242038
* As experiências excluídas do ambiente do autor nunca são removidas do site de publicação na ativação da página. NPR-24869: Hotfix do CQ-4247832

### Plataforma {#platform-2}

* Patch jQuery 1.12.4 do clientlib para incluir a correção de segurança. NPR-24129: Hotfix do Granite-20058
* Adição de suporte STARTTLS no Day CQ Mail Service. NPR-23941: Hotfix do CQ-4240397
* Remova o padrão MERGE_PRESERVE aclHandling. NPR-24593: Hotfix do Granite-21889
* O LineChecker falha ao externalizar links quando a solicitação contém parâmetros de query inválidos. NPR-24127: Hotfix do CQ-4241893

### MSM {#msm}

* Hotfixes proativos para ataques de Scripts entre Sites (XSS). NPR-21893: Hotfix do CQ-4223385
* MSM LiveRelationship: falha de RolloutConfig efetivo se o BlueprintConfig estiver na raiz. NPR-23999: Hotfix do CQ-4243000

### Sites {#sites-3}

* A criação de uma nova experiência em uma área de live copy requer que a herança seja quebrada para ser configurada. NPR-24995, Hotfix para CQ-4248209
* (Interface do usuário para toque) Vários ícones na barra de ferramentas superior desaparecem ao bloquear ou desbloquear uma página. NPR-23954: Hotfix do CQ-4243345
* Os campos não estão alinhados corretamente no contexto. NPR-23958
* Ação de publicação na criação de quebras de página bloqueadas. NPR-23970: Hotfix do CQ-4243203
* Os relatórios OTB em /etc/reports/ não estão funcionando corretamente e não mostram nenhum gráfico de dados históricos. NPR-20035: Hotfix do CQ-4220180
* Falha na criação do lançamento ao iniciar o fluxo de trabalho &quot;Solicitar inicialização&quot; em um projeto. NPR-24255: Hotfix do CQ-4245030
* Tags e atributos HTML ignorados por e-mails após a instalação CFP10. NPR-24287: Hotfix do CQ-4240028
* Seletor de tags: Sugestão de tag nos query de campo de tag de metadados de tag do schema, portanto, demorando muito para carregar. NPR-24347: Hotfix do CQ-4244291
* A integração do Salesforce falha com configurações de proxy. NPR-24418: Hotfix do CQ-4245300
* (WCM) O PageManager deixa a Página com check-in em Exceção durante a criação da Revisão. NPR-24565: Hotfix do CQ-4246203
* O botão Device Emulator desaparece do modo de edição e pré-visualização após aplicar CFP14. NPR-24566: Hotfix do CQ-4247060
* (Interface clássica) As tags inteiras são exibidas como vazias uma vez criadas na caixa de diálogo. NPR-24688, Hotfix para CQ-4246407
* Não é possível criar a versão na primeira tentativa. NPR-24774: Hotfix do CQ-4232176
* Os relatórios OTB em /etc/reports/ não estão funcionando corretamente e não mostram nenhum gráfico de dados históricos. NPR-24138: Hotfix do CQ-4220180

###  Vulnerabilidade{#vulnerability-1}

* A integração do Salesforce está vulnerável à Falsificação de solicitação do lado do servidor (SSRF). NPR-24289: Hotfix do CQ-4245277
* Vulnerabilidade SSRF (Server Side Request Forgery) em ReportingServicesProxyServlet. NPR-24657: Hotfix do CQ-4246880

### Granite {#granite-3}

* As operações de leitura de metadados não estão sendo terminadas. NPR-24240: Hotfix do Granite-19866
* Atualize Jetty para 9.4.11.v20180605 para corrigir vulnerabilidades. NPR-25033: Hotfix do Granite-22120

### WCM - Componentes do Foundation {#wcm-foundation-components-1}

* PageComparator lançando ClassCastException ao classificar páginas. NPR-24123: Hotfix do CQ-4244048
* A funcionalidade Mostrar/Ocultar do componente de formulário suspenso não está funcionando como esperado. NPR-24562: Hotfix do CQ-4222853

### Interface do usuário {#user-interface}

* A alta utilização da CPU é observada devido a muitas solicitações na funcionalidade do Admin Search. NPR-23588: Hotfix do Granite-21286
* (Interface clássica) O componente exibe os valores padrão mesmo se o serviço de modelo de dados de formulário associado estiver definido como campo vazio. NPR-21903: Hotfix do GRANITE-19744
* Vários campos lançando o NPE quando nenhum FormData está presente para solicitação. NPR-24513: Hotfix do Granite-21055

## Forms {#forms-4}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-4}

#### Núcleo {#core}

* (OSGI) AEM Forms OSGI afetado pelo alerta de segurança de vínculo de dados Jackson. NPR-24274: Hotfix do CQ-4230245

#### Rights Management {#rights-management}

* Falha no POI do Apache após a instalação AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: Hotfix do CQ-4245898, CQ-4244778

#### Formulários HTML5 {#html-forms}

* Os dados não são preenchidos com o preenchimento prévio de campos de várias linhas na pré-visualização HTML. NPR-23357: Hotfix do CQ-4244212
* Quando uma letra é visualizada por pré-visualização padrão, o mapeamento do fragmento do layout não é exibido enquanto o mesmo é exibido corretamente quando clicado no botão pré-visualização. NPR-22993: Hotfix do CQ-4237745
* Problema com a pré-visualização HTML de um campo de texto quando um padrão de Número de Segurança Social é aplicado a um modelo. NPR-23205

#### Formulários adaptáveis {#adaptive-forms-3}

* Erro &quot;Guidelib não está definido&quot; ao adicionar AEM formulário ao componente parsys. NPR-24269: Hotfix do CQ-4244546

### Instalador do Forms JEE {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Finalizações de linha de janela em arquivos de script Shell fazem com que o LCM não seja executado no UNIX. NPR-22958

### Pacotes OSGI e de conteúdo incluídos {#osgi-bundles-and-content-packages-included-3}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP16

[Obter arquivo](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP16

[Obter arquivo](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral de [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Os principais destaques deste Cumulative Fix Pack são:

* Correção de segurança pró-ativa na tabela do Foundation para manter a consistência do design.
* Adicionado suporte para typeHint para salvar valores como string.
* Oferece segurança aprimorada para o serviço de preenchimento prévio da Forms
* Atualize para o arquivo adobe-reader-extensions-dsc.jar mais recente para ver as correções na extensão do Reader.
* O gancho de validação foi ajustado para considerar itens &quot;:inválidos&quot; para a entrada do número de aumento.

### Ativos {#assets-4}

* Os dados EmbedXMP são sempre definidos como &quot;ativos&quot; para o processo de geração de Ptiff. NPR-22776: Hotfix do CQ-4234498
* Não é possível definir vários valores padrão em campos de Vários valores. NPR-22900: Hotfix do CQ-4239000
* (Dynamic Media) Ao marcar a caixa de seleção Representações dinâmicas, o arquivo zip baixado gera a imagem TIFF original com um arquivo de zero byte. NPR-22410: Hotfix do CQ-4198471
* (Interface do usuário para toque) Local de upload padrão para ativos na visualização da coluna. NPR-23475: Hotfix do CQ-4237057

### Integração {#integration-5}

* No modo Público alvo, os autores podem modificar um componente herdado do blueprint sem cancelar a herança. NPR-22751: Hotfix do CQ-4237907
* A variável de caminho não é codificada corretamente, resultando em XSS (Cross site scripting, script entre sites) não persistente. NPR-22851

### MSM {#msm-1}

* Durante a implantação de um LiveCopy com várias configurações de implantação, se um ResourceNameConflict surgir abaixo da raiz, o fluxo de implantação será encerrado sem incluir todas as ramificações. NPR-22842: Hotfix do CQ-4236188

### Plataforma {#platform-3}

* Implemente um limite de pesquisa em uma solicitação para aplicação reversa. NPR-23351: Hotfix do Granite-21135****
* A alteração no padrão da mensagem não é refletida em loggers personalizados. NPR-23486: Hotfix do CQ-4241974

### Sites {#sites-4}

* A criação de um link em um texto de um Editor de Rich Text para um documento com espaços ou outros caracteres especiais não funciona. NPR-22289: Hotfix do CQ-4224321
* Salvar o segmento com um valor enorme (10000000000) define o aumento como 0, causando uma mensagem de erro. NPR-22524: Hotfix do CQ-4237006
* Não é possível clicar em Adicionar item no componente Multicampo. NPR-22552: Hotfix do CQ-4237404
* A barra de rolagem horizontal não fica visível quando o segmento tem um título longo. NPR-22615: Hotfix do CQ-4237001
* O carregamento de uma audiência vazia gera um código JavaScript incorreto. NPR-22974: Hotfix do CQ-4238734
* Ao programar uma ativação ou desativar o título do fluxo de trabalho é obrigatório, portanto, o título do fluxo de trabalho personalizado não é traduzido na linha do tempo. NPR-23121: Hotfix do CQ-4237552
* Solicitação de correções para problemas em segmentos de Públicos alvos em Sites. NPR-23128
* (Firefox) A caixa de seleção para a pessoa selecionada não é a correta. NPR-23345
* Os rótulos para os diferentes modos são exibidos junto com os ícones. NPR-23275
* Erro &#39;Valor inválido do seletor de recursão&#39; ao migrar um componente do AEM 6.0 para o AEM 6.2. NPR-23503: Hotfix para CQ-4241258

### Comunidades {#communities-1}

* As notificações por email e Web não são acionadas devido a falha de mensagem nos grupos. NPR-23447: Hotfix do CQ-4242880

### Tradução {#translation-1}

* As cópias de idioma do ativo estão sendo criadas quando o ativo &quot;Não traduzir&quot; está definido na configuração de tradução. NPR-22540: Hotfix do CQ-4237962

### Interface do usuário {#user-interface-1}

* Usar o Omnisearch com um query hyphen retorna um erro de servidor. NPR-22999: Hotfix do Granite-19674
* O DatePicker não suporta a definição manual de dicas de tipo externas definidas por campo oculto. Alterar a dica de tipo aciona um erro de conversão. NPR-23333: Hotfix do Granite-21194

### WCM - Componentes do Foundation {#wcm-foundation-components-2}

* O componente CAPTCHA foi descontinuado para melhor segurança, se você estiver usando o componente CAPTCHA, a mensagem &quot;O componente Captcha está obsoleto e não deve mais ser usado&quot;. será exibido após a instalação do 6.2 SP2-CFP15 ou versão posterior. AEM componente pode ser personalizado para incluir o reCAPTCHA para melhor segurança NPR-22151: Hotfix para CQ-4220052
* O componente &#39;Tabela&#39; do WCM Foundation está vulnerável a Scripts armazenados entre sites. NPR-23206: Hotfix do CQ-4240760

###  Vulnerabilidade{#vulnerability-2}

* Scripts entre sites (XSS) nos links de Projeto da interface do usuário do administrador. NPR-23272: Hotfix do CQ-4241795

## Forms {#forms-5}

### Pacote complementar do Forms {#forms-add-on-package-5}

#### Gerenciamento de correspondência {#correspondence-management}

* Quando uma letra é visualizada por pré-visualização padrão, o mapeamento do fragmento do layout não é exibido enquanto o mesmo é exibido corretamente quando clicado no botão pré-visualização. NPR-23335: Hotfix do CQ-4237745
* Os dados na letra correspondente aos vínculos definidos no XDP não são preenchidos usando o URL da letra direta. NPR-24145: Hotfix do CQ-4244290

#### Mobile Forms {#mobile-forms}

* (Gerenciamento de correspondência) Desalinhamento de dados ao carregar a carta com o XML do público alvo. NPR-22993: Hotfix do CQ-4237663

#### Reader Extensions Service {#reader-extensions-service}

* Não é possível aplicar a extensão do leitor no Adobe PDF. NPR-23067

#### Gerenciador do Forms {#forms-manager}

* O Forms incorporado ao Site não é publicado na republicação da Página do Site. NPR-23014: Hotfix do CQ-4236566

####  Vulnerabilidade{#vulnerability-3}

* Hotfixes proativos para script entre sites. NPR-20624: Hotfix do CQ-4206055
* Vulnerabilidade do Script entre sites (XSS) armazenada na guia Observações do Gerenciador de formulários. NPR-27157: Hotfix do CQ-4255556

#### Serviço de criptografia {#encryption-service}

* (OSGI) [JEE] Status de assinatura incorreto para PDF com anexo ao verificar o uso de &quot;Validar processo PDF&quot;. NPR-23269, NPR-23737

### Instalador do Forms JEE {#forms-jee-installer-5}

#### Núcleo {#core-1}

* Os problemas reportados na análise de código estático do Core-ext devem ser corrigidos. NPR-13947

#### Serviço PDFG {#pdfg-service}

* O conversor HTML para PDF não está funcionando. NPR-21545

### Pacotes OSGI e de conteúdo incluídos {#osgi-bundles-and-content-packages-included-4}

O texto seguinte documentos a lista dos pacotes OSGI e dos pacotes de conteúdo incluídos no CFP.

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP15

[Obter arquivo](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP15

[Obter arquivo](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Aprimoramento da capacidade de edição das propriedades de metadados dos ativos.
* O trabalho de Notificação de expiração de senha foi reconfigurado para ativos que já estavam vencidos.
* Console de interface de usuário de toque personalizada para estender locais adicionais.
* Atualização do cq-msm-core para uma sincronização eficiente do Livecopyindex.
* Funcionalidade de replicação simplificada para vários Rollouts.

### Ativos {#assets-5}

* Os usuários não conseguem baixar ativos com aviso de isenção de responsabilidade e nomes de arquivo longos. NPR-22163: Hotfix do CQ-4235274
* O caractere de aspas simples impede a atualização de metadados na visualização em massa e a interface do usuário é completamente quebrada quando você abre as propriedades de um ativo usando as ações rápidas da barra de ferramentas. NPR-22317, NPR-22353: Hotfix do CQ-4236990, CQ-4236469
* O trabalho de notificação de expiração de ativo não desativa os ativos expirados. NPR-22346: Hotfix do CQ-4237188
* O download de ativos falha ao usar o Gerenciamento de direitos digitais nos Ativos do Safari. NPR-22378: Hotfix do CQ-4236460
* A representação da Web para imagem pequena tem um tamanho de pixel impreciso. NPR-22435: Hotfix do CQ-4236742

### Sites {#sites-5}

* (Interface do usuário para toque) A tag movida é exibida em um novo e antigo local nas propriedades da página. NPR-21921, Hotfix para CQ-4238598
* (Interface do usuário para toque) O Editor de Rich Text remove todos os atributos, exceto a id da tag &lt;a>. NPR-22045: Hotfix do CQ-4234133
* Colar conteúdo diretamente no Editor de Rich Text usando CTRL+V ignora as quebras de linha. NPR-22117: Hotfix do CUI-5881
* (Interface do usuário de toque) Não é possível mostrar mais de 40 tags em namespace. NPR-22290: Hotfix do CQ-99114
* Problemas de RSS Feed, porta -1 a AEM 6.2 NPR-22158: Hotfix para CQ-4233339
* (IE) Ao criar qualquer caractere no campo Rich Text pela primeira vez, um espaço à direita é adicionado ao caractere. NPR-22443: Hotfix do CQ-4235343
* Ao tentar corresponder ao nome do pacote, o objeto Java Use congela SightlyJavaCompilerService devido a um caractere de espaço à direita na declaração do pacote. NPR-22557: Hotfix do Granite-20836
* O console Interface do usuário de toque não coleta novos idiomas para marcação. NPR-22250: Hotfix do CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) A data de publicação e a data de capa exigiam que os campos fossem definidos para os fólios antes de serem carregados no DPS. NPR-22484

### Commerce {#commerce}

* Várias vulnerabilidades de script entre sites (XSS) no assistente de criação de catálogo de comércio. NPR-22344: Hotfix do CQ-4237017

### MSM {#msm-2}

* A sincronização do LiveCopyIndex leva ao congestionamento de threads durante atualizações de índice longas. NPR-22214: Hotfix do CQ-90667
* a propriedade cq:cugEnabled é desativada quando outro campo em uma live copy é editado, portanto, desprotegendo a página. NPR-22246: Hotfix do CQ-4236050
* A ação de Roll-out de página falha ao atualizar filhos quando uma página é suspensa. NPR-22483: Hotfix do CQ-4236956
* A implantação de uma estrutura que foi movida em um lead principal leva a um cq:moveTarget errado. NPR-22373: Hotfix do CQ-4232536

### Integração {#integration-6}

* Tentar classificar ofertas na biblioteca do seletor de ofertas resulta em comportamento irregular. NPR-22208: Hotfix do CQ-4235439
* O TargetContentImpl deixa o AEM lento durante consultas de longa duração. NPR-22361: Hotfix do CQ-4236907
* O mecanismo do Target (mbox.js, at.js) não usa URLs danificados e usa URLs que contêm dois pontos, que podem falhar em determinadas implantações. NPR-22366: Hotfix do CQ-4237854
* A personalização da página exige a publicação diretamente no nó da marca. NPR-22370: Hotfix do CQ-4236895

### Foundation {#foundation}

* Os modelos Sightly de Scripting do Apache utilizam o pacote Provider **org.apache.sling.scripting.sightly.models.provider/1.0.18**. NPR-22614: Hotfix para Sling-5944, Sling-6866

### Projetos {#projects}

* O Workflow Starter não pode aceitar o valor TypeHint de String. NPR-22436: Hotfix do CQ-4237855

### Tradução {#translation-2}

* Investigue problemas com a funcionalidade Visualização. NPR-22201: Hotfix do CQ-4223753

### Interface do usuário {#user-interface-2}

* (Interface clássica) O componente exibe os valores padrão mesmo se o serviço de modelo de dados de formulário associado estiver definido como campo vazio. NPR-21903: Hotfix do GRANITE-19744

### WCM - Componentes do Foundation  {#wcm-foundation-components-3}

* Erro ao publicar uma página de Live Copy que aponta para uma página do Importador no Adobe Campaigns. NPR-22470: Hotfix do CQ-4237164
* Erros de JavaScript ao abrir o Editor de fragmentos de experiência. NPR-22598: Hotfix do CQ-4238415

### Fluxo de trabalho {#workflow}

* O Serviço de Notificação por E-mail do Fluxo de Trabalho do Day CQ aciona um e-mail por nó Mongo para notificações WorkflowCompleted e WorkflowAborted. NPR-22486: Hotfix do CQ-4238172

## Forms {#forms-6}

### Pacote complementar do Forms {#forms-add-on-package-6}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte Versões do AEM Forms.

#### Formulários adaptáveis {#adaptive-forms-4}

* Inconsistência no valor do espaço reservado suspenso no formulário adaptável no IE11 e Chrome. NPR-22405: Hotfix do CQ-4227096

### Instalador do Forms JEE {#forms-jee-installer-6}

#### Instalar o LCM {#install-lcm}

* Atualize Jars Jsafe para Cryptoj 6.1.3.1 no instalador e no LCM. NPR-22744

### Feature Packs incluídos {#feature-packs-included}

#### Gerenciamento de processos {#process-management}

* (Espaço de trabalho HTML) Quando um usuário reclama uma tarefa, a contagem de filas é atualizada para esse usuário específico, mas não para outros usuários, a menos que a página seja atualizada. NPR-19778: Hotfix do CQ-4233665

### Pacotes OSGI e pacotes de conteúdo incluídos no CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP14

[Obter arquivo](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP14

[O Get ](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
FileAEM Cumulative Fix Pack 6.2 SP1-CFP13 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Ativada a configuração do campo Parâmetro estático nas Configurações do componente do Público alvo ao usar o AT.js como biblioteca do cliente.
* Correções na funcionalidade mostrar/ocultar do componente suspenso.
* Correções para usar audiências de sincronização de públicos alvos.
* Mais versatilidade do Gerenciamento de correspondência para acomodar caracteres especiais.

### Ativos {#assets-6}

* A remoção da versão falha ao remover versões antigas de ativos. NPR-21682: Hotfix do CQ-4212996
* A reorganização de pastas em uma pasta reordenável não é persistente. NPR-21964: Hotfix do CQ-4231761

### Sites {#sites-6}

* (TouchUI)(ClassicUI) Várias vulnerabilidades de script entre sites (XSS) em HTL e componentes principais. NPR-21532: Hotfix do CQ-4232305 e CQ-4232511
* A criação/formatação de conteúdo (por exemplo, atribuição/remoção de novos estilos de lista) em um texto selecionado não funciona bem no Internet Explorer 11. NPR-21533: Hotfix do CQ-4230689
* (Safari) Os usuários não conseguem visualização de todos os ativos no painel do localizador de ativos. NPR-21981: Hotfix do CQ-4213720
* A Distorção de tempo retorna o erro &quot;RecursionTooDeepException&quot; com página distorcida e nenhuma nova versão é criada mesmo quando a data é alterada. NPR-21707: Hotfix do CQ-4199536
* Ao carregar uma página no editor, o WorkflowStatusProvider (pageinfo.json) é carregado três vezes, fazendo com que AEM instância execute lentamente. NPR-21778: Hotfix do CQ-59232

### Integração {#integration-7}

* A criação de audiências do tipo e navegador móveis no modo de criação de Públicos alvos não está funcionando no AEM. NPR-21676, NPR-21681: Hotfix do CQ-4232100
* Sob alta latência durante a atualização de um componente direcionado, é possível adicionar outra oferta antes que o componente seja atualizado completamente. NPR-21744: Hotfix do CQ-4233158/CQ-4234293
* Os usuários não podem ver valores de teste de Parâmetro estático na chamada da mbox que podem ser vistos ao testar o AT.js como a biblioteca do cliente na configuração da nuvem. NPR-21930: Hotfix do CQ-4234520

### Plataforma {#platform-4}

* Problemas de desempenho com a sincronização do usuário quando o número de usuários ou grupos é grande. NPR-20431: Hotfix do CQ-4223282
* Usuários não sincronizados com a Sincronização de usuários usando a Sling Distribution. NPR-21911: Hotfix do Granite-20404
* Impedindo que palavras de interrupção sejam realçadas em trechos de pesquisa (em uma página de Geometrixx). NPR-21835: Hotfix do Granite-21067\
   Observação: Essa correção exige o Oak CFP 1.4.20 ou superior.

### Tradução {#translation-3}

* a propriedade jcr está ausente para a ID de usuário do Iniciador ao criar o projeto de tradução. NPR-21715: Hotfix do CQ-4230713

### WCM - Componentes do Foundation {#wcm-foundation-components-4}

* A funcionalidade Mostrar/Ocultar do componente de formulário suspenso não está funcionando como esperado. NPR-22164: Hotfix do CQ-4235288

## Forms {#forms-7}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-7}

#### Formulários adaptáveis {#adaptive-forms-5}

* Injeção de entidade externa XML (XXE) no Forms adaptável. NPR-21982: Hotfix do CQ-109878
* (iOS11) Quando clicado no componente de anexo do arquivo, o anexo do arquivo abre a câmera em vez do navegador de arquivos do dispositivo. NPR-21926: Hotfix do CQ-4214348
* O título ausente na interface de usuário de criação de tema está causando exceção e falha na renderização da caixa de diálogo. Hotfix do CQ-4236143

#### Gerenciamento de correspondência {#correspondence-management-1}

* Problemas de renderização com dados xml contendo caracteres especiais. NPR-21712: Hotfix do CQ-4229137

### Instalador do Forms JEE {#forms-jee-installer-7}

#### Serviço de Assembler {#assembler-service}

* O arquivo PDF gerado usando o 6.2.0-ASM-1017-003 está corrompido. NPR-21427: Hotfix do CQ-4228046

#### Serviço PDFG {#pdfg-service-1}

* Falha de OCR devido ao tamanho inesperado da página (PDF) de arquivos PNG, JPEG e TIFF. NPR-19489: Hotfix do CQ-4209079

## Pacotes OSGI e pacotes de conteúdo incluídos no CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP13

[Obter arquivo](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP13

[Obter arquivo](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Manuseio de metadados aprimorado para campos multivalor.
* Suporte para códigos de países de múltiplos caracteres (mais de dois) em workflows de tradução.
* Melhoria na renderização de páginas com vários componentes aninhados.
* Sincronização aprimorada das datas de publicação para ativos entre AEM e Adobe Digital Publishing Suite.

### Ativos {#assets-7}

* Muitos caracteres no OmniSearch causa falha no servidor AEM. NPR-21083: Hotfix do CQ-4223602
* Os valores especificados na segunda opção em um Campo multivalor no Schema Metadados não são anexados aos valores especificados anteriormente no CRX-de. NPR-21220: Hotfix do CQ-4224526
* O download de ativos falha ao usar o Gerenciamento de direitos digitais nos Ativos do Safari. NPR-21387: Hotfix do CQ-4230287

### Sites {#sites-7}

* (DAM) (ClassicUI) Várias vulnerabilidades de script entre sites (XSS) em alguns arquivos SWF no início rápido AEM autor/publicação do CQ. NPR-21073, NPR-21074: Correção para NPR-20612
* O seletor de tags não traduz as tags disponíveis em vários idiomas.NPR-21221: Hotfix para CQ-78855
* A renderização de problemas com AEM console de artigos como o uso de vários componentes aninhados o torna lento. NPR-21271: Hotfix do CQ-4224158

### Integração {#integration-8}

* Ao adicionar uma estrutura de Público alvo, o modo de Definição de metas não está disponível na lista do modo de Seleção no editor. NPR-21047

### Dispositivo móvel sob demanda {#mobile-on-demand-1}

* (Digital Publishing Suite) As datas de publicação dos fólios no AEM não correspondem às datas que aparecem no Folio Producer. NPR-21145

### MSM {#msm-3}

* O processo de redefinição da Live Copy é interrompido após a exclusão da primeira página local no LC. NPR-21276: Hotfix do CQ-4229743

### Plataforma {#platform-5}

* A tag personalizada que faz referência a tags implementadas como script não é encontrada após a atualização para AEM 6.3. NPR-20149: Hotfix para Granite-18433

### Tradução {#translation-4}

* Os workflows de tradução falham com códigos lang_country com mais de 2 caracteres. NPR-21088: Hotfix do CQ-4197439
* A página do ativo não deve ser enviada novamente para um projeto de tradução até que o projeto seja concluído. NPR-21219: Hotfix do CQ-4209908

### Interface do usuário {#user-interface-3}

* Selecionar componente não exclui a propriedade de público alvo durante o envio do formulário. NPR-21163: Hotfix do GRANITE-14125
* O duplo de expansão HTTP.encodePathOfURI codifica o sinal de mais &#39;+&#39;. NPR-21417: Hotfix do GRANITE-16340

###  Vulnerabilidade{#vulnerability-4}

* Scripts entre sites (XSS) no editor de metadados DAM. NPR-21434: Hotfix do CQ-83472
* Vários arquivos SWF vulneráveis a scripts entre sites (XSS). NPR-20612: Hotfix do CQ-4213297

## Forms {#forms-8}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms  {#forms-add-on-package-8}

#### Gerenciamento de correspondência {#correspondence-management-2}

* (IE11) A renderização inicial do conteúdo HTML ocorre somente no lado esquerdo enquanto o lado direito é carregado intermitentemente após a UI completa ser carregada. NPR-21554
* O botão de envio de pré-visualização Carta é desativado após a instalação do AEM 6.2 SP1-CFP9. NPR-21547
* Ao selecionar o tipo de vínculo de ativo, a janela Seletor de ativo não é aberta no assistente para Editar vínculo de dados de carta. NPR-21164: Hotfix do CQ-4194567
* Para editar um módulo de texto incorporado ou editável, toque no ícone Editar relevante ou clique com o duplo no módulo de texto relevante na pré-visualização de letras. NPR-21402

#### Formulários adaptáveis {#adaptive-forms-6}

* O componente de botão Enviar do AEM Forms mostra type=&quot;button&quot; em vez de type=&quot;submit&quot;. NPR-21007
* Os dados permanecem persistentes ao adicionar ou excluir novos painéis para painéis repetíveis. NPR-21408

### Instalador do Forms JEE {#forms-jee-installer-8}

#### Núcleo {#core-2}

* A atualização para o Java 8 Update 131 mais recente gera uma exceção: &quot;O provedor JsafeJCE está desativado, uma verificação de autointegridade exigida FIPS 140 falhou.&quot; NPR-21355

   **Observação:** este NPR requer configurações adicionais; para obter detalhes, consulte a atualização [ ](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr)mais recente do Java 8.

* Atualize jars jsafe para cryptoj 6.1.3.1 em Core, Encryption, Signature &amp; Documento Security. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Instalar o LCM {#install-lcm-1}

* Atualize Jars Jsafe para Cryptoj 6.1.3.1 no instalador e LCM. NPR-21362

#### Serviço PDFG {#pdfg-service-2}

* Atualize Jars Jsafe para Cryptoj 6.1.3.1 em PDFG. NPR-21359

#### Gerenciamento de processos {#process-management-1}

* (Espaço de trabalho HTML) Habilitar o redimensionamento de colunas para que a categoria de nomes não apareça truncada. NPR-19770: Hotfix do CQ-4233668

#### Reader Extensions Service {#reader-extensions-service-1}

* Atualize jars jsafe para cryptoj 6.1.3.1 em RE. NPR-21357

## Pacotes OSGI e de conteúdo incluídos no CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP12.1

[Obter arquivo](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2 SP1-CFP12.1

[Obter arquivo](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Atualização do cq-msm-core para uma sincronização eficiente do Livecopyindex.
* Melhoria na eficiência da edição de fragmentos de conteúdo.
* Fornece a opção de validação no gerenciador de pacotes para detectar permissões de ACL.
* Introduziu a capacidade da Campanha de incluir ID de e-mail para correspondência do cliente.
* Aprimoramento das capacidades de codificação de vídeo para arquivos Dynamic Media.
* Correções no componente Sightly e no LiveCopies.

### Ativos {#assets-8}

* Falha na codificação de vídeo do Dynamic Media para arquivos que incluem espaços em seus nomes. NPR-20818: Hotfix do CQ-102469
* Várias vulnerabilidades de script entre sites (XSS) em alguns arquivos SWF no início rápido AEM Autor/Publicação do CQ. NPR-21071, NPR-21072
* Os usuários não conseguem baixar ativos com aviso de isenção de responsabilidade e nomes de arquivo longos. NPR-20255: Hotfix do CQ-4222139

### Sites {#sites-8}

* Integração de AEM e Campanha: Links especiais são regravados no Adobe Campaign, impedindo que os clientes enviem correio para: hiperlinks em seus emails. NPR-20787: Hotfix do CQ-4225760
* (Interface do usuário para toque) AEM problemas de usabilidade e desempenho quando o idioma é definido como francês. NPR-20854: Hotfix do CQ-4227628
* Vincular um arquivo de ativo codificado usando o plug-in de link no RTE retorna um link vazio. NPR-20626, NPR-21059: Hotfix do CQ-4223011
* O editor de metadados do fragmento de conteúdo impede que os autores de conteúdo salvem alterações nos Fragmentos de conteúdo. NPR-20641: Hotfix do CQ-4224755
* Alias de propriedade da página leva à Solicitação de publicação/Solicitação de cancelamento de publicação. NPR-20731: Hotfix do CQ-4226227
* Problemas de componente de texto com a codificação do link no elemento RTE. NPR-20755: Hotfix do CQ-4224321

### Plataforma {#platform-6}

* ResourceResolverImpl.map() não chama ResourceDecorator. NPR-20788: Hotfix do GRANITE-19718
* org.apache.sling.i18n.DefaultLocaleResolver não consegue processar solicitações via org.apache.sling.engine.SlingRequestProcessor. NPR-20706: Hotfix do CQ-94880
* Solicite a adição de uma opção de validação no Gerenciador de pacotes para detectar se quaisquer permissões/privilégios de ACL foram alterados em um pacote específico. Hotfix do CQ-4229196

### Integração {#integration-9}

* (Search &amp; Promote) A definição ambígua de filtro para o pacote de conteúdo leva a caminhos substituídos na instalação. NPR-20808: Hotfix do CQ-4227615

### Fluxo de trabalho {#workflow-1}

* Problemas de estabilidade com a implantação do servidor de produção do AEM. NPR-20979: Hotfix do Granite-19104

### Projetos {#projects-1}

* (Interface do usuário para toque) Não é possível adicionar membros do grupo a um projeto. NPR-20990: Hotfix do CQ-4205375

### WCM-Componentes do Foundation {#wcm-foundation-components-5}

* O componente de imagem Sightly &#39;link to&#39; gera um erro 403 devido à extensão .html ausente. NPR-20823: Hotfix do CQ-4195909
* Em um site de blueprint usando o LiveCopy, tentar excluir um componente de formulário lança uma NullPointerException e adiciona o componente de formulário em vez de excluí-lo. NPR-20855: Hotfix do CQ-4204628
* A sincronização do LiveCopyIndex leva ao congestionamento de threads durante atualizações de índice longas. NPR-20634: Hotfix do CQ-90667

### Segurança {#security}

* Atualização proativa da biblioteca XSS. NPR-21174
* Atualize para o Apache Commons Email 1.5, que apresenta uma API simplificada para enviar e-mails. NPR-20509: Hotfix do Granite-18240
* Correção de segurança aplicada à API de proteção do Apache Sling XSS para eliminar a possibilidade de ignorar XSS. NPR-21290: Hotfix do GRANITE-19924
* Bypass XSS na função XSSAPI#getValidHref. NPR-21174: Hotfix do Granite-19924

### Aplicativos móveis {#mobile-apps}

* Correção de problemas com solicitações curl Head para ativos OOTB no AEM. NPR-20511: Hotfix do CQ-4221520 e CQ-103024

## Forms {#forms-9}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte Versões do AEM Forms.

Os principais destaques do AEM Forms são:

* Ativação da autenticação de certificado para usuários do Workbench.
* Correções de usabilidade para o Gerenciamento de correspondência, formulários HTML5 e área de trabalho do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-9}

#### Formulários HTML5 {#html-forms-1}

* Problemas de usabilidade com componentes de script em dispositivos iOS 10 e 11. NPR-21092

#### Gerenciamento de correspondência {#correspondence-management-3}

* (Interface do usuário de correspondência) Desative o botão Enviar após um clique. NPR-21078

### Instalador do Forms JEE {#forms-jee-installer-9}

#### Serviço de Assembler {#assembler-service-1}

* o docConvertor não produz PDF/A com o erro &quot;O prefixo &quot;stEvt&quot; do elemento &quot;stEvt:action&quot; não está vinculado&quot;. NPR-21032: Hotfix do CQ-4222540
* Uma exceção é lançada com o nome java.lang.IllegalArgumentException mensagem:Nenhuma constante enum com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE ao chamar o serviço OMPFSubmission/PDFA/PDFtoPDFA. Isso impede que o processo de verificação de assinatura de vida curta seja concluído até que o servidor seja reiniciado. NPR-20792

#### Workbench {#workbench}

* Habilitar autenticação de certificado para usuários do Workbench. NPR-17548: Hotfix do CQ-4214486

#### Gerenciamento de processos {#process-management-2}

* O processo de preparação de dados chama várias vezes quando o formulário móvel é renderizado com parâmetros dataref. NPR-19801: Hotfix do CQ-4230427: CQ-4230400

## Pacotes OSGI e pacotes de conteúdo incluídos no CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP11

[Obter arquivo](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2 SP1-CFP11

[Obter arquivo](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Adicionada uma nova função de utilitário onDialogLoaded para testes.
* Adicionados testes e configurações de unidade de front-end ao ClientLibraryProxyServlet.
* Correções de desempenho no componente do editor de várias imagens no local.
* Atualizações de configuração no Apache Sling JCR ResourceBundleProvider.

### Ativos {#assets-9}

* A pré-visualização de ativos não funciona se os workflows de atualização de ativos estiverem desativados. NPR-20543: Hotfix do CQ-4204986
* Problemas de renderização com a classe adicionada ao granito: propriedade class (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix do CQ-4219238
* Os ativos em miniatura com caracteres especiais no título mostram o objeto java no atributo alternativo de NPR-20347: Hotfix para CQ-4223620
* Substituição do código de comparação de versão pelo código proprietário da Adobe devido a problemas de licenciamento. NPR-20273: Hotfix do CQ-4223758
* Problemas de processamento ao carregar arquivos CMYK PSB com várias camadas alfa. NPR-20251: Hotfix do CQ-4220869
* Os dicionários de internacionalização não funcionam a menos que o servidor seja reiniciado em org.apache.sling.i18n 2.5.6. NPR-20525: Hotfix para Granite - 19490
* Nenhum despejo de thread está sendo gerado de acordo com o período de scheduler com a configuração padrão do Coletor de Thread Dump (start AEM padrão). NPR-20288: Hotfix para GRANITE-19488 / GRANITE-12741 / CQ-90647.

### Sites {#sites-9}

* Se o filtro de datas modificado for alterado depois de abrir a pesquisa salva, não haverá efeito nos resultados e os resultados exibidos serão os mesmos que o valor salvo anterior do filtro de datas modificado. NPR-19739: Hotfix do CQ-4219425
* Falha ao carregar páginas com componentes aninhados. NPR-20312
* O fluxo de trabalho de solicitação de exclusão é acionado na exclusão de pacotes de fluxo de trabalho. NPR-20266: Hotfix do CQ-4221686
* (Interface do usuário para toque) Problema com Copiar/Colar com a área de transferência do SO e a área de transferência interna AEM. NPR-20228: Hotfix do CQ-4220383
* AEM instância fica lenta com a visualização de lista quando vários ativos (mais de 100) estão sendo carregados. NPR-20034: Hotfix do CQ-4222695
* (Interface do usuário de toque) A exclusão de inicializações por meio do console da interface do usuário clássica torna todas as páginas não editáveis. NPR-20520: Hotfix do CQ-4225074
* A lista suspensa público alvo não funciona com vários componentes de RTE em uma caixa de diálogo. NPR-20345: Hotfix do CQ-4220981

### Plataforma {#platform-7}

* Quando acessado usando uma sessão anônima, ClientLibraryProxyServlet não faz solicitações de proxy para bibliotecas clientes na instância de publicação e lança um erro HTTP 404 não encontrado. NPR-20195: Hotfix do Granite-14409

### Integração {#integration-10}

* Selecionar o mecanismo de público alvo como Adobe Target impede que o componente seja carregado e emite um erro no log do servidor. NPR-20058: Hotfix do CQ-88071, CQ-109698, CQ-4201600

### Comércio {#commerce-1}

* Nenhuma mensagem de pop-up de confirmação ou redirecionamento é exibida ao criar produtos da mesma página. NPR-20257: Hotfix do CQ-4223414

### Interface do usuário {#user-interface-4}

* Quando o Datepicker é um campo em vários campos, os valores salvos nos campos de data não são persistentes durante a edição do componente. NPR-20077: Hotfix do GRANITE-19147
* As consultas anteriores não são abortadas caso consultas consecutivas sejam acionadas, resultando em resultados incorretos. NPR-20397: Hotfix do GRANITE-19306

### WCM - Componentes do Foundation {#wcm-foundation-components-6}

* A propriedade ImageMap ainda existe mesmo depois de remover as imagens do componente Editor de várias imagens no local. NPR-20142: Hotfix do CQ-4222982

## Forms {#forms-10}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms  {#forms-add-on-package-10}

#### Formulários adaptáveis {#adaptive-forms-7}

* valueCommit Script é executado duas vezes para DropDownList quando alterado pela interface do usuário. NPR-19989: Hotfix do CQ-110212

### Instalador do Forms JEE {#forms-jee-installer-10}

**Gerenciamento de processos**

* O pacote CFP contém AEM Forms HTML Workspace versão 2.2.26. NPR-2009
* O formulário pré-preenchido não funciona quando o formulário móvel é configurado para visualização como PDF. NPR-20566

**Rights Management**

* A caixa de diálogo Seleção de Certificado de Autenticação Mútua/CAC deve exibir certificados com EKU (Enhanced Key Usage) como autenticação de cliente ou logon de cartão inteligente. NPR-20708
* O Forms JEE é compatível com autenticação mútua PKCS#11. NPR-15001

## Pacotes OSGI e pacotes de conteúdo incluídos no CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Lista de pacotes OSGi incluídos AEM CFP 6.2 SP1-CFP10

[Obter arquivo](assets/do-not-localize/bundle-list-cfp10.txt)

Lista de pacotes de conteúdo incluídos no AEM CFP 6.2 SP1-CFP10

[Obter arquivo](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Configuração da interface clássica do Analytics adaptada para entrada secreta.
* Correções para o cache de persistência independente do Contexthub.
* Cálculo preciso das dimensões do Ativo.
* Otimização do desempenho AEM ao publicar ativos no Brand Portal.
* Correções no valor Tipo de recurso no nó da tela.
* Ativada a funcionalidade de pesquisa de caracteres especiais e sensíveis a maiúsculas e minúsculas para o conteúdo do fragmento do documento.
* Aprimoramento do Forms adaptativo para anexar PDF como anexos no Safari.\
   Fornece um novo Dynamic Media que se conecta à nova Dynamic Media Publishing Infrastructure para obter replicação mais rápida e escalonável.

### Ativos {#assets-10}

* A AEM Assets não consegue extrair referências de subativo para ativos do InDesign, incluindo links de duplicado para o ativo. NPR-19006: Hotfix do CQ-4204186
* A opção Classificar não está funcionando para ativos dentro da coleção em Comércio. NPR-19508: Hotfix do CQ-4213622
* Quando um ativo com o mesmo nome de um ativo pré-existente é movido para o mesmo local, o valor de cq: lastReplicationAction para os ativos é trocado entre si, o que resulta na criação de metadados errados. NPR-19531
* Uma mensagem de erro é exibida ao publicar um grande número de ativos, apesar de todos os ativos terem sido publicados corretamente. NPR-19629: Hotfix do CQ-4219611
* As representações estáticas são listadas com dimensões fixas e não refletem o tamanho da representação real. NPR-20004
* A instância do AEM fica lenta quando vários ativos (mais de 4) são publicados no Brand Portal. NPR-20009

### Sites {#sites-10}

* AEM exibe um comportamento inesperado quando um usuário tenta publicar/desfazer a publicação/criar uma versão de uma página bloqueada por outro usuário. NPR-19249; Correção para CQ-4215298 e CQ-4203856
* Ao promover a inicialização aninhada manualmente, a página secundária é excluída. NPR-19704
* Problemas de persistência quando o ContextHub armazena a camada de persistência padrão durante a inicialização. NPR-19979: Hotfix do CQ-4218399
* Os fragmentos de conteúdo são sobrepostos com outros botões. NPR-19980: Hotfix do CQ-4221519
* A página do site não é exibida quando visualizada usando o alias no SiteAdmin. NPR-20053: Hotfix do CQ-4221478
* Erro ao publicar uma página de Live Copy que aponta para uma página do Importador no Adobe Campaigns. NPR-20066: Hotfix do CQ-4220846

### Plataforma {#platform-8}

* Atualização do POI do Apache para a versão 3.16 para oferecer suporte à inclusão da imagem de plano de fundo dos slides PPT nas execuções. NPR-18286
* Problemas de renderização com o Internet Browser 11 e o Edge ao carregar vários ativos na mesma pasta. NPR-20062

### Integração {#integration-11}

* O arquivo at.js personalizado não é publicado quando acessado com o usuário anônimo. NPR-19542: Hotfix do CQ-4219592
* Migração de credenciais existentes do Analytics para a Autenticação WSSE. NPR-19962

### Brand Portal {#brand-portal}

* Ativação da ação Publicar tags do AEM no Brand Portal a partir do console tagadmin/tagging. NPR-20271

## Forms {#forms-11}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms  {#forms-add-on-package-11}

#### Gerenciamento de correspondência {#correspondence-management-4}

* Ativada a funcionalidade para pesquisar o texto real em fragmentos de documento quando uma carta é visualizada. NPR-19712

#### Formulários adaptáveis {#adaptive-forms-8}

* Aprimoramento do Forms adaptativo para anexar PDF como anexos no Safari. Para suportar o mesmo recurso em formulários existentes, precisamos fazer com que a alteração na configuração no widget anexo e em &quot;Tipos de arquivo suportados&quot; atualize o valor application/pdf em vez de .pdf. NPR-19623

#### Gerenciador do Forms {#forms-manager-1}

* Se validationState for indefinido em um campo de formulário adaptável e o evento elementFocusChanged ocorrer, um evento de erro (errorState) será retornado ao servidor Adobe Analytics. NPR-19513

### Instalador do Forms JEE {#forms-jee-installer-11}

#### Núcleo {#core-3}

* O gerenciador de conexões não está disponível durante o encerramento. O chefe corta a dependência do JDBC antes que o autor da EAR seja desimplantado, causando problemas de corrupção. NPR-19703

## Feature Packs incluídos {#feature-packs-included-1}

* Correção de miniaturas e melhorias de transparência no Dynamic Media. NPR-15207

## Pacotes OSGI e de conteúdo incluídos no CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP9

[Obter arquivo](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Lista de pacotes OSGi atualizados no AEM 6.2SP1-CFP9

[Obter arquivo](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Introdução de tags a modelos de usuário personalizados no Serviço de modelo de e-mail do Adobe.
* Aprimoramentos de botões TouchUI no aplicativo para desktop.
* Desativado o botão Enviar ao clicar para impedir vários envios de formulário em uma página de tradução.
* Configurados vários componentes do RTE em uma caixa de diálogo.
* Atualizações de referência reforçadas em live copy.
* Ativada a funcionalidade de pesquisa que diferencia maiúsculas e minúsculas para o conteúdo do fragmento do documento.
* Adicionada a lista de bibliotecas Linux à documentação de instalação do AEM Forms.

### Ativos {#assets-11}

* Problemas com a aplicação do Filtro Omnisearch em coleções inteligentes no navegador Safari. NPR-19511
* Os metadados de palavras-chave do PDF não são extraídos e são modificados incorretamente quando há várias palavras-chave associadas a um Ativo PDF. Para solucionar o problema, a propriedade de metadados do campo Assunto foi removida para Ativos PDF. No entanto, é possível editar o esquema de metadados para adicionar um campo de texto de vários valores ao campo Assunto. NPR-19126
* O serviço de notificação de fluxo de trabalho não codifica os links no email, o que os impede de carregar depois que os usuários clicam neles. NPR-19490: Hotfix do CQ-4218055
* Não é possível carregar a lista completa de páginas/ativos na exibição em Coluna usando o Chrome. NPR-19458: Hotfix do CQ-4214248
* O ícone Incorreto de Tempo desligado é exibido AEM caixa de entrada ao ativar o fluxo de trabalho &quot;Solicitar Ativação&quot;. NPR-19365: CQ-4216174
* Problemas com a classificação na visualização da lista. NPR-19217: CQ-95602
* Ao alterar o título ou a imagem em miniatura nas configurações da Pasta de ativos, o grupo original e as permissões da pasta são substituídos. NPR-19283: Hotfix do CQ-4216080
* As estações de trabalho do Windows 10 alternam automaticamente para o Modo de toque, desabilitando o funcionamento de alguns botões. NPR-19183

### Sites {#sites-11}

* Problemas com a presença de vários componentes do RTE em uma caixa de diálogo. NPR-19311: NPR-19587
* A limpeza automática de versão no vanilla AEM 6.2 só funciona uma vez depois que o VersionManagerImpl é inicializado. NPR-19315: Hotfix do CQ-4217175
* A instância do fluxo de trabalho fica presa na etapa do fluxo de trabalho &quot;Exportação do Salesforce.com&quot;. NPR-19222: Hotfix do CQ-4212976
* As páginas de cópias de idioma criadas a partir de cópias online não são editáveis. NPR-18967
* ReferencesUpdateAction falha ao atualizar Links em um LiveCopy aninhado com alteração de hierarquia. NPR-18715: Hotfix do CQ-4214105

### Plataforma {#platform-9}

* O serviço Modelo de email da Adobe adiciona tags a modelos de usuário personalizados. NPR-19190: Hotfix do CQ-4217113

### Projetos {#projects-2}

* Os editores de projeto não conseguem copiar/colar ativos na pasta de ativos do projeto. NPR-19619
* Não é possível gerar pré-visualização para projetos de Tradução após a instalação do 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integração {#integration-12}

* Acesse as propriedades dos artigos que estão sendo definidos incorretamente na Adobe Digital Publishing Solution, na interface do usuário clássica. NPR-19366
* Suavize a renderização de miniaturas devido a artigos em tamanho normal no console AEM artigo. NPR-19086: CQ-4217148
* Comportamento incorreto de dobramento automático ao personalizar ofertas por meio do Campaign se os usuários tiverem acesso a várias áreas. NPR-19290: Hotfix do CQ-4218029
* A caixa de diálogo de direcionamento não é exibida no modo de direcionamento quando um módulo de destino é editado e salvo mais de uma vez. NPR-19144: Hotfix do CQ-4216708

### Fluxo de trabalho {#workflow-2}

* Os usuários não conseguem filtrar notificações na Caixa de entrada por usuário/grupo na interface clássica da caixa de entrada. NPR-19122: Hotfix do CQ-4215374
* O Mapa de imagem não retém as coordenadas selecionadas no componente de imagem HTL. NPR-18911: CQ-4211584

## Forms {#forms-12}

* As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-12}

* Quando o conteúdo é copiado do Microsoft Word ou de um navegador da Web para o editor de texto do gerenciador de correspondência, o estilo é perdido. NPR-19530
* O conteúdo sem quebra de linha do Editor de texto não quebra. NPR-19481
* Ativada a funcionalidade para pesquisar o texto real em fragmentos de documento quando uma carta é visualizada. NPR-17792: Hotfix do CQ-4214501

#### Gerenciamento de correspondência {#correspondence-management-5}

>[!NOTE]
>
>Esta funcionalidade de pesquisa para fragmentos de texto tem algumas restrições:-
>
>* O conteúdo do fragmento do documento faz distinção entre maiúsculas e minúsculas e os títulos não fazem distinção entre maiúsculas e minúsculas.
>* Os resultados da pesquisa não são destacados quando parte da palavra pesquisada está em um estilo diferente ou contém um caractere especial como &quot; ou &quot; ou &quot; ou \.
>* A pesquisa não funciona para conteúdo dinâmico (como valores de elementos do dicionário de dados ou valores de variáveis) no fragmento do documento.


#### Gerenciador do Forms {#forms-manager-2}

* As propriedades do Schema XML do Adaptive Forms não podem ser editadas após a aplicação do CFP6 no AEM 6.2. Hotfix para CQ-4219684
* Todos os serviços do pacote principal do AEM Forms Manager não são iniciados ao reiniciar o servidor. Hotfix do CQ-4217014

### Instalador do Forms JEE {#forms-jee-installer-12}

#### Instalar o LCM {#install-lcm-2}

* A tela Administrador no Microsoft Windows exibe a versão 6.0 após a instalação do CFP6. Hotfix do CQ-4217573

## Feature Packs incluídos {#feature-packs-included-2}

* Aprimoramentos de botões TouchUI no aplicativo para desktop. NPR-18676

## Pacotes OSGi incluídos no CFP8 {#osgi-bundles-included-in-cfp}

Lista de pacotes OSGi atualizados no AEM 6.2SP1-CFP8

[Obter arquivo](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP8

[Obter arquivo](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Alteração de comportamento na exibição de títulos no Cartão de imagem para Imagem com dc: propriedade title definida como String [] (vários campos).
* Correções no problema de desempenho com Cloud Services Dynamic Media, interface de usuário de toque e de segurança.
* Correções no Apache Felix Http Bridge 3.0.8
* Solução da replicação sem binários (BLR) entre o ambiente de autor e publicação.
* Suporte para o arquivo da Biblioteca de públicos alvos, AT.JS, uma biblioteca de implementação para integração do cliente com a Adobe Target projetada para implementações típicas da Web e aplicativos de página única.
* Desempenho AEM aprimorado ao introduzir o tempo limite de conexão configurável pelo usuário para soluções de Marketing Cloud (Analytics, DTM, Público alvo e S&amp;P).

### Ativos {#assets-12}

* Durante o teste da ingestão de vídeo com AEM 6.3 configurados com Cloud Services Dynamic Media, a exceção &quot;Muitos arquivos abertos&quot; é causada. NPR-18734; Hotfix para CQ-4211407
* A configuração do URL personalizado para ativos em uma página não funciona após reiniciar a instância do AEM. NPR-18634; Hotfix para Granite-18085
* Na TouchUI, o botão Publicar é exibido para usuários sem permissão para publicar ativos. NPR-18620; Hotfix para CQ-4214042
* A opção de representação dinâmica não está presente na caixa de diálogo de download de um ativo depois que o contrato de licença é definido para ele. NPR-18607; Hotfix para CQ-4212342
* A representação dinâmica não pode ser baixada para ativos que incluem espaços em seus nomes. NPR-18571; Hotfix para CQ-4211738
* Não é possível salvar mais de um usuário ao compartilhar a pasta de ativos com a Creative Cloud. NPR-18489; Hotfix para CQ-103297
* dc: título &amp; dc: a descrição não é alterada para um valor de vários campos em crx/de. NPR-18474; Hotfix para CQ-4209086
* A operação de mover ativos causa degradação do desempenho. NPR-18346
* Nenhum item é exibido na Linha do tempo quando é aberto com o conjunto de opções padrão Mostrar tudo. NPR-18302; Hotfix para CQ-4211957
* Ocorre um erro quando um arquivo de texto ASCII/UTF-8 codificado é carregado no AEM Assets e a geração de miniaturas falha. NPR-18006: CFP do CQ-4209345
* Os botões de ação Publicar ficam visíveis mesmo quando o usuário não tem acesso de replicação. NPR-17353; Hotfix para CQ-4209269
* O Siteadmin e o Miscadmin não funcionam quando a miniação é ativada usando min:gcc;obfuscate=true. NPR-18593; Hotfix para CQ-4209220
* Os itens de menu personalizados não aparecem até que a tela seja atualizada sempre. NPR-18500; Hotfix para CQ-4213581
* Atualize o arquivo Moment.js para 2.10.6. NPR-18596; Hotfix para Granite-11881
* A aplicação de permissões para macros DM quebra a visualização para o usuário administrativo. NPR-18544; Hotfix para CQ-4211729
* Publicar mais tarde para ativos está lançando ArgumentException ilegal. CQ-4214532

### Sites {#sites-12}

* Em um cluster de autor ativo-ativo com MongoDB, ambos os autores tentam disparar a replicação para o mesmo conteúdo, quando o tempo atinge o Tempo inativo definido para o conteúdo. NPR-18708; Hotfix para CQ-4210982
* NPE ao mover um recurso com uma referência que não tem jcr: nó de conteúdo. NPR-18664
* Os espaços reservados não estão visíveis em uma página que contém vários componentes parsys. NPR-18645; Hotfix para CQ-110253
* Problemas de simultaneidade em AbstractCopyMoveCommand. NPR-18591
* Ao copiar texto para um componente parsys de outra instância AEM, parsys é criado sem qualquer conjunto resourceType. NPR-18511; Hotfix para CQ-4212306

### Plataforma {#platform-10}

* O instalador do JCR não atualiza a versão do pacote após a instalação do pacote. NPR-18728; Correção para NPR-15135
* A replicação sem binários (BLR) falha com o ambiente de autor e publicação de binários. NPR-18704
* Solicitação de resolução da ponte Apache Felix Http em AEM ambiente. NPR-18297
* A replicação falha quando várias páginas com uma estrutura semelhante são replicadas simultaneamente com o Sling Content Distribution. NPR-18665; Hotfix para Granite-13712
* Construção de pacotes de distribuição de venda e não de limpeza automática. NPR-18601; Hotfix para Granite-16183

### Integração {#integration-13}

* Exibir ofertas publicadas de pastas de biblioteca resulta em NPE. NPR-18732; Hotfix para CQ-4214593
* A data de start/término de uma atividade não é atualizada no JCR e no Público alvo quando alterada de uma data específica para &quot;Quando ativada/desativada&quot;. NPR-18612; Hotfix para CQ-104831
* A integração do Analytics com AEM não tem tempo limite de conexão ou soquete definido para as conexões httpclient. NPR-18497
* A integração do DTM com o AEM não tem tempo limite de conexão ou soquete definido para as conexões httpclient. NPR-18495
* A integração do Público alvo com o AEM não tem tempo limite de conexão ou soquete definido para as conexões httpclient. NPR-18494
* A integração do Search &amp; Promote com o AEM não tem nenhum tempo limite de conexão ou soquete definido para as conexões httpclient. NPR-18493
* A atividade do público alvo é desativada após adicionar uma experiência extra. NPR-18227; Hotfix para CQ-4201895

### WCM-Componentes do Foundation {#wcm-foundation-components-7}

* Os mapas de imagem não retêm as coordenadas selecionadas no componente de imagem HTL. NPR-18530; Hotfix para CQ-4211584

### Tradução {#translation-5}

* Os resultados da pesquisa de tradução não incluem nomes de projetos de tradução. NPR-18224; Hotfix para CQ-4210658

### Portal de marcas {#brand-portal-1}

* Ativação da ação Publicar tags do AEM no Brand Portal a partir do console tagadmin/tagging. CQ-4212165

## Forms {#forms-13}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-13}

#### Gerenciamento de correspondência {#correspondence-management-6}

* Os dados corretos não são exibidos no painel de edição até que o fragmento seja salvo. NPR-19092
* A adição do fragmento do documento a uma letra leva bastante tempo. NPR-18958
* Se existir uma declaração XML em um arquivo xml de dados e a representação de carta for iniciada por meio de uma solicitação de POST, a carta correspondente não exibirá os dados. NPR-18870
* Nenhum log de auditoria é gerado para ações realizadas em ativos do CM. NPR-16618

>[!NOTE]
>
>Não instale este Pacote de complementos CFP se você for afetado com os dois problemas abaixo:
>
>* Copiar Colar do Word / Web para o Editor de texto CM mostra o conteúdo de quebra de linha. NPR-19530
>* O conteúdo sem quebra de linha no Editor de texto CM não quebra. NPR-19449

>
>
Estas questões seriam abordadas na futura PCP.

#### Formulários adaptáveis {#adaptive-forms-9}

* Ao adicionar um novo painel para painéis repetíveis, o valor do campo suspenso no painel anterior é excluído. NPR-18772
* Campos de formulário adaptáveis marcados para aceitar apenas números inteiros também aceitam alguns caracteres especiais do teclado numérico. NPR-18680
* Script para alterar o título do botão no evento initialize do painel guideroot não está funcionando. NPR-18476
* A barra de rolagem não é vista no painel direito para regras criadas no editor de regras. NPR-18716

#### Aplicativo AEM Forms {#aem-forms-app}

* O Forms não é renderizado corretamente no aplicativo AEM Forms quando ele está no modo offline ou não está conectado à rede. CQ-4218368

### Instalador do Forms JEE  {#forms-jee-installer-13}

#### Serviço PDFG {#pdfg-service-3}

* O Gerador de PDF não produz documentos PDF com níveis de marcadores especificados. Hotfix do CQ-4211102

## Pacotes OSGi incluídos no CFP7 {#osgi-bundles-included-in-cfp-1}

Lista de pacotes OSGi atualizados no AEM 6.2SP1-CFP7

[Obter arquivo](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP7

[Obter arquivo](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Gerenciamento eficiente de componentes ocultos no modo de layout no tablet.
* Apresentando Quickactions em dispositivos híbridos.
* Resolução de problemas de sincronização de nível de componente com cópias online.

### Ativos {#assets-13}

* O cliente é bloqueado quando o usuário que não tem a permissão necessária tenta mover a operação em um ativo. NPR-18330; Hotfix para CQ-4212560
* A mesclagem de várias configurações de serviços de conteúdo inteligente causa problemas de usabilidade. NPR-18273; Hotfix para CQ-4201557
* As ações/Workflows de finalização de compra não estão disponíveis no console Linha do tempo uma vez por aprox. 80 fragmentos são adicionados na pasta Ativos. NPR-18257; Hotfix para CQ-4211214 e NPR-18251; Correção para CQ-4211216.
* O sistema falha em falta de memória e carece de paginação durante os relatórios de Ativos. NPR-17865; Hotfix para CQ-4209759
* Falha na reprodução do vídeo publicado no ativo de vídeo codificado. NPR-17849; Hotfix para CQ-4210739
* A miniatura do PDF não é gerada. NPR-17831, NPR-17750; Hotfix para CQ-4210547
* Os ativos expirados não são desativados pelo trabalho de Notificação de expiração do Adobe CQ DAM. NPR-17666; Hotfix para CQ-107766
* As atividades de expiração de ativos param se um ativo não tiver um proprietário atribuído. NPR-17665; Hotfix para CQ-4197946
* Uma exceção de ponteiro nulo é gerada quando uma pasta de ativo com mais de 150 referências recebidas é movida. CQ-4200981

### Sites {#sites-13}

* A personalização funciona somente para o primeiro IP quando a regra de segmentação é definida para um intervalo de IP. NPR-18121; Hotfix para CQ-83767
* Falha de logon devido a NumberFormatException quando a propriedade historyShow está ativada. NPR-18073; Hotfix para CQ-101965
* As páginas excluídas marcadas estão visíveis na interface de usuário para toque. NPR-18025; Hotfix para CQ-86694
* Problemas de desempenho ao carregar uma página com públicos-alvo grandes (mais de 2000). NPR-17884; Hotfix para CQ-4209567
* Não é possível selecionar uma imagem depois de remover outras imagens na página. NPR-17711; Hotfix para CQ-4201323

### Plataforma {#platform-11}

* Os controles de interface de toque não estão ocultos para usuários que não têm as permissões necessárias. NPR-17945; Hotfix para CQ-4211231
* Tags japonesas ausentes no campo do seletor. NPR-17768; Hotfix para CQ-4210456
* O query getsize() retorna resultados incorretos quando FastQuerySize está ativado. NPR-18018
* O console da Web na instância standby não está acessível. NPR-17861; Hotfix para Granite-14582

### Comércio {#commerce-2}

* A travessia do query ocorre quando o diagrama do catálogo não tem nenhuma condição definida para uma seção. NPR-18229; Hotfix para CQ-4211924

### Comunidades {#communities-2}

* PollingImporterImpl. atrasos AEM encerramento. NPR-18298; Hotfix para CQ-96133

### Integrações {#integrations}

* Correção de erros de componentes de pesquisa do AEM que podem ocorrer quando o AEM Day HTTP Client 3.1 OSGI é configurado com um Proxy que requer Autenticação Digest. NPR 18128
* Caixa de seleção ausente para reverter herança. NPR-17753; Solicitação de hotfix para CQ-4210139
* Os usuários não podem configurar a prioridade ao direcionar um componente com várias atividades. NPR-18658; Hotfix para CQ-4210727
* Os usuários não conseguem navegar na pasta /etc/segmentation para selecionar uma audiência criada na pasta /etc/segmentation/group1. NPR-18522

### Segurança {#security-1}

* O assistente para Mover ativo trava se o usuário não tiver permissão de gravação na pasta do público alvo. NPR-18300
* Solicitação para usar uma versão atualizada de org.apache.sling.servlets.post servelet (2.3.22) na API Apache Sling para evitar uma vulnerabilidade XSS. NPR-18963

### Tradução {#translation-6}

* A página do ativo não deve ser enviada novamente para um projeto de tradução até que o projeto seja concluído. NPR-18249; Hotfix para CQ-4209908

### WCM-Componentes do Foundation {#wcm-foundation-components-8}

* Não é possível usar o componente iparsys de base WCM em modelos editáveis. NPR-18223; Hotfix para CQ-4210384
* O Mapa de imagem não retém as coordenadas selecionadas no componente de imagem HTL. NPR-18032; Hotfix para CQ-4211584
* Quando um componente de imagem HTL é renderizado, o nome do arquivo no URL é renomeado causando a quebra do URL. NPR-17908; Hotfix para CQ-4211587
* Não é possível sair de Propriedades da página depois de fazer alterações. NPR-17832; Hotfix para CQ-96110

## Forms {#forms-14}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [AEM Forms Releases](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-14}

**Gerenciamento de correspondência**

* O Dicionário de dados é lido repetidamente durante a renderização da carta. NPR-18482, Hotfix para CQ-4210805
* Adição do JavaDocs à classe com.adobe.livecycle.content. NPR-18467
* Ao criar uma carta, a descrição da carta não é salva. NPR-18039
* Quando um módulo de texto é salvo e uma expressão no módulo de texto não contém tags de expressão de abertura ou fechamento, nenhuma mensagem de erro é exibida. O módulo de texto exibe uma mensagem de erro e não é renderizado na carta. NPR-17798
* Erros inesperados vistos em registros na instalação do pacote suplementar. NPR-18295

**Gerenciador do Forms**

* A interface do usuário do AEM Forms lista todos os ativos na ordem mais antiga. Os usuários não podem reordenar os ativos na ordem mais recente. NPR-18451

### Instalador do Forms JEE  {#forms-jee-installer-14}

**Serviço de saída**

* Problema de desempenho aprimorado do serviço de Saída para AEM formulários 6.2. NPR-18033

**Serviço de assinaturas**

* Não é possível assinar um documento PDF com Módulo de segurança de hardware remoto. NPR-18017

## Pacotes OSGi incluídos no CFP6 {#osgi-bundles-included-in-cfp-2}

Lista de pacotes OSGi atualizados no AEM 6.2SP1-CFP6

[Obter arquivo](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP6

[Obter arquivo](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Correção de vários problemas de interface do usuário com ativos de compartilhamento, movimentação, publicação e download.
* Maior capacidade da caixa de diálogo Mover na exibição de ativos referenciados.
* Solução de vários problemas em componentes e workflows do WCM, como Cancelar publicação e Expurgação da versão.
* A capacidade de resposta da barra de ação foi aprimorada em relação à exibição de ações da barra de ferramentas e componentes do Coral.

### Ativos {#assets-14}

* Aprimoramentos de desempenho na funcionalidade de publicação no Brand Portal. NPR-17189; Hotfix para CQ-4204150
* Compartilhar um ativo usando a opção Compartilhar link não cria um arquivo zip com uma estrutura de pasta simples para download. NPR-17513; Hotfix para CQ-4209381
* Selecionar um ativo no DAM e clicar em Publicar não exibe a opção Publicar no Brand Portal na página de detalhes do ativo. NPR-17351; Hotfix para CQ-94905
* Nas etapas do fluxo de trabalho do DAM, os fluxos binários adquiridos de Session ou ResourceResolver devem ser fechados em um bloco final para garantir que os vazamentos de recursos não ocorram. NPR-17385; Hotfix para CQ-4209452
* Carregar um documento do Word no DAM resulta em uma exceção de ponteiro nulo e a instância do fluxo de trabalho permanece presa no estado Em execução. NPR-17160; Hotfix para CQ-4207358
* Os botões Compartilhar, Mover, Publicar e Baixar estão visíveis para ativos expirados na página Editor de metadados para usuários não administradores. NPR-16903; Correção para CQ-101440/CQ-104535
* Ações como Compartilhar, Mover, Publicar e Copiar devem estar visíveis para usuários administrativos no console Ativos. NPR-16902; Hotfix para CQ-4207111

### Sites {#sites-14}

* Ao mover uma página usando a interface clássica e a interface de toque, a caixa de diálogo Mover não mostra referências além de 150, impossibilitando que os usuários atualizem essas referências e republiquem a página. Esse problema foi corrigido com a introdução de uma propriedade para a interface clássica: &#39;maxRefNo&#39; que pode ser configurado no nó siteadmin: &#39;/libs/wcm/core/content/siteadmin&#39;. Essa propriedade especifica o número máximo de referências (valor padrão 150) que são exibidas antes de uma operação de movimentação intensa e se uma página tiver mais referências, elas não serão exibidas na caixa de diálogo movePage. Essa configuração também funciona para damadmin e miscadmin ao aplicar configuração nos nós: `'/libs/wcm/core/content/damadmin'` e `'/libs/wcm/core/content/miscadmin'` respectivamente. NPR-17222; Hotfix para CQ-85878

* Ao trabalhar com componentes WCM, os hiperlinks com espaços são removidos no Editor de Rich Text da interface de toque. NPR-17698, NPR-17570; Hotfix para CQ-4206768
* Ao disparar o fluxo de trabalho Solicitar para não publicação das propriedades da página, erros de JavaScript são exibidos para usuários sem direitos de replicação. NPR-17294; Hotfix para CQ-102064
* A renderização ou exportação de um componente de imagem HTL altera o URL para um número, renomeando o nome do arquivo, o que causa links quebrados. NPR-17245; Hotfix para CQ-59616
* A exclusão de uma inicialização em uma inicialização aninhada faz com que as inicializações secundárias fiquem órfãs. NPR-17228; Hotfix para CQ-4202639
* A execução da Expurgação da versão no AEM 6.2 com Oak 1.4.13 aplicado causa um aviso constantemente repetido nos registros. NPR-17391; Hotfix para CQ-4206870
* Após instalar uma correção ou uma atualização para o componente ContextHub, o pacote de conteúdo substitui todos os segmentos em /etc/segmentation/contexthub, resultando na perda de todos os segmentos personalizados do ContextHub. NPR-17250; Hotfix para CQ-79958
* Ao executar um fluxo de trabalho com grupos aninhados como usuários do fluxo de trabalho, o WorkflowStatusProvider (pageinfo.json) faz com que a instância do fluxo de trabalho seja bloqueada. NPR-17555; Hotfix para CQ-4202056
* Ao usar os componentes do editor de página WCM, existe uma grande quantidade de espaço vazio no final da página no modo de edição da interface de toque da instância do autor. NPR-17510; Hotfix para CQ-4205441
* A renderização ou exportação de um componente de imagem HTL altera o URL para um número, o que causa links quebrados. NPR-17245; Hotfix para CQ-59616

### Interface {#ui}

* Selecionar um ativo e clicar em Ferramentas do desenvolvedor nem sempre exibe as ações da barra de ferramentas na barra de ações em conexões lentas e a página precisa ser recarregada. NPR-17568; Hotfix para CQ-108365
* A barra de ação deve ser atualizada para usar dois container: coral-actionbar-primário e coral-actionbar-secundário, em vez de coral-actionbar-container. NPR-17591; Hotfix para GRANITE-15225

### Dispositivo móvel sob demanda {#mobile-on-demand-2}

* Os usuários com permissões &quot;Somente leitura&quot; para o aplicativo AEM Mobile não podem pré-visualização conteúdo da página de Gestão de conteúdo do AEM Mobile. NPR-17390; Hotfix para CQ-4209690

### Segurança {#security-2}

* A vulnerabilidade XSS na saída gerada por HTMLRendererServlet. NPR-17136
* Solicitação para impedir a divulgação AEM versão na página de feeds de sindicalização AEM Web. NPR-16219

### Forms {#forms-15}

#### Pacote complementar do Forms {#forms-add-on-package-15}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte Versões do AEM Forms.

**Formulários adaptáveis**

* Para um formulário adaptável com anexo, as entradas de duplicado para as tags afSubmissionInfo são criadas no XML enviado quando o formulário é submetido pela segunda vez. NPR-17364
* Ao usar o navegador Google Chrome, após remover um anexo de um formulário, tentar reanexar o mesmo anexo novamente gera um erro. NPR-17297
* Se houver painéis aninhados e repetidamente carregados com preguiça no Forms adaptativo baseado em XSD ou no modelo sem formulário, os valores preenchidos no formulário não serão retidos no Documento de registro (DOR). NPR-17176
* Erros exibidos no log de erros do Editor de regras devem ser adicionados no bloco catch de um código JavaScript do bloco try/catch. NPR-16757
* Clicar em um anexo de arquivo em um formulário emite um erro de console do navegador e não exibe a pré-visualização do anexo. NPR-17174

**Gerenciamento de correspondência**

* A funcionalidade Criar interface de usuário de correspondência é quebrada em caso de texto incorporado ou de adição de uma linha em branco na interface do usuário. NPR-17748
* O navegador pisca quando uma carta é aberta para edição. NPR-17576
* Ao adicionar funções remotas em elementos de dicionário de dados computados, se o número de funções for maior que o comprimento da guia mostrando funções remotas, a barra de rolagem não aparecerá na guia. NPR-17359
* O método da API, importe com.adobe.icc.services.api.LetterInstanceService não funciona. NPR-17922, NPR-16008
* Uma variável adicionada em um módulo de texto não é visível no painel Vínculo de dados ao editar uma carta. NPR-17940
* A interface do usuário do Gerenciamento de correspondência não é aberta quando a ação de envio de HTML usa o método POST. NPR-17595

**Gerenciador do Forms**

* Com um formulário adaptável configurado para teste AB, clicar em Teste AB do Start não start o teste e emite um erro no console do navegador. NPR-17838

**Serviço do Forms**

* Os problemas reportados na análise de código estático dos formulários OSGI devem ser corrigidos. NPR-13951

#### Instalador do Forms JEE {#forms-jee-installer-15}

**Serviço de saída**

* O uso do serviço de saída AEM formulários 6.2 para unir um formulário específico a um XML de dados leva 20 vezes mais tempo do que o tempo gasto pelo servidor LiveCycle ES4 SP1 para a mesma operação. Ele foi corrigido em ambientes Windows e Linux. NPR-17501

**Instalar o LCM**

* Depois de instalar a compilação AEM Forms 6.2 GM e aplicar o CFP AEM 6.2, executar o LiveCycle Configuration Manager exibe um ponto-e-vírgula indesejado nas Informações da versão e a data de instalação do patch não é atualizada. NPR-14322

**Gerenciamento de processos**

* A variável TaskContext não é preenchida em processos do AEM Forms. CQ-4211857

#### Pacote de pacotes JEE AEM Forms {#aem-forms-jee-bundles-package}

* Os recursos dos usuários de formulários, seja usando o console da interface do administrador JEE ou o console OSGi, devem ser os mesmos. NPR-17670

### Pacotes de recursos incluídos no CFP5 {#feature-packs-included-in-cfp}

**Pacote Forms JEE**

Gerenciamento de processos - Espaço de trabalho HTML

* Ao atribuir uma etapa do espaço de trabalho, a guia anexos do espaço de trabalho deve mostrar um contador para os anexos ou notas, caso haja mais de um anexo ou nota. NPR-17771
* Solicitação de suporte ao Office 365 no AEM JEE Forms para recursos de e-mail no fluxo de trabalho do formulário. NPR-13866

**Pacote complementar do Forms**

Gerenciamento de correspondência

* Ao editar fragmentos no editor de texto durante uma pré-visualização de carta, o texto processado deve ser exibido para edição em vez das condições embutidas usadas nos fragmentos. NPR-15748, NPR-17504

### Pacotes OSGi incluídos no CFP5 {#osgi-bundles-included-in-cfp-3}

Lista de pacotes OSGi atualizados entre AEM6.2 SP1-CFP5

[Obter arquivo](assets/do-not-localize/cfp5_osgi_bundles.txt)

Lista de pacotes de conteúdo atualizados entre AEM6.2 SP1-CFP5

[Obter arquivo](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques deste Cumulative Fix Pack são:

* Correções em ativos para representação Camera Raw de arquivos, visualização da linha do tempo e orientação da imagem
* Melhoria na

   * Inicializações do WCM para sites
   * Fluxo de trabalho de projetos
   * Componentes do ContextHub

* Correções para Campanha, Mobile sob demanda e tradução
* Melhorias na usabilidade no Editor de regras para formulários adaptáveis
* Editor de condições em linha aprimorado para o Gerenciamento de correspondência em formulários
* Correções do gerenciamento de processos e do serviço de saída para formulários AEM em JEE
* Correção relacionada ao Forms Designer para o Editor de scripts

### Plataforma {#platform-12}

* O formulário de pesquisa de Search &amp; Promote ignora a configuração `environment` quando o serviço de nuvem é configurado, tornando-o inutilizável na instância do autor. NPR-16594: Hotfix do CQ-4206076
* A adição ou personalização de colunas aos resultados **Assets OmniSearch** ao sobrepor em /apps não funciona. NPR-16737: Hotfix do CQ-4206785
* A **ferramenta de diagnóstico **página não funciona após uma atualização no local do AEM 6.1 SP2 para o AEM 6.2 SP1. NPR-17121; Hotfix para CQ-4196786
* HTL: Ao selecionar um Fórum, criando um Tópico e uma Publicação, a propriedade `Sightly SightlyCompiledScript` adiciona incorreta `addSelectors` a `RequestDispatcherOption`. NPR-17008: Hotfix do GRANITE-16384

* Adicionado suporte para `CRON expressions` em `ManagedPollConfigs` usado pelo `ReportImporter`. NPR-16608: Solicitação de hotfix para CQ-4206066

* Falha ao carregar uma imagem de avatar para um usuário LDAP. NPR-16561; Hotfix para Granite-17013
* O número de resultados exibidos na tela Gerenciamento do usuário é diferente na visualização de cartão e Lista. NPR-16241; Hotfix para GRANITE-16914
* Falha ao carregar as notificações de fluxo de trabalho ao visualizar no navegador Google Chrome no modo Tela cheia. NPR-17013: Hotfix do CQ-4207567

### Ativos {#assets-15}

* A orientação da imagem não é aplicada corretamente ao importar uma imagem com uma orientação definida. NPR-16750: Hotfix do CQ-4204356
* A visualização Linha do tempo do Assets não exibe nenhum ativo, mesmo que &quot;Mostrar tudo&quot; esteja definido por padrão. NPR-16957: Hotfix do CQ-98780
* Os arquivos Camera Raw (incluindo ARW, CR2, NEF, DNG e EPS) quando adicionados como renderização em ativos não podem ser selecionados ou excluídos. Esses arquivos são baixados automaticamente quando o usuário clica neles. NPR-16949: Hotfix do CQ-4206846
* Criar um pdf dentro de outro pdf na interface do usuário do Assets não exibe os pdfs criados na interface do usuário do DAM, embora eles estejam visíveis no repositório do crx. NPR-16833: Hotfix do CQ-4206501
* Fazer upload de um ativo como um nó filho a partir de si mesmo usando a interface do usuário de toque causa um problema. O ativo é carregado como um filho direto do ativo selecionado anteriormente. NPR-16534: Hotfix do CQ-4204287
* Na interface do usuário do DAM, comentar em um ativo e marcar um usuário no comentário não gera uma notificação por email. NPR-16589: Hotfix do CQ-102318

### Projetos {#projects-3}

O console de fluxo de trabalho Projetos mostra NullPointerException na página quando os workflows são expurgados. NPR-17017: Hotfix do CQ-4194269

### Sites {#sites-15}

* Os arquivos em `ContextHub` não são minimizados na instância do autor. NPR-17022: Hotfix do CQ-79456
* A promoção de inicialização do WCM-Launches leva muito tempo para promover uma inicialização que consiste em uma grande árvore de uma página. NPR-16480: Hotfix do CQ-82731
* `ClientContext` O Renderizador de condição de segmento falha quando um segmento (ou audiência) é criado com uma regra inoperante ou inacabada. NPR-16759: Hotfix do CQ-4205104
* Em Inicializações de WCM, as páginas associadas a uma Inicialização não são despublicadas quando a ação é iniciada nas propriedades da página na interface de usuário de toque. NPR-16560: Hotfix do CQ-4204681
* O Link Rewriter regrava falsamente os valores href contendo dois pontos, assumindo que o dois pontos &quot;:&quot;define uma namespace JCR. NPR-16753: Hotfix do CQ-4203762
* No Importador de design do WCM, abrir uma página do importador de teste e tentar carregar um arquivo zip causará problemas se ele tiver sido carregado e excluído anteriormente. NPR-16486: Hotfix do CQ-90962
* Navegar até o painel **[!UICONTROL Navegação global]** usando os navegadores Firefox Safari e Google Chrome fornece uma experiência de usuário diferente. O navegador Firefox exibe o menu **[!UICONTROL Ferramentas]**, enquanto o navegador Google Chrome mostra o menu **[!UICONTROL Navegação]**. NPR-16770; Hotfix para CQ-4200456

### Campanha {#campaign}

* Ao testar templates de campanha AEM e modificar seeds addresses para incluir &quot;Dados adicionais&quot;, o menu suspenso Adobe Campaign desaparece no Touch UI Context Hub. NPR-16771: Hotfix do CQ-105748

### Mobile on-demand {#mobile-on-demand-3}

* Quando a comprovação de uma publicação do ambiente do autor do AEM, uma ação de comprovação que leva mais de 5 segundos causa um pico incomum no painel inicial AEMM - AEM Integração PECS Integração com um alto número de solicitações de status por segundo. NPR-16908: Hotfix do CQ-4207055
* O gerenciamento de configuração do AEM Mobile falha após a instalação da atualização AEM-6.2-SP1-CFP1-1.0. NPR-16909: Hotfix do CQ-4204892

### Tradução {#translation-7}

* A visualização de trabalhos de tradução não funciona após a instalação do 6.2 SP1 - CFP1. NPR-16481; Hotfix para CQ-4204655
* A cópia de idioma criada usando Pontos de tradução para a raiz Principal em vez da live copy do país local. NPR-17257; Hotfix para CQ-4208287

### Segurança {#security-3}

* Nenhuma validação de tipo MIME é executada quando binários de arquivos são carregados para AEM. NPR-16617
* Problemas com o upload de imagens de avatar de usuários do LDAP. NPR-16561

### Forms {#forms-16}

#### Pacote complementar do Forms {#forms-add-on-package-16}

**Formulários adaptáveis**

* No editor adaptável Forms, o comentário Configuração do Público alvo em head.jsp deve ser substituído pela nova instrução Context Hub. NPR-17173
* No Adaptável Forms Rule Editor, o **[!UICONTROL Choose an Item]** mostra o evento como &#39;null&#39;. NPR-17139
* O formulário enviado é reenviado ao navegar para frente usando a seta para frente (>). NPR-17080
* Ao enviar um formulário adaptável via AJAX, a função de retorno de chamada &quot;erro&quot; nunca é chamada em caso de erro. NPR-17034
* Clicar no botão **[!UICONTROL Salvar formulário]** no Editor de regras em tempo de execução não salva o formulário. NPR-16905
* O texto estático deve ser excluído da ordem de tabulação na forma Adaptável. NPR-16749
* O valor calculado de um campo decimal é exibido incorretamente. NPR-16596
* O ícone para exibir o conteúdo da Ajuda deve ser incluído na ordem de tabulação dos formulários adaptáveis. NPR-16484
* Suporte para o uso de expressão regular do tipo `dataRef=C:/Users/`na &#39; **[!UICONTROL Configuração do serviço de preenchimento prévio padrão]**&#39; para Preenchimento prévio de dados para o Adaptive Forms. NPR-16425

* As validações não são acionadas corretamente para todos os painéis se houver um cenário aninhado de carregamento lento. NPR-15821

**Gerenciamento de correspondência**

* A representação da carta falha se uma carta contiver um módulo de texto em branco (um sem texto). NPR-17054
* Quebras de linha e espaços de guia são removidos do conteúdo depois de serem colados no Editor de texto. NPR-17039
* A exibição de referências de um módulo de texto leva muito tempo se o módulo de texto for referenciado em muitas letras. NPR-17035
* A edição, salvamento, exclusão e definição de referência para fragmentos de documento leva muito tempo. NPR-17033
* O texto justificado é renderizado em uma fonte diferente ao visualizar a carta. NPR-16976
* A funcionalidade de pesquisa não funciona corretamente se o texto pesquisado tiver várias ocorrências. NPR-16920
* A barra de ferramentas do Editor de texto é exibida intermitentemente no navegador. NPR-16919
* A construção **[!UICONTROL Salvar formulário]** do Editor de regras não funciona. NPR-16905
* O menu suspenso Fonte não preenche a família Fonte ao criar um módulo de texto com base no dicionário de dados usando o Internet Explorer. NPR-16944
* Depois de criar um fragmento de texto, a fonte da carta muda na visualização da carta. NPR-16830
* As letras com espaços de tabulação no início ou entre expressões no fragmento do documento não podem ser renderizadas ou visualizadas. NPR-16769

**Forms portátil**

* A pré-visualização de formulário móvel mostra o conteúdo sobreposto, embora o formulário seja exibido corretamente para renderização em PDF. NPR-17105

**Portal da Forms**

* Clicar no link **[!UICONTROL Download]** de um formulário enviado abre uma página HTML em vez de um formulário PDF. NPR-17082

* `Upload Comments` para anexos de arquivo não são exibidos na interface para instâncias enviadas, embora estejam presentes no XML armazenado no repositório crx. NPR-17075

**Serviço de extensões Reader**

* Um arquivo específico não é Reader Extended em AEM formulários instalação OSGI. NPR-16625

#### Instalador do Forms JEE  {#forms-jee-installer-16}

**Núcleo**

* Durante o processo de atualização, o Configuration Manager falha com o tempo limite. NPR-16774 (Consulte [Configurar tempo limite para operações no nível do componente](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Gerenciamento de processos - Espaço de trabalho HTML**

* O ponto de partida de uma Tarefa de Start não começa com os dados enviados no momento do envio do ponto de partida. NPR-16917
* Clicar no botão **[!UICONTROL Retornar]** para um formulário no espaço de trabalho HTML não fecha o formulário, mas o retorna à Fila de grupo.\
   NPR-16352

**Gerenciamento de processos**

* Permite que os usuários definam o nome de exibição de tarefas anteriores para qualquer uma das tarefas seguintes em uma instância do processo. NPR-15382

**Serviço de saída**

* O Serviço de Saída não processa um PDF modificado para incluir um campo &#39;milli-sec&#39; adicional nos metadados `date-time format`. NPR-16838

#### Designer do Forms {#forms-designer}

* AEM Editor de scripts do Designer não respeita os padrões das Propriedades do formulário para `Calculate Event`e `Validate Event`. NPR-15921

### Pacotes de recursos incluídos no CFP4 {#feature-packs-included-in-cfp-1}

**Pacote complementar do Forms**

* Aprimoramento no Editor de condições em linha para o Gerenciamento de correspondência. NPR-10981

### Pacotes OSGi incluídos no CFP4 {#osgi-bundles-included-in-cfp-4}

Lista de pacotes OSGi atualizados entre o AEM 6.2 SP1 e CFP4

Os principais destaques da CFP3 são:

* Recurso de pesquisa mais eficiente para a interface clássica e para o componente de pesquisa AEM usando proxy com autenticação de compilação
* Corrige problemas ao carregar ativos e exibir metadados de ativos
* Corrige problemas ao criar pastas e mover páginas, caso o título tenha caracteres especiais.
* Correções para usar audiências de sincronização de definição de metas, campanhas de publicação e seleção de Métrica de meta na interface de usuário de toque
* Resolve problemas de sincronização para trabalhos de tradução
* Oferece segurança aprimorada para o serviço de preenchimento prévio da Forms
* Melhorias no rascunho do portal de formulários e no componente de envios e no serviço Forms com códigos de barras
* Melhorias na usabilidade para formulários adaptáveis que contêm widgets de anexos de arquivos ou fragmentos carregados lentamente.
* Aprimoramentos de usabilidade no Gerenciamento de correspondência, incluindo recursos de pesquisa aprimorados, registro de ativos excluídos e importação de dicionários de dados.

### Plataforma {#platform-13}

* Uma condição de raça em **ModelAdapterFactory**, que é possível quando dois threads tentam injetar o mesmo campo, resulta em falha ao construir o modelo. NPR-16443: Hotfix para SLING-6584
* A opção de validação no gerenciador de pacotes para detectar conflitos entre arquivos sobrepostos (arquivo JSP ou JavaScript) em /apps e o arquivo que continha um Hotfix em /libs. A sobreposição afetada pode ser rebaseada para incluir alterações do arquivo em /libs. NPR-16216: Hotfix do CQ-81729
* O logon no error.log às vezes para alguns segundos após iniciar o editor e precisa ser limpo para ser executado novamente. Solicite a atualização da estrutura de registro e forneça o registro Sling. NPR-15913: Hotfix do Granite-15452
* Solicite a atualização da API &quot; `use"` do JavaScript para evitar falhas na implementação da API de uso do JavaScript HTL. NPR-16461: Hotfix para SLING-6780

### Sites {#sites-16}

* Após a atualização do AEM 6.0 para o AEM 6.2, a interface de usuário clássica mostra desempenho lento enquanto pesquisa tags devido a vários query. Para resolver o problema, as etapas mencionadas em [Desativar status de replicação no console de marcação (interface clássica)](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr) podem ser seguidas. NPR-15842: Hotfix do CQ-4201748.

* Ao criar uma página na interface de usuário para toque, a verificação de entrada para o campo &#39;nome&#39; não verifica o caractere especial &#39;Apostrophe&#39; (o mesmo que na interface de usuário clássica). Portanto, a página não pode ser movida. NPR-16404: Hotfix do CQ-4205321.
* Aplicar estilos diferentes em duas linhas no Editor de Rich Text e depois mesclá-los remove o estilo aplicado na segunda linha. NPR-16389: Hotfix do CQ-4203835.
* Na tela Sites da interface de usuário de toque, tentar colar uma página dentro de uma página sem subpáginas não funciona, pois o botão Colar não aparece. NPR-15894: Hotfix do CQ-4201696.
* Ao rolar a guia Páginas no painel Localizador de conteúdo, alguns conjuntos de páginas são exibidos indefinidamente na interface clássica, enquanto a interface de usuário de toque mostra um conjunto limitado de poucas páginas não repetitivas. NPR-16271: Hotfix do CQ-4202371
* A abertura das Propriedades da página de um LiveCopy na interface do usuário para toque e o clique em Salvar sem qualquer alteração anuncia qualquer guia do LiveCopy e cria um nó de configuração do LiveSync. NPR-16327: Hotfix do CQ-108562
* A restrição de formulário não consegue ler a propriedade `ConstraintMessage`. NPR-16388: Hotfix do CQ-101330
* O componente `wcm/foundation/components/parsys` não exibe o espaço reservado **[!UICONTROL &#39;Arraste componentes aqui]**&#39;. NPR: 16748: Hotfix para CQ-4205187

### Ativos {#assets-16}

* O rasterizador pdf para de funcionar e causa problemas de memória após a instalação do 6.2 SP1 ou do Hotfix 12430. NPR-15991
* Os metadados de uma propriedade de string, `documentNumber` são exibidos como uma data, mas devem ser um número. NPR-16134: Hotfix do GRANITE-16916
* truncamentos de texto no balão de evento da linha do tempo. NPR-16226: Hotfix do CQ-85226
* Ao criar uma pasta na hierarquia de conteúdo com um título com caracteres especiais, o formulário codificado do caractere especial é exibido. NPR-15935: Hotfix do CQ-4202987
* O usuário não pode carregar ativos ou criar pastas enquanto navega por ativos devido a comportamento inconsistente exibido ao usar o botão &#39;Criar&#39;. NPR-16410: Hotfix do CQ-4204793
* Erros inesperados são encontrados durante o upload de recursos HTML compartilhados da visualização de artigos em Criação AEM. NPR-16133: Hotfix para AEMM-4155970

### Integração {#integration-14}

* Ao habilitar a autenticação proxy com autenticação Digest, o componente AEM Search lança uma ConcurrentModificationException. NPR-15309: Hotfix do CQ-4199191
* Ao criar uma Atividade de teste A/B de Público alvo no AEM, a audiência não sincroniza até o Público alvo e mostra &#39;no audiência&#39;. NPR-16229: Hotfix do CQ-4204210
* Depois de instalar o SP1+NPR-11577 v1.2, ao escolher &quot;Usar uma métrica do Analytics&quot; para a métrica de meta enquanto segmenta na interface do usuário do Touch, a lista suspensa de métricas nunca é carregada. NPR-16129: Hotfix do CQ-4204316
* Ao usar a definição de metas, a publicação da campanha não publica automaticamente a árvore inteira, incluindo a marca e o principal. NPR-15855: Hotfix do CQ-94630

### Tradução {#translation-8}

* O trabalho de sincronização de tradução não é acionado automaticamente e AEM pesquisa não ocorre sem executar o ping nos projetos de tradução. NPR-15163: Hotfix do CQ-90856

### Forms {#forms-17}

#### Pacote complementar do Forms {#forms-add-on-package-17}

**Formulários adaptáveis**

* Ao salvar um formulário adaptável com um anexo, o caminho completo do anexo é adicionado à tag `fileAttachment` do XML gerado, em vez do nome do anexo. NPR-16529
* Em formulários adaptáveis baseados em XDP, o invólucro `afData/afBoundData` está presente no XML enviado, embora mesmo o XML de pré-preenchimento não tenha invólucros `afData/afBoundData`. NPR-16118

* Notação exponencial no campo Número: Ao usar formulários adaptáveis, se um número com uma fração decimal que exceda dez caracteres no total for inserido, o número se tornará uma notação exponencial no XML enviado. NPR-16106
* Para formulários que contêm um componente de anexo de arquivo e um fragmento carregado lento, o xml de dados enviado não contém as informações do componente de anexo de arquivo. NPR-16022
* Para um painel repetitivo carregado com preguiça que não tenha um ancestral repetível, os filhos repetíveis dentro de uma segunda instância do painel não serão repetidos. NPR-15944
* Ao tentar salvar um fragmento dentro de um fragmento no editor de formulários, a raiz do modelo de fragmento não preenche o valor do fragmento filho. NPR-15943
* Ao criar uma caixa de seleção com apenas um item e tentar mostrar o título da caixa de seleção mantendo o título do item oculto, a ação de criação de dicionário acionará um `ArrayIndexOutOfBoundException` se o texto do item estiver vazio. O dicionário não é criado e nenhuma resposta de erro é gerada na tela. NPR-15816
* Para formulários adaptáveis com widgets de anexo de arquivo, algumas partes do formulário são desativadas depois que o arquivo anexado é visualizado.\
   NPR: 16611

* Para widgets de anexo de arquivo nos quais vários anexos são permitidos, se uma nova instância de formulário com um anexo for enviada em um widget com um anexo anterior, um código de erro será exibido ao abrir o anexo adicionado em vez do conteúdo real. NPR-16258
* Proteger o serviço de preenchimento prévio de formulários do acesso não autorizado por meio de protocolos como `file://`, `http://` e `ftp://`. Consulte &quot; [Configuração do serviço de Prefill utilizando o Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754).&quot; NPR-15414

* Solicite a renderização do formulário adaptável em formato PDF em vez de HTML na etapa Verificar e anexe todos os anexos ao PDF para que a impressão exiba o formulário completo. NPR-9011

**Gerenciamento de correspondência**

* Ao trabalhar com fragmento de texto em uma letra no modo Pré-visualização/Edição, se o texto for convertido em lista, a funcionalidade da letra inteira será interrompida e um erro de JavaScript será gerado. NPR-16460
* A importação de um arquivo XSD para criar um Dicionário de dados no nó Gerenciamento de correspondência falha, pois o navegador fica sem responder toda vez que o XSD é carregado e o nó raiz é selecionado. Esse problema é independente do navegador e não aparece nos registros do servidor. NPR-16452
* Ao visualizar uma carta usando o navegador Internet Explorer e tentar editar o tamanho da fonte do conteúdo, os valores do duplicado são vistos de 8 a 72 na lista suspensa do tamanho da fonte. NPR-16387
* Caso um campo flutuante apareça como um campo de entrada de um fragmento XDP, o campo não se expande na pré-visualização de letras ao usar o navegador Internet Explorer. NPR-16367
* Ao tentar enviar uma carta diretamente da pré-visualização, o pop-up para o nome da carta não é exibido corretamente devido a estar oculto. NPR-16353
* Os espaços de linha adicionados ao editar uma carta não são refletidos na janela de Pré-visualização. Para listas em fragmentos de texto, a saída PDF não mostra o espaçamento correto. NPR-16267
* Ao trabalhar em um fragmento de documento de texto usando o navegador Internet Explorer, tentar fornecer recuo ao texto falha, pois o cursor não permite recuo de texto. NPR-16128
* A adição ou modificação de um dicionário de dados a um fragmento de documento de texto existente leva muito tempo e o usuário nem sempre é notificado. NPR-16102
* Ao visualizar uma carta com conteúdo rolável usando o navegador Internet Explorer, a barra de rolagem do navegador se sobrepõe à barra de rolagem da carta e todo o conteúdo não pode ser exibido para fragmentos no lado direito. NPR-16068
* Ao criar ou editar fragmentos de documento de texto usando o navegador Google Chrome, o menu suspenso de seleção de cores aparece automaticamente e não pode ser removido. O usuário precisa selecionar lista como tipo de entrada de dados para poder editar o fragmento. NPR-16067
* Ao usar a Letterinstance API, o método `import com.adobe.icc.services.api.LetterInstanceService` não funciona. NPR-16008
* A alteração dos formatos de exibição de data para `locale=en_US; dateFormat=MMM dd,yyyy;` na Configuração do Asset Composer não funciona como esperado e o formato de data é exibido como caracteres inválidos. NPR-16007
* O tipo de Ligação de dados em letras enquanto a recriação é mostrada como &quot;Usuário&quot;, mesmo se definida de forma diferente anteriormente. NPR-16619

**Portal da Forms**

* Os cenários de atualização para componentes de rascunho e envio não funcionam com a implementação de amostra do banco de dados. NPR: 16752

**Serviço Forms com código de barras (BCF)**

* A análise de código estático do BCF (Barcoded Forms Service, serviço de com código de barras) relata problemas. NPR-13855

#### Instalador do Forms JEE  {#forms-jee-installer-17}

**Gerenciamento de processos - Espaço de trabalho HTML**

* Proteger o serviço de preenchimento prévio de formulários do acesso não autorizado por meio de protocolos como &quot;file://&quot;, &quot;http://&quot; e ftp://. Para obter detalhes, consulte [Configuração do serviço de preenchimento prévio usando o Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15434

**Gerenciamento de usuários **

* A tela de logon SAML mostra a versão incorreta (6.1.0) no servidor AEM 6.2. NPR-13825
* Com a AEM Forms configurada para autenticação de Logon Único (Kerberos), se a autenticação do usuário falhar ao tentar fazer logon, um código de erro &quot;404&quot; será retornado. O usuário é redirecionado para o site de logon somente depois de atualizar a página. NPR-15015

#### Designer do Forms {#forms-designer-1}

* A alteração da localidade do formulário para francês (Canadá) na verificação ortográfica do dicionário não funciona no AEM Forms Designer.\
   NPR-15896

### Pacotes de recursos incluídos no CFP3 {#feature-packs-included-in-cfp-2}

**Pacote complementar do Forms**

* Ao excluir qualquer ativo no gerenciamento de correspondência, uma mensagem de aviso deve ser registrada no arquivo error.log. NPR-13225
* Aprimore a funcionalidade de pesquisa ao visualizar uma carta no gerenciamento de correspondência, para permitir a pesquisa de texto no conteúdo do fragmento de texto, em vez de pesquisar somente o título da carta ou o rótulo. NPR-16103

### Pacotes OSGi incluídos no CFP3 {#osgi-bundles-included-in-cfp-5}

Lista de pacotes OSGi atualizados entre o AEM 6.2 SP1 e CFP3

[Obter ](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
arquivoOs principais destaques do Cumulative Fix Pack 2 são:

* Correções de estabilidade e melhorias de desempenho em AEM plataforma, incluindo a estrutura Sling e as operações
* Gerenciamento de ativos aprimorado com várias correções para acesso, movimentação, pesquisa, upload e publicação de ativos
* Criação e gerenciamento de sites aprimorados com correções em fragmentos de conteúdo, plug-in de âncora, apresentação de slides e componentes do Context Hub
* Várias correções na interface do usuário de toque, incluindo o editor de texto, o Omnisearch e o processo de criação de variantes
* Melhorias nos workflows de tradução; conector Microsoft aprimorado para usar novas APIs de tradução para o portal do Azure
* Correções em projetos e Campanha
* Criação e gerenciamento aprimorados com correções em formulários adaptáveis, gerenciamento de correspondência e recursos do portal de formulários
* Correções nos componentes do núcleo Forms JEE, XTG e espaço de trabalho HTML

### Plataforma {#platform-14}

* O `SlingPostProcessor` é acionado se a página que faz referência direta à estrutura Sling for editada. NPR-15754: Hotfix do CQ-104153

* O valor das tags com a propriedade `tagBasePath` não é obtido na caixa de diálogo clássica da interface do usuário ao navegar até um componente de página. NPR-15543: Hotfix do CQ-4199950

* Durante a execução de operações Sling, quando você tem um pedaço chamado &#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk` é executado em um loop sem fim com partes vazias. NPR-15455: Hotfix para SLING-5701

* Quando uma interface estende outra interface, os métodos injetáveis na superinterface não são inseridos corretamente. NPR-15202: Hotfix para SLING - 5710
* Uma possível exceção de ponteiro nulo não é impedida ao usar a chamada de função `com.adobe.granite.infocollector.impl.FilesTraversal`. Hotfix NPR-15169 para CQ-4197640
* O estado do fluxo de trabalho é inconsistente para alguns nós secundários e o erro é exibido ao despachar eventos de observação para esse nó. NPR-15701: Hotfix do GRANITE-13786
* Quando o usuário seleciona um nó no CRXDE (por exemplo, /content/dam/) e a guia &#39;Controle de acesso&#39;, certificando-se de que existe uma Lista de Controle de acesso, arrastar e soltar alguns elementos move os elementos diferentes daquele selecionado. Hotfix NPR-15696 para GRANITE-16300
* Selecionar um usuário na lista suspensa ao tentar representar faz com que o pop-up inteiro do usuário desapareça. NPR-15774: HotFix para CQ-4201738/GRANITE-11895
* No Omnisearch, a pesquisa por tags com sugestões preenchidas automaticamente não funciona. NPR-15088: Hotfix do GRANITE-14426.\
   Observação: Essa correção exige o Oak CFP 1.4.11 ou superior.

### Autor do Mobile AEM {#mobile-aem-author}

* Ao usar pacotes AEM Mobile e ContentSync com um aplicativo híbrido, AEM responde a uma solicitação de busca (com carimbos de data e hora) feita pelo aplicativo com o pacote mais antigo, em vez do solicitado pelo aplicativo. NPR-15749: Hotfix do CQ-104153

### Sites {#sites-17}

* O status de modificação da Caixa de entrada do fluxo de trabalho no núcleo do WCM não é alterado se o usuário modificar uma página depois de ativar um fluxo de trabalho. NPR-15684: Hot fix para CQ-4196974
* O plug-in Âncora no Editor de Rich Text para interface de toque gera HTML5 não compatível quando o usuário clica no ícone de âncora e adiciona um nome. Ele deve adicionar um atributo &#39;id&#39; em vez do atributo &#39;name&#39; na tag HTML5 do elemento âncora. NPR-15650: Hotfix do CQ-89782
* Quando um schema de metadados com vários campos é criado e aplicado aos metadados do fragmento do conteúdo, nenhuma barra de rolagem é criada na tela de metadados do fragmento do conteúdo, tornando os campos ineditáveis. NPR-15478: Hotfix do CQ-4202622
* A edição do componente de campo `TagInput` não mostra os valores configurados anteriormente em relação aos campos de diálogo. NPR-15464: HotFix para CQ-4200360

* Na interface do editor de fragmento de conteúdo, caso muitas variações de um fragmento de conteúdo sejam criadas, o painel lateral não mostra a barra de rolagem para navegar por todas as variações. NPR-15445: HotFix para CQ-4199444
* Quando os usuários são removidos de grupos diretos, eles são adicionados a grupos herdados. NPR-15400: Hotfix do CQ-98758
* Criação de WCM: O autor da interface de toque não permite a edição de páginas que têm vírgulas no nome. NPR-15396: Hotfix do CQ-4199723
* Ao usar a interface de usuário de toque para criação, a função `Granite.author.editableHelper.doSelectParent` passa argumentos na ordem errada, gerando um erro de JavaScript. NPR-15349: Hotfix do CQ-4198594
* O segmento ContextHub exibe a experiência mesmo se o cookie de opção de não participação estiver presente. NPR-15293: Hotfix do CQ-4198024
* O componente de Apresentação de slides na interface clássica não pode criar slides ou arrastar e soltar imagens para criar novos slides. NPR-15281: Hotfix do CQ-4194164
* Os usuários, independentemente da permissão, recebem as opções de &quot;Criar&quot;, como Criar página, Criar site, Criar Live Copy, Criar lançamento e Criar catálogo no console de administração do site. NPR-15278: Hotfix do CQ-94436
* Depois de instalar o AEM 6.2 Service Pack 1, o controle deslizante &quot;Incluir subpáginas&quot; para de funcionar para inicializações de página. NPR-15230: Hotfix do CQ-4198449
* Solicitação para aprimorar a Expurgação da versão para buscar e processar versões em blocos e também para usar um caminho especificado em um query XPath. NPR-15186: Hotfix do CQ-109205
* O botão Limpar está ausente na guia de miniatura Propriedades da página no componente Sites. Hotfix NPR-15143 para CQ-4196997
* Para um site que usa Live Copies, marcar a caixa de seleção &quot;Live Copy&quot; no painel Colunas no console siteadmin não exibe o status da Live Copy corretamente e somente a marcação HTML é exibida. NPR-15108: Hotfix do CQ-97086
* Ao editar os Fragmentos de conteúdo, se o usuário clicar em Concluído (&#39; reño) para editar antes de obter a resposta da publicação, o conteúdo editado não será salvo corretamente. NPR-15014: Hotfix do CQ-4194095
* Fechar a página Editar durante o modo Timewarp e tentar reabri-la do Siteadmin resulta em um erro com o status &#39;500&#39; em vez de reabrir a página. NPR-14965: Hotfix do CQ-109647:
* Na interface do usuário do Digital Asset Manager (DAM), a pesquisa Seletor de usuários para localizar autorizações gera uma exceção de &quot;Memória insuficiente&quot;. NPR: 15307: HotFix para CQ-98542

### Ativos {#assets-17}

* Depois de pesquisar um ativo no Omnisearch, selecionar um ativo e tentar editar propriedades clicando em &#39;Propriedades da Visualização&#39; e, em seguida, o botão &#39;Salvar&#39; redireciona os usuários para uma página em branco. NPR-15900: Hotfix do CQ-4202372
* A interface do usuário do Assets não responde aos eventos. Selecionar um ativo e clicar em &quot;Publicar&quot; ou &quot;Representações&quot; não resulta em nenhuma atividade. NPR-15828: Hotfix do CQ-4202247
* Ao publicar um ativo da visualização de cartão, o cartão não é atualizado para refletir um estado publicado, a menos que a página seja atualizada. NPR-15826: HotFix para CQ-102732
* Hotfix cumulativo contendo Hotfixes de ativos. NPR-15225
* Se o caractere E comercial (&#39;&amp;&#39;) estiver incluído no nome de uma pasta de ativos, o nome da pasta não será exibido corretamente ao navegar para o ativo. NPR-15775: Hotfix do CQ-4201735
* O uso do caractere E comercial (&#39;&amp;&#39;) no nome de um arquivo de ativo causa problemas ao acessar suas propriedades. NPR-15770: Hotfix do CQ-4201737
* Ao navegar pelos Ativos e usar o modo de exibição &#39;visualização de coluna&#39;, se o usuário atualizar a página após selecionar e clicar em um ativo, os detalhes do ativo serão exibidos em vez do conteúdo atualizado. NPR-15768: Hotfix do CQ-4201727
* A ingestão de PDS consome até 100% da utilização da CPU com um monte de bibliotecas para serviços pdf. HotFix NPR-15606 para GRANITE-12929
* O acesso à interface do usuário &#39;Meus compartilhamentos de link&#39; usando o navegador Firefox não exibe os itens compartilhados nem os usuários e a tela não pode ser usada. NPR-15539: HotFix para CQ-4200992
* Ao usar o Gerenciador de ativos digitais, se uma página estiver associada a um conjunto de imagens, mover as imagens para uma nova pasta interrompe a associação de páginas e a página associada perde algumas das imagens. NPR-15538: Hotfix do CQ-111479
* No componente Dam Viewer, o uso do modo de execução &#39;nosamplecontent&#39; causa erros na mídia dinâmica. NPR-15449: Hotfix do CQ-4195425
* Ao criar perfis de vídeo, se uma predefinição de codificação de vídeo de alta qualidade e média qualidade for escolhida, as alterações feitas não serão salvas. NPR-15447: Hotfix do CQ-4195482
* Embora o upload de um ativo para o Brand Portal falhe devido à resposta a erros do servidor, o status é atualizado para &quot;Publicado&quot; na interface do portal da marca, dificultando o rastreamento do arquivo perdido. NPR-15442: Hotfix do CQ-4197968
* Ao publicar uma pasta de ativos no Brand Portal, onde a publicação leva mais de uma hora, alguns arquivos não conseguem publicar. NPR-15441: Hotfix do CQ-4199493
* Ao usar o console do Localizador de ativos na visualização de colunas, a tentativa de criar uma pasta falha depois que ela é bem-sucedida ao tentar novamente. NPR-15370: Hotfix do CQ-4199448
* Se um ativo ou pasta selecionado na interface do usuário do DAM tiver uma vírgula no nome, a guia Referências não estará disponível e exibirá a mensagem &quot;A Lista de referências não está disponível para várias seleções&quot;. NPR-15362: Hotfix do CQ-4199721
* A publicação de uma pasta no Brand Portal não altera o estado publicado da pasta, mesmo que os ativos da pasta sejam publicados com êxito. NPR-15292: Hotfix do CQ-4197667
* Ao navegar para o console Ativos na interface do usuário de toque, uma exceção é exibida ao ativar determinados ativos. NPR-15217: HotFix para CQ-108779
* Publicar um vídeo no Youtube quando a conexão for feita por meio de um servidor proxy. NPR-15109: HotFix para CQ-110332
* Uso de um ativo com um nome contendo um ponto ou ponto (.) em dados-sly-resource não é resolvido para o mesmo ativo e o caminho de saída é terminado no ponto. NPR-15069: Hotfix do CQ-4195914
* Após atualizar o AEM 6.2 para o Service Pack 1, a sincronização dos ativos no Scene7 falha. A propriedade dam:Scene7FileStatus exibe o status &#39; `UploadFailed`&#39; mesmo para ativos publicados. NPR-15269: Hotfix do CQ-4197708

### Interface do usuário {#user-interface-5}

* Em **[!UICONTROL Touch UI]**, a data salva não é exibida para campos de data que não têm type=&#39;datetime&#39; ao usar o navegador Internet Chrome versão 56.0.2924.87. NPR-15383: Hotfix para GRANITE-16481
* Em **[!UICONTROL Interface do usuário de toque]**, o Editor de Rich Text remove o thread e os elementos de legenda das tabelas HTML ao renderizá-los. NPR-15267: Hotfix do CRTE-41
* `FileUpload Validator` não trata de casos em que a inicialização automática é verdadeira ou quando  `uploadFile()` é chamada manualmente e gera um relatório de validação inválido nesses casos. NPR-15295: Hotfix do GRANITE-13499

* O Omnisearch não permite que os clientes que usam /apps adicionem uma fonte de dados de coluna, pois presume que a configuração de localização está listada em */libs/granite/omnisearch/content/metadata/*. Hotfix NPR-13188 para GRANITE-16479
* Ao usar a **[!UICONTROL interface de usuário de toque]**, as variantes de produto não são criadas no mesmo nível do produto. O usuário não é informado sobre o status do processo de criação da variante. NPR-15345: HotFix para CQ-4198948

**Scene7**

* A execução do fluxo de trabalho do Scene7 resulta em arquivos abertos que não são fechados. Solicite a melhoria do serviço AEM-S7 para que ele mantenha e reutilize uma única instância HttpClient com configuração de pool compartilhado. NPR-15357: HotFix para CQ-109958

### Tradução {#translation-9}

* Ao usar projetos de tradução, atualizar cópias de idioma do principal inglês produz 11 inicializações separadas com o mesmo nome e raiz de origem, mas com raízes de inicialização ligeiramente diferentes, caso o nome da página siga um padrão definido. NPR-15605: Hotfix do CQ-4200699
* Os projetos de tradução não são criados para páginas quando as raízes de idioma têm hífens e traços no nome. NPR-15171: HotFix para CQ-96286
* Solicite a atualização do conector Microsoft para poder usar as APIs do Microsoft Translator, que a Microsoft disponibiliza no portal do Azure. NPR-15320: Hotfix do CQ-101010

### Projetos {#projects-4}

* Somente 20 projetos inativos estão visíveis na tela Projetos, embora existam mais de 20 projetos inativos no repositório. NPR-15656: Hotfix do CQ-4200903

### Campanha {#campaign-1}

* Ao usar os componentes Campanha - Direcionamento e MAC - Integração de Público alvo e teste, a despublicação do atividade não atualiza o status da atividade na interface Principal. NPR-15401: HotFix para CQ-4199839
* Ao mover um produto em AEM Commerce, o Assistente para movimentação de produtos perde os valores pré-preenchidos para o nome do produto, título, páginas referenciadas, criar autor e data de criação. NPR-15228: Hotfix do CQ-98617

### Segurança {#security-4}

* Parâmetro de token CSRF adicionado a formulários com um método de GET. NPR-15229

### Forms {#forms-18}

#### Pacote complementar do Forms {#forms-add-on-package-18}

`**Adaptive Forms**`

* Os valores padrão são substituídos por valores vazios no xml no preenchimento prévio do formulário Adaptive com XML de entrada. NPR-15721
* O invólucro `afData/afBoundData` está presente no XML enviado, embora mesmo o XML de pré-preenchimento não tenha o invólucro `afData/afBoundData` em formulários adaptáveis baseados em schemas XML. NPR-15541

* Os títulos na barra Acordeão devem ser títulos HTML &#39;h2&#39; editáveis em vez da tag &#39;a&#39;. NPR-15475
* O layout acordeão de um painel de formulário não está acessível aos usuários de leitores de tela. Os usuários não podem navegar até a guia acordeão usando apenas o teclado usando um software de leitor de tela, como JAWS ou NVDA. NPR-15474

`**Correspondence Management**`

* Salvar, excluir e definir a referência de um fragmento de documento leva muito tempo. NPR-15939
* Alinhamento de guias definido em Gerenciar ativos em texto que contém várias quebras de cabeçalhos na interface do usuário do CCR. NPR-15818
* As miniaturas dos módulos de Texto não mostram conteúdo alinhado, embora o texto contenha conteúdo alinhado criado usando guias no Google Chrome. NPR-15819

`**Forms Portal**`

* O serviço de preenchimento prévio não funciona para XDP Forms. NPR-15466
* Ao armazenar rascunhos e envios de formulários adaptáveis para o banco de dados, o estado do formulário adaptável é corrompido quando a conectividade do banco de dados falha por qualquer motivo (por exemplo, após um longo tempo de inatividade). NPR-15297

#### Instalador do Forms JEE  {#forms-jee-installer-18}

`**Core**`

* Após atualizar para a versão mais recente do Java 1.8.0_121-b13, a interface do usuário do Admin não está acessível no AEM Forms. NPR-15330

`**XTG**`

* Ao usar o serviço de Saída para unir um formulário específico a um dataxml, o tempo de resposta é 20 vezes maior do que o tempo gasto pelo servidor ES4 SP1 para a mesma operação. NPR-15283

#### Aplicativo AEM Forms {#aem-forms-app-1}

* Ao recuperar tarefas não salvas, a mensagem mostrada na recuperação de tarefas não salvas precisa ser mais clara para reduzir o erro do usuário. NPR-15377
* O aplicativo AEM Forms não renderiza formulários criados a partir de modelos personalizados. NPR-15892
* Os usuários não conseguem fazer logon no aplicativo AEM Forms. NPR-15891

Os principais destaques do AEM 6.2 SP2-CFP1 são:

* Simplifica a funcionalidade de replicação nos Sites:

   * Correções para vários problemas de implantação, LiveCopy e gravação com falha

* Aumenta a capacidade de resposta da interface do usuário de toque durante:

   * Pesquisas de ativos
   * classificação baseada em tamanho

* Melhora o gerenciamento de tags em coleções inteligentes
* Controles de acesso mais leves durante operações CRUD em pastas

### Plataforma {#previous}

* Solicitação para remoção de chamadas de API `ReplicationQueue#forceRetry` durante a inicialização de agentes de replicação, pois essas chamadas retardam significativamente a instância, especialmente quando ela tem muitos agentes de replicação. NPR-14032: Hotfix do GRANITE-13095
* Solicitação de `DurboImportConfigurationProviderService` configuração OSGi para suportar campos que podem armazenar uma matriz de valores. NPR-14570: Hotfix do CQ-108684
* Usar o componente Sightly em uma página após migrar para o AEM 6.2 faz com que a caixa de diálogo Propriedades da página pare de funcionar. NPR-14328: Hotfix do CQ-108355
* A desprogramação de um trabalho agendado anteriormente não remove o nó correspondente abaixo de */var/eventing/Schedul-jobs*. NPR-14253: Hotfix para SLING-5666
* Quando um administrador tenta representar como um usuário excluído, a interface do usuário falha ao atualizar. NPR-14247: Hotfix do CQ-107446
* Verificação de proteção XSS que causa codificação incorreta no componente Sightly. NPR-14004: Hotfix do CQ-93821
* Solicitação para atualizar o Jackrabbit Filevault para a versão 3.1.30 para resolver vários problemas. NPR-13454
* O erro de cache ocorre quando a distribuição Sling sincroniza os pacotes de distribuição do autor para a publicação. NPR-13034: Hotfix do GRANITE-13970

### Sites {#sites-18}

* Problemas com o VersionManagerImpl ao remover versões incorretas do histórico de versões. NPR-14372
* O componente parsys do WCM Sightly Foundation ignora os nomes das tags de declaração do componente, `cq:htmlTag / cq:tagName`. NPR-14225
* Quando o Sightly Parsys é usado para renderizar componentes inseridos via JavaScript na interface do usuário para toque, a decoração personalizada é ignorada depois que a página é atualizada. NPR-14122
* As listas suspensas do público alvo não funcionam na caixa de diálogo Touch UI quando vários campos Richtext, como links, são criados. NPR-13911
* Ao editar um campo de texto com várias propriedades do Editor de Rich Text (RTE) em uma caixa de diálogo (Interface do usuário de toque), o foco é alternado aleatoriamente para uma propriedade específica do RTE. NPR-13703
* O componente de vídeo padrão fora da caixa não renderiza a miniatura do vídeo. NPR-14976
* Informações carregadas lentamente na guia Usos em tempo real no Editor de modelos. NPR-14880: Hotfix do CQ-83417
* A instalação do Hotfix-10936 em uma instância AEM 6.2 desativa o componente iparsys. NPR-14330: Hotfix do CQ-106982
* Problemas com vários componentes de Rollout e um problema de Live Copy após a migração para AEM 6.1 SP1. NPR-15256
* A ação de Roll-out de página não cria filhos além do primeiro nível, mesmo para várias configurações de Roll-out. NPR-15055
* Ao enviar a caixa de diálogo Propriedades da página do Editor, os dados inalterados nas guias LiveCopy são regravados. NPR-14693
* Quando a caixa de diálogo Propriedades da página é enviada do Editor, o MSM Post Processor grava alguns parâmetros da solicitação em vez do parâmetro `msm:writeLiveCopyConfig`. NPR-14434
* Vários problemas relacionados ao componente de implantação, Live Copies e outros aspectos do MSM. NPR-12235

### Ativos {#assets-18}

* O Fluxo de Trabalho do UnPack não consegue processar imagens com caracteres especiais no nome do ficheiro de imagem. NPR-15227: Hotfix do CQ-103887
* Os ativos que têm a expressão Repetir com Condição não são exibidos corretamente. Quando o usuário pré-visualização o modelo de letra `*CDN3835RLCEN*`, nenhum ativo localizado na área público alvo do corpo é exibido. Quando o ativo `*VIPReassement*`, que é um ativo opcional, que é pré-selecionado não está selecionado, os outros ativos pré-selecionados são exibidos na carta. NPR-14844

* Ao criar uma coleção inteligente, a marca de estilo não é preservada quando a coleção inteligente é salva. NPR-15081: Hotfix do CQ-4195494
* Query de pesquisa de ativos que são executados lentamente na interface de usuário de toque durante pesquisas simultâneas por vários usuários. NPR-15019: Hotifx para CQ-4195405
* Os metadados extraídos para uma propriedade do tipo `Long[]` convertem para o tipo `String[]` quando o ativo original é carregado novamente para um local diferente. NPR-15016: Correção do CQ-4195005

* Os usuários não conseguem excluir uma pesquisa salva ou uma coleção inteligente. NPR-14924: Hotfix do CQ-108494
* Editar metadados para ativos em massa (modo anexar) ao usar um valor booliano para TypeHint em um campo suspenso no schema de metadados subjacente produz um erro. NPR-14529: Hotfix do CQ-106876
* Usuários sem direitos de replicação não podem excluir pastas de ativos. NPR-14321: Hotfix do CQ-88271
* Ao tentar editar os perfis de vídeo de um vídeo no Editor de Canais, a caixa de diálogo de design não abre e gera uma Exceção de ponteiro nulo no registro de erros. NPR-14144: Hotfix do CQ-81101
* A propriedade de carimbo de data e hora &quot;Criado&quot; gerada pelo sistema exibida na página de propriedades de um ativo está incorreta. NPR-13992: Hotfix do CQ-95029
* Solicitação para ativar a detecção de ativos de duplicado para usuários sem acesso de Leitura no AEM Assets NPR-13851: Hotfix para CQ-102281
* Os usuários não conseguem editar metadados para ativos em massa na página de propriedades. NPR-13721: Hotfix do CQ-100703
* Mensagem de erro incorreta na interface clássica quando um ativo de duplicado é carregado. A mensagem de erro não indica por que o upload falhou. NPR-13691: Hotfix do CQ-99272
* A AEM Assets não consegue classificar mais de 50 ativos por tamanho de cada vez na visualização da Lista quando a pasta contém vários ativos. CQ-100588
* A seleção de vários ativos gera um erro com o Código de resposta - 414 (URI de solicitação muito longa) se o URI do ativo/pasta for muito longo. NPR-13516: Hotfix do CQ-76076
* A página Relatório de ativos não responde quando o usuário seleciona todas as opções na caixa de diálogo Configurar colunas. NPR-13187: Hotfix do CQ-95589
* Comportamento inesperado do Seletor de tags no Safari e no Internet Explorer. NPR-13134
* A edição da pesquisa salva no painel de Pesquisa do administrador de ativos permite salvá-los como seleções inteligentes aninhadas, o que causa problemas de estabilidade do ambiente. NPR-13119: Hotfix do CQ-99460
* Depois de mover um arquivo (ou pasta) e, em seguida, renomeá-lo, os metadados &#39;cq:name&#39; não refletem o novo nome de arquivo (nome da pasta). NPR-13036: Hotfix do CQ-99141
* O ativo com nomes que incluem caracteres especiais não pode ser baixado do link de download compartilhado por email. NPR-12872: Hotfix do CQ-95795
* Os relatórios de ativos prontos para uso gerados quando há um número substancial de ativos causam muitos percursos nos quais a pesquisa não atinge nenhum índice e picos de uso da CPU. NPR-12811: Hotfix do CQ-84409
* Os usuários na instância do autor do AMS AEM Assets acessam redes diferentes que não conseguem carregar ativos usando o carregamento de partes sem privilégios de exclusão em pastas. NPR-12768: Hotfix do CQ-82715
* Em pesquisas baseadas em tags para ativos usando o painel Pesquisa de ativos, o recurso Tipo à frente não se limita ao caminho raiz e exibe tags de todas as namespaces. NPR-12666
* O componente StaticRenditions gera uma exceção de ponteiro nulo. NPR-12665
* Solicitação para desativar MissingMetadataNotificationJob, pois isso faz com que a interface de usuário de notificação de emblema quebre a página com uma exceção de tempo de execução &quot;Não é possível verificar a entrada&quot;. NPR-12500: Hotfix do CQ-93573
* A opção &quot;Desativar edição&quot; para um campo de tag não funciona em páginas de propriedades de ativos na TouchUI. NPR-12429: Hotfix do CQ-88835
* Correções de API na implementação do AEM Assets 6.2 para SMB do aplicativo associado. NPR-11099
* Desde a atualização do Jquery, os usuários não conseguem selecionar uma coleção de ativos e confirmar a seleção no painel Associar conteúdo de um fragmento de conteúdo. NPR-14847: Backport para CQ-4194209
* Apesar de chamar a classificação infinita no lado do cliente, somente os artigos/banners/coleções exibidos atualmente na interface do usuário são classificados. NPR-14493: Hotfix do CQ-109926
* Solicitação para implementar o recurso omnisearch para AEM serviço móvel sob demanda. A pesquisa por palavra-chave para qualquer artigo, coleção ou banner não retorna correspondências. NPR-14093: Hotfix do CQ-101394
* Ao usar o componente de seleção de Coral (*granite/ui/components/coral/foundation/form/select*) em uma caixa de diálogo, a inicialização do valor não funciona corretamente no Internet Explorer (navegadores IE11 ou Edge) quando o valor selecionado contém um único item. NPR-13395: Hotfix do CQ-101013

### Projetos {#projects-5}

* Ao exportar um projeto de tradução criado com o Método de Tradução como &#39;humano&#39; e Provedor de Tradução como &#39;nenhum&#39;, nenhum arquivo Translation_export_summary.xml é gerado porque o arquivo de mapeamento GUID está ausente. NPR-13137: Hotfix do CQ-91976
* Nos projetos AEM, ao criar um projeto com a propriedade de data de vencimento definida, a conversão de data define o tempo incorretamente devido à diferença no fuso horário entre o servidor e o cliente. NPR-13003: Hotfix do CQ-98288
* A opção &quot;Revelar em sites&quot; é omitida do trabalho de tradução quando um projeto de tradução é atualizado. NPR-12966: Hotfix do CQ-93740
* Quando um projeto de tradução é criado para uma página do site exportada, ele não é renderizado corretamente na pré-visualização. NPR-12964: Hotfix do CQ-84627

### Fluxo de trabalho {#workflow-3}

* O link de carga na guia Arquivo do console Fluxo de trabalho retorna um erro com o código de resposta &#39;404&#39; ao clicar nele. NPR-14993: Hotfix do CQ-4194977
* Ao usar AEM workflows padrão, o CQ Mailer não envia uma notificação por email para o grupo que perde o endereço de email de um único membro. NPR-14804: Solicitação de hotfix para CQ-91499
* Aprimoramentos de desempenho para a caixa de entrada e o selo de notificação na interface do usuário de toque. NPR-14145: Hotfix do CQ-101125
* Os usuários não conseguem pré-visualização a carga do console Caixa de entrada do fluxo de trabalho ao iniciarem workflows. NPR-13226: Hotfix do CQ-100275
* O cookie &#39;saml_request_path&#39; configurado usando o SAML Authentication Handler exibe um cookie definido com um &#39;?&#39; extra caractere. Além disso, quando uma resposta SAML é postada de volta para AEM, o cookie AEM &#39;saml_request_path&#39; retorna um valor inválido devido a caracteres já codificados. NPR-13517: Hotfix pró-ativo para GRANITE-11722 e GRANITE-14414

### Integração da solução {#solution-integration}

* Após a integração do AEM 6.2 com o Search &amp; Promote, se um usuário pesquisar um termo que retorna um banner, a funcionalidade de pesquisa não responde. NPR-14549: CFP do CQ-109631

### Dynamic Media {#dynamic-media}

* Vários trabalhos de sling AEM-Scene7 que foram criados e cancelados durante AEM ativação são registrados como trabalhos de arquivamento durante a replicação. NPR-12835: Hotfix do CQ-86115

### Segurança {#security-5}

* Solicitação para resolver o problema de validação de entrada no filtro WCMDebug. NPR-12444: Solicitação de hotfix para CQ-94890
* Solicitação pró-ativa para corrigir o comportamento XSS ao usar o Assistente para Criar Inicialização.\
   NPR-13062: Solicitação de hotfix para CQ-99577

#### Pacote complementar do Forms {#forms-add-on-package-19}

`Adaptive Forms`

* Ao criar um painel repetível usando formulários adaptáveis, o título do painel não pode ser atualizado em tempo de execução. NPR-15325
* Quando o valor padrão de um botão de opção é definido e um valor diferente do padrão é selecionado ao salvar ou enviar, o valor não é exibido no preenchimento prévio. NPR-15304
* O Google Chrome mostra um comportamento incorreto ao usar o evento de opções para preencher dinamicamente a lista suspensa e enviar o valor do item selecionado. NPR-15198
* Ao criar um painel repetível usando formulários adaptáveis, o título do painel não pode ser atualizado em tempo de execução. NPR-15181
* Ao usar o modo de edição para formulários adaptáveis, erros de JavaScript como - &quot;O manipulador do componente é inválido&quot; e &quot;o guidelib não está definido&quot; são encontrados. NPR-15112
* Fragmento de carregamento lento dentro de um painel repetitivo não funciona como esperado. NPR-13916, NPR-14785

`Correspondence Management`

* Os ativos do Gerenciamento de correspondência com `'Repeat with condition'`conjunto de expressões não são exibidos corretamente. NPR-14844
* Ao pesquisar por um ativo do Gerenciamento de correspondência (como uma letra, um fragmento de documento ou qualquer outro tipo), o ícone Fila para download não aparece na barra de ferramentas. NPR-14745
* Ao criar um módulo de Lista, a alternância das propriedades específicas do ativo (como editável, obrigatório) não funciona. NPR-14689
* O painel Elementos de dados no utilitário Construtor de Expressões continua sendo carregado caso um módulo de condição seja criado sem selecionar um dicionário de dados. NPR-14688
* Ao visualizar uma carta, os usuários não podem usar espaços de tabulação para alinhar o conteúdo no formato tabular. NPR-14481
* Ao exportar ativos do Gerenciamento de correspondência em massa da interface do usuário, o servidor AEM Forms gera registros desnecessários. NPR-15226
* Quando uma carta é visualizada, o texto justificado é exibido em uma fonte diferente. NPR-15468

`**Forms Portal**`

* Anexos de formulários enviados no portal da Forms não ficam visíveis quando um novo rascunho do envio do portal é enviado. NPR-13515

`**Forms Manager**`

* Ao navegar no diretório *FormandDocuments*, o botão Colar não é exibido quando o usuário copia qualquer ativo e, em seguida, navega para uma pasta diferente. CQ-111327

#### Instalador do Forms JEE {#forms-jee-installer-19}

`Rights Management`

* O evento de auditoria relacionado ao logon do usuário é registrado com um tempo inválido. A hora correta para o evento de auditoria não é rastreável. NPR-13107
* O Adobe Acrobat Reader e o Microsoft Office não conseguem abrir documentos protegidos com autenticação estendida. NPR-14482

`Process Management`

* Quando uma tarefa de rascunho encaminhada no espaço de trabalho HTML é retornada ao usuário inicial, a tarefa não aparece na fila do usuário inicial. NPR-15178

`Assembler Service`

* A AEM Forms não pôde validar um PDF/A-2b com mais de duas assinaturas. NPR-14101

`XTG`

* Ao imprimir um documento usando uma bandeja de desvio da impressora, a função `GeneratePrintedOutput` não permite a obtenção de papel da bandeja de desvio direita. NPR-14079

#### Designer do Forms {#forms-designer-2}

* O Forms Designer trava quando o usuário executa o utilitário Verificação ortográfica com a Localidade do formulário selecionada como Francês (Canadá). NPR-13740
* O Forms Designer trava quando o usuário seleciona calculate evento ou validate evento para um campo de formulário e altera a linguagem para JavaScript e insere `this.` na janela **[!UICONTROL Editor de scripts]**. NPR-12974

### Pacotes de recursos incluídos no CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms Add-on Package):

* Quando um formulário adaptável é criado a partir de um arquivo XDP, a tabulação para acessibilidade não segue o padrão definido. NPR-12562

`Adaptive forms` (Forms Add-on Package):

* O Construtor de regras para formulários adaptáveis não fornece acesso baseado em função. As alterações feitas por um autor não são rastreáveis. NPR-12840

`Core` (Instalador do Forms JEE):

* A funcionalidade CORS (CoreCross Origem Resource Sharing) como filtro de servlet não está ativada para Jpatrão+. NPR-13050

## Instruções de download para CFP via Software Distribution {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Para clientes da AEM Forms, é essencial instalar AEM pacote complementar de formulários após instalar qualquer AEM Service Pack, Cumulative Service Pack ou Feature Pack.

Você pode baixar o pacote CFP diretamente da Distribuição de software ou executar as seguintes etapas:

1. Abra [Distribuição de software](https://experience.adobe.com/downloads). Você precisa de uma Adobe ID para fazer logon na Software Distribution (Distribuição de software).
1. Toque em **[!UICONTROL Adobe Experience Manager]** disponível no menu de cabeçalho.
1. Toque no nome do pacote, selecione **[!UICONTROL Aceitar termos do EULA]** e toque em **[!UICONTROL Download]**.

## Instruções de instalação para CFP {#installation-instructions-for-cfp}

Esta seção aborda os requisitos e as etapas para instalar o CFP.

### Antes de instalar  {#before-you-install}

>[!NOTE]
>
>Os Feature Packs opcionais fornecidos pela Adobe depende da versão de lançamento e do Cumulative Fix Pack. Se você tiver algum Feature Pack instalado, entre em contato com a [equipe de Atendimento ao cliente do AEM](https://helpx.adobe.com/br/marketing-cloud/contact-support.html) para validar a compatibilidade com este Cumulative Fix Pack do AEM 6.2.

>[!NOTE]
>
>É recomendável executar a validação em cada novo pacote de instalação antes de tentar instalá-lo. A pré-validação analisa e relata todos os erros encontrados antes da instalação e avisa os usuários sobre esses erros, sobreposições e permissões de forma proativa.
>
>Você pode acessar a documentação para a opção Validar em [https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/pt/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* O AEM 6.2 Service Pack 1 é um pré-requisito para o CFP. Para obter instruções de instalação, consulte [Notas de versão do AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).

* O download do Cumulative Fix Pack está disponível em [Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20), que você pode acessar diretamente da instância AEM.
* Para uma implantação de cluster usando ( RDBMK ou MongoDB), o pacote CFP pode ser instalado em qualquer uma das instâncias do Autor que usa o Gerenciador de pacotes.

* Antes de instalar o Cumulative Fix Pack, verifique se você fez um instantâneo ou um backup da instância do AEM.
* Não há suporte para a desinstalação do CFP.

### Instale o CFP via Software Distribution {#install-the-cfp-via-package-share}

Execute as seguintes etapas para instalar o Cumulative Fix Pack em uma instância AEM 6.2 SP1 existente:

1. Clique no link [Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) para baixar o pacote.

1. Abra [Gerenciador de pacotes](http://localhost:4502/crx/packmgr/index.jsp) e clique em **[!UICONTROL Carregar pacote]** para fazer upload do pacote.

1. Selecione o nome do pacote e clique em **[!UICONTROL Instalar]**.

### Instalação automática {#automatic-installation}

O CFP pode ser instalado automaticamente em uma instância em execução das seguintes maneiras:

* Coloque o pacote em ../crx-quickstart/install enquanto o servidor estiver em execução. O pacote é instalado automaticamente.
* Use a [API HTTP do Package Manager](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html) - certifique-se de usar `cmd=install&recursive=true` - para que o pacote aninhado esteja instalado.

### Validar instalação {#validate-installation}

1. A página Informações do produto (/system/console/ productinfo ) agora deve mostrar a string da versão atualizada &quot;Adobe Experience Manager, Versão 6.2.0.SP1-CFP20&quot; em Produtos instalados.
1. Todos os pacotes OSGI são ATIVOS ou FRAGMENTOS no Console OSGi (Use o console da Web: /system/console/bundles).

>[!NOTE]
>
>Na instalação bem-sucedida do pacote, uma mensagem informativa é exibida indicando que o pacote de conteúdo foi instalado com êxito, como &quot;Pacote de conteúdo AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 instalado com êxito&quot;.

>[!NOTE]
>
>Desde AEM 6.2 SP1-CFP1, o nível de log no Jackrabbit FileVault mudou de INFO para DEBUG para a maioria das mensagens. Para obter registros de instalação para um pacote de conteúdo instalado no AEM 6.2 SP1-CFP1 ou superior, ative o nível de log DEBUG para `org.apache.jackrabbit.vault.packaging.impl`.

### Instalar o AEM Forms {#install-forms}

>[!NOTE]
>
>Pule esta seção se não estiver usando o AEM Forms.

#### Instalar complemento do AEM Forms  {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms em JEE apenas**) O procedimento para instalar um CFP no AEM Forms em JEE está descrito em [Instalando CFP no AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Verifique se você instalou o pacote CFP AEM 6.2 SP1.
1. Baixe o pacote de complementos Forms correspondente listado em [Versões AEM Forms](aem-forms-releases.md) para seu sistema operacional.
1. Instale o pacote de complementos Forms conforme descrito em [Instalação de pacotes de suplementos de formulários AEM](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html).

#### Instalar pacote do AEM Forms JEE {#install-aem-forms-jee-bundles-package}

As correções no JEE do AEM Forms são entregues por meio de um instalador separado. Para obter informações sobre como instalar um CFP em AEM Forms no JEE, consulte [Instalação do CFP no AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Instalador do Designer do Forms  {#designer-installer}

1. Para instalar a atualização, execute o arquivo Designer6.2.0_&lt;Idioma>_Cumulative_QF.msp.
1. Na tela de Boas vindas, clique em **atualizar**. A instalação é iniciada.
1. Depois que a instalação for concluída, clique em **concluir**.

## Parâmetros de tempo limite configuráveis pelo usuário para conexões DTM, Analytics, Público alvo, Search &amp; Promote {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Com AEM Cumulative Fix Pack 6.2 SP1-CFP7 e versões posteriores, os períodos de tempo limite de conexão foram configuráveis em todas as conexões acima, conforme os detalhes abaixo:

| **Conexões** | **Tempo limite da conexão*** | **Tempo limite do soquete**** |
|---|---|---|
| DTM | 30000 ms | 30000 ms |
| Análise | 30000 ms | 30000 ms |
| Target | 60000 ms | 30000 ms |
| Pesquisar e promover | 30000 ms | 30000 ms |

* **Tempo limite da conexão*** - Tempo limite em milissegundos até que uma conexão seja estabelecida. Um valor de tempo limite zero é interpretado como um tempo limite infinito.
* **Tempo limite do soquete**** - Tempo limite em milissegundos para espera por dados ou um período máximo de inatividade entre dois pacotes de dados consecutivos.

>[!NOTE]
>
>Com AEM Cumulative Fix Pack 6.2 SP1-CFP6 e versões posteriores, a configuração OSGi usada para a Integração do Search &amp; Promote é a Configuração de proxy dos componentes HTTP Apache. A configuração Proxy do Day Commons HTTP Client 3.1 não é mais usada.

## Desabilitar o status de replicação no console de marcação (Interface clássica) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Caso esteja usando CFP3 ou posterior, siga estas instruções para desativar o Status de Replicação no console Marcação na interface clássica:

* Sobreposição *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* em */apps*

* Adicionar `replicationStateRequired`: &quot;false&quot; após a linha 416.

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## A última atualização 131 do Java 8 lança uma exceção (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Essas configurações são específicas para clientes AEM Forms que usam a segurança do Documento.

O NPR-21355 está incluído no CFP12.1. Se você estiver instalando o CFP12.1 ou posterior, execute o procedimento a seguir para configurar o NPR-21355 no servidor de aplicativos JBoss. Se você estiver instalando o CFP12.1 no servidor AEM Forms em execução nos servidores de aplicativos Oracle WebLogic ou IBM WebSpehere, nenhuma configuração adicional é necessária:

1. Faça backup, exclua e crie um novo arquivo module.xml. O local padrão do arquivo é [AEM_Forms_Installation_diretory]/jHead/modules/system/layers/base/com/adobe/livecycle/main/

1. Abra o arquivo module.xml recém-criado para edição. Adicione o seguinte código ao arquivo:

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. Crie um backup dos arquivos jsafeFIPS.jar, jsafeJCEFIPS.jar e certjFIPS.jar, localizados em [AEM_Forms_Installation_diretory]/jHead/modules/system/layers/base/com/adobe/livecycle/main/, e exclua os arquivos do diretório mencionado anteriormente.

   Entre em contato com [Suporte ao Adobe](https://helpx.adobe.com/marketing-cloud/contact-support.html) para obter novos arquivos JAR. Coloque os arquivos JAR obtidos de [Suporte ao Adobe](https://helpx.adobe.com/marketing-cloud/contact-support.html) em [AEM_Forms_Installation_diretory]/jHead/modules/system/layers/base/com/adobe/livecycle/main/

1. (Somente Windows) Modifique os arquivos de configuração `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` ou `domain.conf.bat`:

   * Para o servidor JBoss em configuração independente, abra o standalone.conf.bat para edição.
   * Para o servidor JBoss na configuração de cluster, abra o domínio.conf.bat para edição.

   Adicione as seguintes linhas no final e salve o arquivo:

   defina &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   defina &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. (Somente SO baseado em Linux) Modifique os arquivos de configuração [AEM_Forms_Installation_diretory]/jboss/standalone.conf ou domain.conf:

   * Para o servidor JBoss em configuração independente, abra o arquivo standalone.conf para edição.
   * Para o servidor JBoss na configuração de cluster, abra o domínio.conf para edição.

   Adicione as seguintes linhas no final e salve o arquivo:

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## Configurações necessárias para o NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>O NPR-19778 faz parte da PCP14.

A contagem de filas compartilhadas não é atualizada, por padrão, para outros usuários quando um usuário reclama uma tarefa. Para isso, introduzimos uma nova propriedade. Siga as etapas abaixo para configurar essa propriedade na instância do AEM:

1. Vá para IU administrativa -> Serviços -> Espaço de trabalho -> Administração global.
1. Exportar configurações globais.
1. No arquivo XML baixado, adicione a tag `<client_tasksPollingInterval>10</client_tasksPollingInterval>` Aqui, 10 é o exemplo de valor em segundos. É possível modificá-la de acordo.
1. Salve o arquivo.
1. Volte para IU administrativa -> Serviços -> Espaço de trabalho -> Administração global.
1. Importe o arquivo xml na seção Importar configurações globais.
1. Agora você pode fazer logout do sistema e login novamente.
1. A contagem de start da fila compartilhada que são atualizados para outros usuários na área de trabalho.
1. Para desativar a pesquisa, altere o valor para 0 e importe o arquivo XML novamente.

## Alterações na interface do usuário {#ui-changes}

* Alteração de comportamento na exibição de títulos no Cartão de imagem para Imagem com dc: propriedade title definida como String [] ( multifield ): somente o título alterado mais recente será exibido no cartão de imagem na interface do usuário, embora todos os títulos sejam salvos no CRX. Hotfix do CQ-4217165

## Problemas conhecidos {#known-issues}

* Atualizar AEM 6.2SP1-CFP19 e AEM 6.2SP1-CFP20 do CFP18 altera o redirecionamento raiz para a página de boas-vindas da interface clássica em vez de /sites.html/content. Talvez seja necessário corrigir a divisão: Propriedade de público alvo de /welcome.html para /index.html com o CRX Explorer. Esse problema não é observado na atualização do CFP17 ou versão anterior.

Os seguintes erros transitórios podem ocorrer ao instalar o AEM 6.2 SP1-CFPx. No entanto, não é necessária nenhuma resolução para esses erros, pois eles não afetam sua instância AEM e desaparecem depois que o CFP é instalado:

* Ao atualizar AEM instância 6.2SP1-CFP20 para AEM 6.5, alguns URLs personalizados podem não funcionar como:

   * */projects.html*
   * */sites.html*

No entanto, a solução alternativa é reiniciar a instância AEM após uma atualização.

* HTTP 500 Internal Server Error é recebido quando a página de detalhes do componente Webconsole é aberta.
* Erros porque **criar instância do componente** e **A fábrica do serviço devolveu null** ocorrem devido à reinicialização do repositório:

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Não é possível criar a instância do componente devido a falha ao vincular o profileManager de referência
   * org.apache.sling.commons.FrameworkEvent ERROR (org.osgi.framework.ServiceException: A fábrica de serviços retornou nulo. (Componente: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* Erro observado na instalação CFP em Mongo e DB2: **org.apache.sling.Discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Exceção: java.lang.NullPointerException**. Este erro não ocorrerá após a instalação de um CFP sobre CFP8.
* (Tarefa Adobe Granite Maintenance Scheduler Update) com.adobe.granite.manutenção.impl.TaskScheduler: Nenhuma tarefa de manutenção encontrada com o nome WorkflowPurgeTask para granite de janela:week
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* Quando você instala o CFPx no AEM 6.2 SP1 que inclui o pacote de recursos de Tags inteligentes, a etapa de fluxo de trabalho adicionada anteriormente para os Ativos de tags inteligentes é excluída do fluxo de trabalho Atualizar ativos do DAM.

Consulte lista de [Problemas conhecidos no AEM 6.2 SP1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known de problemas).

## Uber Jar {#uber-jar}

O Uber Jar para 6.2 SP1-CFP20 está disponível em [repositório Adobe Public Maven](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/).

Para usar o Uber Jar em um projeto Maven, inclua a seguinte dependência no POM do projeto:

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## Pacotes OSGI e de conteúdo incluídos {#osgi-bundles-and-content-packages-included-5}

O texto seguinte documentos a lista dos pacotes OSGI e dos pacotes de conteúdo incluídos no CFP.

* [Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP20](assets/do-not-localize/updated.txt)
* [Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP20](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [Página de hotfixes do AEM 6.2](https://helpx.adobe.com/br/experience-manager/kb/aem62-available-hotfixes.html)
>* [Notas de versão do AEM 6.2 SP1](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [Notas de versão do AEM 6.2](https://docs.adobe.com/docs/en/aem/6-2/release-notes.html)
>* [Página do produto AEM](http://www.adobe.com/solutions/web-experience-management.html)
>* [Documentação do AEM 6.2](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [Atualizações ](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) de produtos de prioridade de  [Adobe](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

