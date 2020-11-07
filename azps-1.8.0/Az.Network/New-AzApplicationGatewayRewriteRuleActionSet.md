---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f13591a92b52e00ed94e93fec480d810037f061d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730388"
---
# <span data-ttu-id="371bc-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="371bc-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="371bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="371bc-102">SYNOPSIS</span></span>
<span data-ttu-id="371bc-103">Создает набор действий правила перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="371bc-103">Creates a rewrite rule actionset for an application gateway.</span></span>

## <span data-ttu-id="371bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="371bc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="371bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="371bc-105">DESCRIPTION</span></span>
<span data-ttu-id="371bc-106">Командлет **New-AzApplicationGatewayRewriteRuleActionSet** создает набор действий правила перезаписи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="371bc-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="371bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="371bc-107">EXAMPLES</span></span>

### <span data-ttu-id="371bc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="371bc-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="371bc-109">Эта команда создает набор действий правила перезаписи и сохраняет результат в переменной с именем $action.</span><span class="sxs-lookup"><span data-stu-id="371bc-109">This command creates a rewrite rule actionset and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="371bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="371bc-110">PARAMETERS</span></span>

### <span data-ttu-id="371bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371bc-111">-DefaultProfile</span></span>
<span data-ttu-id="371bc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="371bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="371bc-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="371bc-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="371bc-114">Список конфигураций заголовков запросов</span><span class="sxs-lookup"><span data-stu-id="371bc-114">List of request header configurations</span></span>

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

### <span data-ttu-id="371bc-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="371bc-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="371bc-116">Список конфигураций заголовков ответов</span><span class="sxs-lookup"><span data-stu-id="371bc-116">List of response header configurations</span></span>

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

### <span data-ttu-id="371bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371bc-117">CommonParameters</span></span>
<span data-ttu-id="371bc-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="371bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371bc-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371bc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371bc-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="371bc-120">INPUTS</span></span>

### <span data-ttu-id="371bc-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="371bc-121">None</span></span>

## <span data-ttu-id="371bc-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="371bc-122">OUTPUTS</span></span>

### <span data-ttu-id="371bc-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="371bc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="371bc-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="371bc-124">NOTES</span></span>

## <span data-ttu-id="371bc-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="371bc-125">RELATED LINKS</span></span>

[<span data-ttu-id="371bc-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="371bc-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="371bc-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="371bc-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="371bc-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="371bc-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="371bc-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="371bc-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="371bc-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="371bc-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="371bc-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="371bc-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="371bc-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="371bc-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
