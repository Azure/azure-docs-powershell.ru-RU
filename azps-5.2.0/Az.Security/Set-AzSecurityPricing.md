---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407895"
---
# <span data-ttu-id="c95ea-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c95ea-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="c95ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c95ea-102">SYNOPSIS</span></span>

<span data-ttu-id="c95ea-103">Включает или отключает планы Защитника Azure для подписки в Центре безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="c95ea-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="c95ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c95ea-104">SYNTAX</span></span>

### <span data-ttu-id="c95ea-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c95ea-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c95ea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c95ea-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c95ea-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c95ea-107">DESCRIPTION</span></span>

<span data-ttu-id="c95ea-108">Включив или отключив любой из планов Защитника Azure для подписки.</span><span class="sxs-lookup"><span data-stu-id="c95ea-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="c95ea-109">Дополнительные сведения о Защитнике Azure и доступных планах см. [в обзоре защитника Azure.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="c95ea-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="c95ea-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c95ea-110">EXAMPLES</span></span>

### <span data-ttu-id="c95ea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c95ea-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="c95ea-112">Включает **Защитник Azure для серверов** для подписки.</span><span class="sxs-lookup"><span data-stu-id="c95ea-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="c95ea-113">"Стандартный" означает состояние "В этом" для плана Azure Defender, как показано в области цен и параметров Центра безопасности Azure на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="c95ea-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="c95ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c95ea-114">PARAMETERS</span></span>

### <span data-ttu-id="c95ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c95ea-115">-DefaultProfile</span></span>

<span data-ttu-id="c95ea-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c95ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c95ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c95ea-117">-InputObject</span></span>

<span data-ttu-id="c95ea-118">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="c95ea-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c95ea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c95ea-119">-Name</span></span>

<span data-ttu-id="c95ea-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c95ea-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c95ea-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="c95ea-121">-PricingTier</span></span>

<span data-ttu-id="c95ea-122">Уровень цен.</span><span class="sxs-lookup"><span data-stu-id="c95ea-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c95ea-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c95ea-123">-Confirm</span></span>

<span data-ttu-id="c95ea-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c95ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c95ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c95ea-125">-WhatIf</span></span>

<span data-ttu-id="c95ea-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c95ea-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c95ea-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c95ea-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c95ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c95ea-128">CommonParameters</span></span>

<span data-ttu-id="c95ea-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c95ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c95ea-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c95ea-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c95ea-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c95ea-131">INPUTS</span></span>

### <span data-ttu-id="c95ea-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c95ea-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="c95ea-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c95ea-133">OUTPUTS</span></span>

### <span data-ttu-id="c95ea-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c95ea-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="c95ea-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c95ea-135">NOTES</span></span>

## <span data-ttu-id="c95ea-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c95ea-136">RELATED LINKS</span></span>