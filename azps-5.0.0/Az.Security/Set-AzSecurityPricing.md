---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247997"
---
# <span data-ttu-id="25eed-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="25eed-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="25eed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25eed-102">SYNOPSIS</span></span>
<span data-ttu-id="25eed-103">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="25eed-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="25eed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25eed-104">SYNTAX</span></span>

### <span data-ttu-id="25eed-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25eed-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25eed-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="25eed-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25eed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25eed-107">DESCRIPTION</span></span>
<span data-ttu-id="25eed-108">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="25eed-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="25eed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25eed-109">EXAMPLES</span></span>

### <span data-ttu-id="25eed-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25eed-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="25eed-111">Настройка ценовой категории центра безопасности Azure по подписке "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="25eed-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="25eed-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25eed-112">PARAMETERS</span></span>

### <span data-ttu-id="25eed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25eed-113">-DefaultProfile</span></span>
<span data-ttu-id="25eed-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25eed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25eed-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25eed-115">-InputObject</span></span>
<span data-ttu-id="25eed-116">Объект input.</span><span class="sxs-lookup"><span data-stu-id="25eed-116">Input Object.</span></span>

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

### <span data-ttu-id="25eed-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25eed-117">-Name</span></span>
<span data-ttu-id="25eed-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="25eed-118">Resource name.</span></span>

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

### <span data-ttu-id="25eed-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="25eed-119">-PricingTier</span></span>
<span data-ttu-id="25eed-120">Ценовая Категория.</span><span class="sxs-lookup"><span data-stu-id="25eed-120">Pricing Tier.</span></span>

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

### <span data-ttu-id="25eed-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25eed-121">-Confirm</span></span>
<span data-ttu-id="25eed-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25eed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25eed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25eed-123">-WhatIf</span></span>
<span data-ttu-id="25eed-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25eed-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25eed-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25eed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25eed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25eed-126">CommonParameters</span></span>
<span data-ttu-id="25eed-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25eed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25eed-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25eed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25eed-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25eed-129">INPUTS</span></span>

### <span data-ttu-id="25eed-130">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="25eed-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="25eed-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25eed-131">OUTPUTS</span></span>

### <span data-ttu-id="25eed-132">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="25eed-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="25eed-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="25eed-133">NOTES</span></span>

## <span data-ttu-id="25eed-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25eed-134">RELATED LINKS</span></span>
