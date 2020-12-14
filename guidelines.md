---
source-git-commit: 65c8c0b9940f9d2e20234ccc65b1d819971ea52e
workflow-type: tm+mt
translation-type: tm+mt
source-wordcount: '752'
ht-degree: 5%

---
# Diretrizes para contribuição à documentação da Adobe Experience Manager

## Filosofia da documentação

Sabemos que os usuários do Adobe Experience Manager estão trabalhando em ambientes altamente competitivos, lutando para criar experiências digitais que os separarão de seus concorrentes. Portanto, é vital que, quando a Adobe oferece novas ferramentas avançadas em AEM, essas ferramentas sejam complementadas com documentação precisa e clara para permitir que o cliente aproveite imediatamente seu investimento AEM e maximize o ROI.

O objetivo da documentação AEM é colocar a documentação nas mãos dos usuários AEM assim que possível. Portanto, priorizamos a documentação precisa e utilizável e nos esforçamos para atualizá-la continuamente e aprimorá-la.

## Contribuições de documentação

Para melhorar continuamente a documentação AEM, a comunidade inteira de usuários AEM é bem-vinda para contribuir com a documentação. Seja por meio de solicitações ou problemas, as melhorias na documentação podem ser correções, esclarecimentos, expansões e exemplos adicionais.

## Normas de documentação

Embora nos congratulemos com os contributos para a nossa documentação, qualquer contribuição para a documentação AEM, quer sob a forma de um pedido de remessa, quer sob a forma de um problema, deverá estar em conformidade com as nossas normas de contribuição e documentação.

As contribuições que não cumprem estes padrões podem ser rejeitadas.

### Nós documento casos de uso padrão.

AEM documentação abrange casos de uso padrão. Casos de uso que não se enquadram no escopo da instalação padrão e da utilização do produto não fazem parte AEM documentação.

### Geralmente, não documento erros nem as suas soluções.

AEM documentação abrange casos de uso padrão. Por essa razão, os erros, os efeitos causados por erros e as soluções alternativas para erros geralmente não estão documentados.

As exceções a essa regra se aplicam às notas de versão, onde os problemas conhecidos podem ser listados com possíveis soluções que foram aprovadas pelo Gerenciamento de produtos AEM.

### As contribuições para a documentação não se destinam a responder a questões técnicas.

Quaisquer ideias que você precise melhorar AEM documentação são bem-vindas como contribuições. No entanto, comentários, problemas e solicitações pull destinam-se apenas a *contribuições*. Eles não devem ser usados para responder suas perguntas sobre como usar AEM, implementar seu projeto AEM ou resolver problemas técnicos.

Quaisquer dúvidas sobre o uso de erros AEM ou técnicos que você possa ter devem ser relatadas por meio do processo de suporte normal por meio do [portal de suporte empresarial do Experience Cloud](https://helpx.adobe.com/br/contact/enterprise-support.ec.html) ou discutidas na [comunidade do Experience Manager](https://forums.adobe.com/community/experience-cloud/marketing-cloud/experience-manager).

***AEM contribuições de documentação não são uma substituição da*** Carreira do Cliente do Adobe, e quaisquer contribuições que busquem respostas para perguntas relacionadas ao suporte serão rejeitadas.

### As contribuições devem mencionar claramente as páginas de documentação afetadas.

Se você criar um problema para sugerir melhorias na documentação, deverá incluir links para as páginas afetadas. Caso crie um problema usando o link **Editar esta página** em uma página de documentação, o problema será criado automaticamente com um link para a página.

Isso não se aplica a solicitações de baixa automática, pois as solicitações de baixa automática por sua natureza fazem referência às páginas afetadas.

## Diretrizes de documentação

Solicitamos que qualquer contribuição para nossa documentação siga determinadas diretrizes de estilo.

Seguir essas diretrizes facilita a revisão de sua contribuição e, portanto, a integração à nossa documentação é mais rápida.

### Idioma e estilo

#### Idioma

* AEM documentação foi criada e mantida em inglês dos EUA.
* Mantenha as frases o mais simples possível.
* Mantenha o idioma claro e conciso.

Lembre-se de que os leitores de AEM documentação são do mundo inteiro e não se pode esperar que sejam falantes nativos ou fluentes do inglês. Evite coloquialismos e mantenha a linguagem o mais clara e simples possível.

#### Siga o Manual de estilo da Microsoft

[O Manual de ](https://docs.microsoft.com/en-us/style-guide/welcome/) estilo da Microsoft é um guia de estilo de documentação disponível gratuitamente, que se concentra na documentação do software e AEM documentação segue este guia sempre que possível.

### Formatação

| Item | Estilo |
|---|---|
| Elemento ou opção da interface do usuário | **negrito** |
| Nome do arquivo, caminho, entrada do usuário, valores de parâmetro | `monospaced` |
| Código, linha de comando | ```Code Block``` |

### Capturas de tela

As capturas de tela devem ser utilizadas de forma sensata e apenas quando uma descrição textual for insuficiente.

Marcadores ou outras anotações em capturas de tela (como quadros vermelhos, setas ou texto) não devem ser usados. Dessa forma, as capturas de tela são mais fáceis de reutilizar ou replicar em versões localizadas da documentação.

### Referências específicas à versão

Tente evitar referências diretas a uma versão específica em todo o conteúdo da documentação, sempre que possível. Isso torna a documentação mais flexível e extensível para versões futuras.

### Uso do dia, AEM, CQ, CRX

O produto deve ser sempre referenciado pelo nome completo **Adobe Experience Manager** pela primeira vez em um artigo e pode, a partir daí, ser chamado de **AEM**.

O Dia, o Day Software, o CQ e o CRX não devem ser usados, exceto quando inevitável, como em nomes de classe ou referência ao histórico de AEM.