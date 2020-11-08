---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235347"
---
# <span data-ttu-id="2c6f5-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2c6f5-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="2c6f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6f5-103">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="2c6f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c6f5-104">SYNTAX</span></span>

### <span data-ttu-id="2c6f5-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c6f5-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c6f5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2c6f5-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c6f5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6f5-107">DESCRIPTION</span></span>
<span data-ttu-id="2c6f5-108">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="2c6f5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c6f5-109">EXAMPLES</span></span>

### <span data-ttu-id="2c6f5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c6f5-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="2c6f5-111">Настройка ценовой категории центра безопасности Azure по подписке "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="2c6f5-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="2c6f5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c6f5-112">PARAMETERS</span></span>

### <span data-ttu-id="2c6f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6f5-113">-DefaultProfile</span></span>
<span data-ttu-id="2c6f5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c6f5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c6f5-115">-InputObject</span></span>
<span data-ttu-id="2c6f5-116">Объект input.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-116">Input Object.</span></span>

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

### <span data-ttu-id="2c6f5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c6f5-117">-Name</span></span>
<span data-ttu-id="2c6f5-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-118">Resource name.</span></span>

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

### <span data-ttu-id="2c6f5-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="2c6f5-119">-PricingTier</span></span>
<span data-ttu-id="2c6f5-120">Ценовая Категория.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-120">Pricing Tier.</span></span>

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

### <span data-ttu-id="2c6f5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c6f5-121">-Confirm</span></span>
<span data-ttu-id="2c6f5-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c6f5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c6f5-123">-WhatIf</span></span>
<span data-ttu-id="2c6f5-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c6f5-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c6f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6f5-126">CommonParameters</span></span>
<span data-ttu-id="2c6f5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c6f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6f5-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c6f5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6f5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c6f5-129">INPUTS</span></span>

### <span data-ttu-id="2c6f5-130">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2c6f5-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="2c6f5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6f5-131">OUTPUTS</span></span>

### <span data-ttu-id="2c6f5-132">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2c6f5-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="2c6f5-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c6f5-133">NOTES</span></span>

## <span data-ttu-id="2c6f5-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c6f5-134">RELATED LINKS</span></span>
