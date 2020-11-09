---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318023"
---
# <span data-ttu-id="20b67-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="20b67-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="20b67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20b67-102">SYNOPSIS</span></span>
<span data-ttu-id="20b67-103">Создание действия правила перезаписи, заданного для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="20b67-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="20b67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20b67-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20b67-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20b67-105">DESCRIPTION</span></span>
<span data-ttu-id="20b67-106">Командлет **New-AzApplicationGatewayRewriteRuleActionSet** создает набор действий правила перезаписи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="20b67-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="20b67-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20b67-107">EXAMPLES</span></span>

### <span data-ttu-id="20b67-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20b67-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="20b67-109">Эта команда создает набор действий правила перезаписи и сохраняет результат в переменной с именем $action.</span><span class="sxs-lookup"><span data-stu-id="20b67-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="20b67-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20b67-110">PARAMETERS</span></span>

### <span data-ttu-id="20b67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b67-111">-DefaultProfile</span></span>
<span data-ttu-id="20b67-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20b67-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b67-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="20b67-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="20b67-114">Список конфигураций заголовков запросов</span><span class="sxs-lookup"><span data-stu-id="20b67-114">List of request header configurations</span></span>

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

### <span data-ttu-id="20b67-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="20b67-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="20b67-116">Список конфигураций заголовков ответов</span><span class="sxs-lookup"><span data-stu-id="20b67-116">List of response header configurations</span></span>

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

### <span data-ttu-id="20b67-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="20b67-117">-UrlConfiguration</span></span>
<span data-ttu-id="20b67-118">Настройка URL-адреса для множества действий</span><span class="sxs-lookup"><span data-stu-id="20b67-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="20b67-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b67-119">CommonParameters</span></span>
<span data-ttu-id="20b67-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20b67-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b67-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b67-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b67-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20b67-122">INPUTS</span></span>

### <span data-ttu-id="20b67-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="20b67-123">None</span></span>

## <span data-ttu-id="20b67-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20b67-124">OUTPUTS</span></span>

### <span data-ttu-id="20b67-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="20b67-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="20b67-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="20b67-126">NOTES</span></span>

## <span data-ttu-id="20b67-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20b67-127">RELATED LINKS</span></span>

[<span data-ttu-id="20b67-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20b67-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="20b67-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20b67-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="20b67-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20b67-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="20b67-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20b67-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="20b67-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="20b67-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="20b67-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="20b67-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="20b67-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="20b67-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="20b67-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="20b67-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)