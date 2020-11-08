---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: af51b5d864591f868db2ae588eed1d727fc53239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073755"
---
# <span data-ttu-id="cee74-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cee74-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="cee74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cee74-102">SYNOPSIS</span></span>
<span data-ttu-id="cee74-103">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="cee74-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="cee74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cee74-104">SYNTAX</span></span>

### <span data-ttu-id="cee74-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cee74-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee74-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cee74-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee74-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cee74-107">DESCRIPTION</span></span>
<span data-ttu-id="cee74-108">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="cee74-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="cee74-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cee74-109">EXAMPLES</span></span>

### <span data-ttu-id="cee74-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cee74-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="cee74-111">Настройка ценовой категории центра безопасности Azure по подписке "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="cee74-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="cee74-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cee74-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="cee74-113">Задает для центра безопасности "myService1" группы ресурсов Azure ценовую категорию "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="cee74-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="cee74-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cee74-114">PARAMETERS</span></span>

### <span data-ttu-id="cee74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee74-115">-DefaultProfile</span></span>
<span data-ttu-id="cee74-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cee74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cee74-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cee74-117">-InputObject</span></span>
<span data-ttu-id="cee74-118">Объект input.</span><span class="sxs-lookup"><span data-stu-id="cee74-118">Input Object.</span></span>

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

### <span data-ttu-id="cee74-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cee74-119">-Name</span></span>
<span data-ttu-id="cee74-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cee74-120">Resource name.</span></span>

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

### <span data-ttu-id="cee74-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="cee74-121">-PricingTier</span></span>
<span data-ttu-id="cee74-122">Ценовая Категория.</span><span class="sxs-lookup"><span data-stu-id="cee74-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="cee74-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cee74-123">-Confirm</span></span>
<span data-ttu-id="cee74-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cee74-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee74-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee74-125">-WhatIf</span></span>
<span data-ttu-id="cee74-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cee74-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cee74-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cee74-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee74-128">CommonParameters</span></span>
<span data-ttu-id="cee74-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cee74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee74-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee74-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee74-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cee74-131">INPUTS</span></span>

### <span data-ttu-id="cee74-132">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cee74-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="cee74-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cee74-133">OUTPUTS</span></span>

### <span data-ttu-id="cee74-134">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cee74-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="cee74-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="cee74-135">NOTES</span></span>

## <span data-ttu-id="cee74-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cee74-136">RELATED LINKS</span></span>
