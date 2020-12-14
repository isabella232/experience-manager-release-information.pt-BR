---
title: Instalação de pacotes de correção cumulativos no AEM Forms JEE
description: Resumo das etapas para instalar e configurar o Cumulative Fix Pack (CFP) no AEM Forms JEE
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 1%

---


# Instalando Pacotes de Correções Cumulativas em AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Instale o CFP no AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Execute as seguintes etapas, na sequência especificada, para instalar o pacote de correção cumulativo em AEM 6.3 [!DNL Forms JEE].

1. Entre em contato com [Suporte ao Adobe](https://www.adobe.com/account/sign-in.supportportal.html) para obter o instalador do AEM 6.3 [!DNL Forms JEE] para o CFP.
1. Execute o instalador CFP e configure AEM [!DNL Forms JEE] conforme descrito em [Instalar e configurar AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Instale o AEM CFP mais recente [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. Instale o pacote complementar [!DNL Forms] para AEM CFP [6.3.3.x](aem-forms-releases.md)

### Instalar AEM [!DNL Forms JEE] pacotes {#install-aem-forms-jee-bundles-package}

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1; a versão 1.0.2) fornece ao  [!DNL Forms] usuário AEM  [!DNL Forms JEE] os mesmos direitos e recursos que no AEM  [!DNL Forms OSGi]. Verifique os pacotes instalados no Gerenciador de pacotes e instale o pacote se ele ainda não estiver instalado.

### Instruções adicionais para CQ-4208044 {#additional-instructions-for-cq}

Se você estiver usando o servidor AEM 6.3 [!DNL Forms JEE] com o banco de dados Oracle, defina as seguintes configurações após a implantação do CFP1, ou seja, depois que o Configuration Manager for executado. Essa configuração é necessária para sincronizar usuários, grupos e membros de grupo quando a sincronização do domínio corporativo é executada. Consulte o problema CQ-4208044 em [AEM notas de versão 6.3](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205).

1. Faça logon na interface do usuário **Admin**.
1. Navegue até **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciamento de usuários]** > **[!UICONTROL Configuração]** > **[!UICONTROL Importar e exportar arquivo de configuração]**
1. Exporte o arquivo config.xml.
1. Modifique a entrada para &quot; `groupMemberDBQueryBatchSize`&quot; em suas configurações de domínio em *config.xml*. Amostra de entrada:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. Importe o arquivo modificado novamente e execute a sincronização novamente.

## Instale o CFP no AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Execute as seguintes etapas, na sequência especificada, para instalar o pacote de correção cumulativo em AEM 6.2 [!DNL Forms JEE].

>[!NOTE]
>
>Se você estiver no AEM 6.2 [!DNL Forms OSGi], siga as instruções de instalação em [AEM notas de versão CFP 6.2.](release-notes-aem-6-2-cumulative-fix-pack.md)

1. Entre em contato com [Suporte ao Adobe](https://www.adobe.com/account/sign-in.supportportal.html) para obter o instalador do AEM 6.2 [!DNL Forms JEE] para o CFP.
1. Execute o instalador CFP e configure AEM [!DNL Forms JEE] conforme descrito em [Instalar e configurar AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Instale [AEM Hotfix 12785 versão 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785).
1. Instale o [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).
1. Instale o mais recente [AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md).
1. Instale o pacote complementar [!DNL Forms] para [AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md).

### Instalar AEM [!DNL Forms JEE] pacotes {#install-aem-forms-jee-bundles-package-1}

[Pacote](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24)  AEM Forms JEE (aemfd-jee-bundles-package-6.2CFP5; a versão 1.0.2) fornece ao  [!DNL Forms] usuário AEM  [!DNL Forms JEE] os mesmos direitos e recursos que no AEM  [!DNL Forms OSGi]. Verifique os pacotes instalados no Gerenciador de pacotes e instale o pacote se ele ainda não estiver instalado.

### Configurando o tempo limite para operações no nível do componente (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Após o AEM 6.2 CFP4, você pode usar as seguintes instruções para configurar o tempo limite para operações do DSC, caso tenha problemas devido ao tempo limite durante o processo de atualização. (Consulte NPR-16774 em [AEM notas de versão 6.2 CFP4](release-notes-aem-6-2-cumulative-fix-pack.md)).

A implantação do DSC leva um tempo variável devido ao qual pode falhar. Para alterar o tempo limite de operações do DSC, como Instalar, Carregar, Start e Parar, é necessário definir `adobe.component.registry.timeout` usando o argumento JVM com a opção -D.

Especifique o valor da chave em segundos. Por exemplo: `-Dadobe.component.registry.timeout=300`

Você também pode alterar os tempos limite no nível do componente usando as três propriedades a seguir:

1. `adobe.all-component.timeout`: substitui os tempos limite de todos os Serviços do Produto.
1. `adobe.<serviceName>.timeout`: substitui o tempo limite somente para o serviço (&lt;servicename>) mencionado na chave. Se o valor no nível de serviço for definido, o uso desse comando substituirá somente o valor do tempo limite do serviço especificado se ele for definido no nível de Aplicativo.
1. `adobe.<serviceName>.<operationName>.timeout`: Ele só substitui o tempo limite da operação do serviço específico(&lt;servicename>.&lt;operationname>) mencionado na chave. Se o valor for definido no nível Operação, então usar esse comando substituirá somente o valor do tempo limite do serviço especificado se ele for definido no nível Aplicativo ou no nível Serviço.

**Exemplos:**

Use os seguintes comandos para definir o tempo limite no nível do componente:

1. Para definir o tempo limite de todas as operações de serviço como 600 segundos:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Para definir o tempo limite de valores de operação `DesigntimeService` como 500 segundos, use:

   defina &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Para definir o tempo limite de valores de operação `DesigntimeService's previewLCA` como 700 segundos, use:

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Para definir `DSC operations` como load, install etc. como 600 s, use:

   defina &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Instalar e configurar AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Faça um backup da pasta /deployel. É necessário se você decidir desinstalar a correção rápida.
1. Pare o servidor de aplicativos.
1. Extraia o arquivo de arquivamento do instalador de patch para o disco rígido.
1. No diretório nomeado de acordo com o sistema operacional que você está usando:

   **Windows**

   Navegue até o diretório apropriado na mídia de instalação ou pasta no disco rígido onde você copiou o instalador:

   * (Windows de 32 bits): Disk1\InstData\Windows\VM
   * (Windows de 64 bits): Disk1\InstData\Windows_64bit\VM

   Em seguida, clique com o duplo no arquivo chamado:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux, Solaris, AIX**

   Navegue até o diretório apropriado:

   * (Linux): Disk1/InstData/Linux/NoVM
   * (Solaris): Disk1/InstData/Solaris/NoVM
   * (AIX): Disk1/InstData/AIX/VM

   Em um prompt de comando, digite:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Isso inicia um assistente de instalação que o guia pela instalação.

1. No painel Introdução, clique em **[!UICONTROL Próximo]**.
1. Na tela Escolher pasta de instalação, verifique se o local padrão exibido está correto para sua instalação existente ou clique em **[!UICONTROL Procurar]** para selecionar a pasta alternativa na qual AEM [!DNL Forms] está instalado no momento e clique em **[!UICONTROL Próximo]**.
1. Leia as informações de Resumo do patch de correção rápida e clique em **[!UICONTROL Próximo]**.
1. Leia as informações de Resumo de pré-instalação e clique em **[!UICONTROL Instalar]**.
1. Quando a instalação estiver concluída, clique em **[!UICONTROL Next]** para aplicar as atualizações de correção rápida aos arquivos instalados.
1. A caixa de seleção Gerenciador de configuração de Start é selecionada por padrão. Clique em **[!UICONTROL Done]** para executar o Configuration Manager.

   Para executar o Configuration Manager mais tarde, desmarque a opção **[!UICONTROL Configuration Manager]** do Start antes de clicar em **[!UICONTROL Done]**. Você pode start o Configuration Manager posteriormente usando o script apropriado no diretório *`[AEM_forms_root]`/configurationManager/bin*.

1. Dependendo do servidor de aplicativos, escolha um dos seguintes documentos e siga as instruções na seção *Configuração e implantação AEM[!DNL Forms]*.

   Para AEM [!DNL Forms] 6.3, consulte:

   * [Instalação e implantação do  [!DNL Forms] AEM para JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [Instalação e implantação do  [!DNL Forms] AEM para WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [Instalação e implantação do  [!DNL Forms] AEM para WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   Para AEM [!DNL Forms] 6.2, consulte:

   * [Instalação e implantação do  [!DNL Forms] AEM para JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62)
   * [Instalação e implantação do  [!DNL Forms] AEM para WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62)
   * [Instalação e implantação do  [!DNL Forms] AEM para WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62)

   Para o AEM Forms 6.1, consulte:

   * [Instalação e implantação do  [!DNL Forms] AEM para JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [Instalação e implantação do  [!DNL Forms] AEM para WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [Instalação e implantação do  [!DNL Forms] AEM para WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. Reinicie AEM servidor JEE [!DNL Forms].
