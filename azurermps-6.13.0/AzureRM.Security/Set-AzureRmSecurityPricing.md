---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564004"
---
# <span data-ttu-id="855d0-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="855d0-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="855d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="855d0-102">SYNOPSIS</span></span>
<span data-ttu-id="855d0-103">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="855d0-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="855d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="855d0-104">SYNTAX</span></span>

### <span data-ttu-id="855d0-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="855d0-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855d0-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="855d0-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855d0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="855d0-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="855d0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="855d0-108">DESCRIPTION</span></span>
<span data-ttu-id="855d0-109">Задает цены уровня центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="855d0-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="855d0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="855d0-110">EXAMPLES</span></span>

### <span data-ttu-id="855d0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="855d0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="855d0-112">Настройка ценовой категории центра безопасности Azure по подписке "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="855d0-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="855d0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="855d0-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="855d0-114">Задает для центра безопасности "myService1" группы ресурсов Azure ценовую категорию "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="855d0-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="855d0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="855d0-115">PARAMETERS</span></span>

### <span data-ttu-id="855d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="855d0-116">-DefaultProfile</span></span>
<span data-ttu-id="855d0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="855d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="855d0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="855d0-118">-InputObject</span></span>
<span data-ttu-id="855d0-119">Объект input.</span><span class="sxs-lookup"><span data-stu-id="855d0-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="855d0-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="855d0-120">-Name</span></span>
<span data-ttu-id="855d0-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="855d0-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="855d0-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="855d0-122">-PricingTier</span></span>
<span data-ttu-id="855d0-123">Ценовая Категория.</span><span class="sxs-lookup"><span data-stu-id="855d0-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="855d0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="855d0-124">-ResourceGroupName</span></span>
<span data-ttu-id="855d0-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="855d0-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="855d0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="855d0-126">-Confirm</span></span>
<span data-ttu-id="855d0-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="855d0-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="855d0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="855d0-128">-WhatIf</span></span>
<span data-ttu-id="855d0-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="855d0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="855d0-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="855d0-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="855d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="855d0-131">CommonParameters</span></span>
<span data-ttu-id="855d0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="855d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="855d0-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="855d0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="855d0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="855d0-134">INPUTS</span></span>

### <span data-ttu-id="855d0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="855d0-135">System.String</span></span>
<span data-ttu-id="855d0-136">Microsoft. Azure. Commands. Security. командлеты. цены. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="855d0-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="855d0-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="855d0-137">OUTPUTS</span></span>

### <span data-ttu-id="855d0-138">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="855d0-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="855d0-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="855d0-139">NOTES</span></span>

## <span data-ttu-id="855d0-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="855d0-140">RELATED LINKS</span></span>
