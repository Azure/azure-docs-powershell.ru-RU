---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421839"
---
# <span data-ttu-id="59414-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="59414-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="59414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59414-102">SYNOPSIS</span></span>
<span data-ttu-id="59414-103">Создает набор действий по переописи правил для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="59414-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="59414-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59414-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59414-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59414-105">DESCRIPTION</span></span>
<span data-ttu-id="59414-106">При наступлении нового **azApplicationGatewayRewriteRuleActionSet** создается набор действий по перезаписи для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="59414-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="59414-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59414-107">EXAMPLES</span></span>

### <span data-ttu-id="59414-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59414-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="59414-109">Эта команда создает набор действий для изменения правил и сохраняет результат в переменной с именем $action.</span><span class="sxs-lookup"><span data-stu-id="59414-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="59414-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59414-110">PARAMETERS</span></span>

### <span data-ttu-id="59414-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59414-111">-DefaultProfile</span></span>
<span data-ttu-id="59414-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59414-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59414-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="59414-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="59414-114">Список конфигураций загона запросов</span><span class="sxs-lookup"><span data-stu-id="59414-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59414-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="59414-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="59414-116">Список конфигураций для заглавных ответов</span><span class="sxs-lookup"><span data-stu-id="59414-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59414-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="59414-117">-UrlConfiguration</span></span>
<span data-ttu-id="59414-118">Настройка URL-адреса для набора действий</span><span class="sxs-lookup"><span data-stu-id="59414-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59414-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59414-119">CommonParameters</span></span>
<span data-ttu-id="59414-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59414-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59414-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59414-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59414-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59414-122">INPUTS</span></span>

### <span data-ttu-id="59414-123">Нет</span><span class="sxs-lookup"><span data-stu-id="59414-123">None</span></span>

## <span data-ttu-id="59414-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59414-124">OUTPUTS</span></span>

### <span data-ttu-id="59414-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="59414-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="59414-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59414-126">NOTES</span></span>

## <span data-ttu-id="59414-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59414-127">RELATED LINKS</span></span>

[<span data-ttu-id="59414-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59414-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59414-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59414-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59414-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59414-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59414-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59414-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59414-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59414-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59414-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="59414-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="59414-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="59414-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="59414-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="59414-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)