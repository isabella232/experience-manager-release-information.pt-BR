---
title: Versões anteriores de AEM, CQ e CRX
description: Pacotes de documentação para versões mais antigas do Adobe Experience Manager, CQ e CRX.
translation-type: tm+mt
source-git-commit: c8e7f79be233c94d33b7605c73e586dce022412c
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 25%

---


# Versões anteriores de [!DNL Adobe Experience Manager], CQ e CRX {#older-versions-aem-cq-crx}

## Versões anteriores da documentação [!DNL Experience Manager] {#older-version-aem-documentation}

As versões de [!DNL Experience Manager], CQ e CRX listadas nesta página são Fim da vida útil e não são mais vendidas oficialmente pelo Adobe. As versões mais recentes da documentação oficial referente às versões anteriores estão disponíveis para suas necessidades de auto-ajuda. Recomendamos que você atualize para a versão mais recente (que atualmente é [[!DNL Experience Manager] 6.5](https://experienceleague.adobe.com/docs/experience-manager-65.html)).

>[!NOTE]
>
>Para saber quando uma versão [!DNL Experience Manager] chegará ao fim do suporte principal, consulte [produtos e períodos de suporte técnico](https://helpx.adobe.com/br/support/programs/eol-matrix.html) e pesquise `AEM`.

### Antes de instalar {#before-installation}

Antes de baixar o pacote, determine quem usará o conteúdo. Essa decisão determinará como será a implantação:

* Desenvolvedores podem instalar localmente para acesso rápido às referências.
* Para questões de necessidade de documentação empresarial, é recomendado que o pacote seja implantado em uma instância do AEM Author de não produção e internacionalmente acessível.

>[!NOTE]
>
>Os usuários devem estar conectados à instância [!DNL Experience Manager] para acessar esse conteúdo no Autor [!DNL Experience Manager]. Por padrão, o conteúdo não é acessível no AEM Publish (por encontrar-se em /libs).

## Locais de distribuição de software {#software-distribution-locations}

Você exigirá um Adobe ID válido:

* Se você não tiver um Adobe ID, poderá criar um em www.adobe.com
Se precisar de ajuda para criar ou gerenciar seu Adobe ID, [consulte este guia](https://helpx.adobe.com/manage-account.html)

| [!DNL Experience Manager] Versão | Link de distribuição de software |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6,2 | [Baixar o AEM-DOCS-6.2 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-2.zip) |
| [!DNL Experience Manager] 6,1 | [Baixar o AEM-DOCS-6.1 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-6-1.zip) |
| [!DNL Experience Manager] 6,0 | [Baixar o AEM-DOCS-6.0 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip) |
| [!DNL Experience Manager] 5.6.1 | [Baixar o AEM-DOCS-5.6.1 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip) |
| [!DNL Experience Manager] 5,6 | [Baixar o AEM-DOCS-5.6 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip) |
| CQ 5.5 | [Baixar o CQ-DOCS-5.5 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip) |
| CQ 5.4 | [Baixar o CQ-DOCS-5.4 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip) |
| CQ 5.3 | [Baixar o CQ-DOCS-5.3 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip) |
| CRX 2.3 | [Baixar o CRX-DOCS-2.3 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip) |
| CRX 2.2 | [Baixar o CRX-DOCS-2.2 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip) |
| CRX 2.1 | [Baixar o CRX-DOCS-2.1 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip) |
| CRX 2.0 | [Baixar o CRX-DOCS-2.0 da Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip) |

## Como instalar um pacote de documentação {#how-to-install-documentation-package}

Para instalar um pacote de documentação herdado, é necessário ter [!DNL Experience Manager] instalado e em execução na unidade local ou na unidade de rede.

### Baixe o pacote de documentação {#download-documentation-package}

1. Na tabela acima, selecione o link para a versão da documentação [!DNL Experience Manager] a ser baixada. Por exemplo, AEM 5.6.1.

1. Faça logon usando seu Adobe ID. Se você não tiver uma ID, crie uma.

1. Selecione o botão **[!UICONTROL Download]**.

1. Você verá o seguinte:

![Exemplo de distribuição de software](assets/screen_shot_2020-07-10at161922.jpg)

### Instale o pacote na instância local {#install-package-local-instance}

1. Abra a interface do usuário [!DNL Experience Manager]. Em um navegador da Web, insira: `http://localhost:4502/`. Faça logon como um Administrador.

1. Selecione **[!UICONTROL Ferramentas]** > **[!UICONTROL Implantação]** > **[!UICONTROL Pacotes]**.

1. Na interface do usuário do Gerenciador de pacotes, selecione **[!UICONTROL Fazer upload do pacote]**.

1. Navegue para o local de download do pacote AEM 5.6.1 (aem-docs-5-6-1.zip).

1. Selecione o pacote e clique em **[!UICONTROL OK]**.

1. Quando o upload do pacote for concluído, será preciso instalá-lo.

1. Na interface do usuário do Gerenciador de pacotes, encontre o pacote e selecione **[!UICONTROL Instalar]**.

1. Na caixa de diálogo de confirmação, selecione **[!UICONTROL Instalar]** novamente. Observação: a instalação levará alguns minutos.

1. Em um navegador da Web, abra a página de documentação. Usando o exemplo AEM 5.6.1, o URL seria: http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html.

## Obtenha ajuda da comunidade [!DNL Experience Manager] {#get-help-from-aem-community}

Se tiver dúvidas sobre o uso do Experience Manager, recomendamos que você [entre em contato com nossos especialistas experientes da comunidade nos  [!DNL Experience Manager] fóruns](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community).
