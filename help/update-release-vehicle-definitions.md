---
title: Atualizar Definições do Veículo de Liberação
description: 'Este artigo detalha os vários tipos de versões, incluindo versões completas, pacotes de recursos e pacotes de serviços. [!DNL Experience Manager] '
contentOwner: AK
translation-type: tm+mt
source-git-commit: 11ff4f7d66038a80697afe5f104c560137e130f4
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 5%

---


# [!DNL Experience Manager] atualizar as definições dos veículos de versão  {#update-release-vehicle-definitions}

Este documento inclui detalhes sobre os vários tipos de versões [!DNL Adobe Experience Manager], incluindo versões completas, pacotes de recursos e pacotes de serviços que [!DNL Adobe] oferece aos seus clientes.

>[!NOTE]
>
>Para obter o cronograma de versões de [!DNL Experience Manager] atualizações, consulte [[!DNL Experience Manager] o roteiro de versões de atualização](update-releases-roadmap.md)

## Versão completa {#full-release}

| Itens | Descrição |
|-------|------|
| Definição | <ul> <li> Versão programada </li> <li> Suporta caminhos de atualização para versões específicas, que são definidos nas notas de versão </li> </ul> |
| Nomeação | <ul> <li> Os números de versão das principais versões aumentam com base na fórmula X+1.Y.Z. </li> <li> Os números de versão para versões secundárias aumentam com base na fórmula X.Y+1.Z </li> </ul> Onde X é o número da versão primária, Y é o número da versão secundária e Z o número do patch. |
| Inclusões | <ul> <li> Novos recursos </li> <li>  Melhorias </li> <li>  Correções de erros </li> </ul> |
| Documentação | <ul> <li> As notas de versão estão disponíveis no portal de documentação </li> <li> A documentação sobre recursos, melhorias e correções de erros está disponível no portal de documentação </li> </ul> |
| Cadência | Anualmente |
| Disponibilidade e instalação | <ul> <li> Fornecido como instalador de produto independente </li> <li>  Disponível no site de licenciamento e na Managed Services </li> <li> O site de licenciamento pode exigir a migração do repositório de conteúdo </li> </ul> |
| Nível de teste | Totalmente validado pelo controle de qualidade |

## Service Pack {#service-pack}

| Item | Descrição |
|-----|-----|
| Definição | <ul> <li> Versão programada </li> <li> Atualmente, não é possível reverter </li> </ul> |
| Nomeação | <ul> <li> O número de versão do patch é um número de um único dígito </li> <li> Após a instalação, aumentará o dígito de correção do número de versão instalado, com base na fórmula X.Y.Z.SPx </li> </ul> Onde X é o número da versão primária, Y é o número da versão secundária e Z o número do patch. x é o número do service pack. |
| Inclusões | <ul> <li> Novos recursos</li> <li>  Melhorias </li> <li> Correções de erros </li> <li> Pacotes de recursos de interesse comum (se houver) </li> </ul> |
| Documentação | <ul> <li> Notas de versão disponíveis no portal de documentação </li> <li> Documentação sobre recursos, melhorias, correções de erros no portal de documentação </li> </ul> |
| Cadência | Trimestral |
| Disponibilidade e instalação | <ul> <li> Entregue como um pacote </li> <li> Disponível na distribuição de software</li> <li>  Requer instalação funcional existente </li> </ul> |
| Nível de teste | <ul> <li> Todas as correções validadas </li> <li>  Sanidade geral do pacote com execuções de automação </li> </ul> |

## Cumulative Fix Pack  {#cumulative-fix-pack-aem}

| Item | Descrição |
|-----|-----|
| Definição | <ul> <li> Modelo de delivery único para liberação de correções </li> <li> Pacote de conteúdo do agregador contendo o pacote de conteúdo de componentes individuais </li> <li>  Os CFPs são sobrepostos de hot fixes e nenhum aprimoramento faz parte dele.  </li> </ul> |
| Nomeação | X.Y.Z.CFPx <br> Onde X é o número da versão primária, Y é o número da versão secundária e Z o número do patch. x é o número cumulativo do service pack. |
| Inclusões | CFP é um pacote de correções cumulativo que contém correções de todos os componentes em datas especificadas. Por exemplo, se um cliente aplicar CFP3, então CFP3 = CFP1 + CFP2. |
| Documentação | Notas de versão disponíveis no portal de documentação |
| Cadência | Trimestral |
| Disponibilidade e instalação | <ul> <li> Entregue como um pacote </li> <li>  Disponível na distribuição de software </li> <li>  Dependendo do service pack mais recente lançado </li> <li>  A PCP é autodependente. Os clientes não precisam se preocupar em encontrar/resolver dependências. O CFP deve ser instalado no Service Pack lançado mais recentemente. </li> <li>  O CFP pode ser instalado como um único pacote, o que melhora a experiência do cliente.  </li> </ul> |
| Nível de teste | Garantia de qualidade validada no nível de integração e teste de regressão |

## Sobreposição {#overlay}

| Item | Detalhes |
|-------|--------|
| Nomeação | overlay-&lt;ID do tíquete> |
| Inclusões | Correção de erros para um arquivo JS ou JSP |
| Documentação | Nenhum |
| Cadência | Se necessário |
| Disponibilidade e instalação | <ul> <li> Entregue como pacote pelo [!DNL Experience Manager] Atendimento ao cliente  </li> <li> Não necessariamente incluído em service packs ou versões completas </li> </ul> |
| Nível de teste | Validado pelo Atendimento ao cliente |

## Feature Pack {#feature-pack}

| Itens | Detalhes |
|--------|-----|
| Definição | <ul> <li>Pacotes de recursos são funcionalidades complementares e são fornecidos por Service Packs. Se uma versão [!DNL Experience Manager] tiver lançado seu último service pack, o Adobe não fornecerá nenhum pacote de recursos para ele no futuro. </li> <li> Os FPs contêm aprimoramentos de produtos, programados para uma versão subsequente do produto, mas disponibilizados antecipadamente com base na decisão do [!DNL Adobe's] Gerenciamento de produtos.</li> <li>  Os recursos são sempre mesclados com a próxima versão principal e, em seguida, portados para a versão [!DNL Experience Manager] exigida pelo cliente </li> <li>  Os pacotes de recursos de interesse comum e GA são mesclados no próximo service pack  </li> </ul> |
| Nomeação | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusões | <ul> <li> Novos recursos </li> <li> Melhorias </li> <li> Correções de erros (atualizações de produtos incrementais) </li> </ul> |
| Documentação | A documentação está disponível em adobe.com. |
| Cadência | Varia com a área do Produto |
| Disponibilidade e instalação | <ul> <li>Entregue por Service Packs </li> <li> Disponível na Distribuição de software. Os clientes aceitam [!DNL Adobe's] Termos e condições por meio da Distribuição de software. </li> </ul> |
| Nível de teste | Os pacotes de recursos de Disponibilidade Geral são validados para QA. |

* 1: As correções OAK não são entregues como hot fixes individuais. No entanto, eles estão incluídos na correção Cumulative Oak subsequente. Se necessário, uma compilação de diagnóstico sobre o COFP mais recente pode ser disponibilizada. A condição prévia é que o cliente tenha o COFP mais recente em execução. As compilações de diagnóstico fornecem somente o mesmo nível de garantia de qualidade que uma correção. Portanto, eles não fornecem o mesmo nível de garantia de qualidade que um pacote de correções cumulativo, service pack ou versão do produto. A correção final é feita com o próximo CFP.
