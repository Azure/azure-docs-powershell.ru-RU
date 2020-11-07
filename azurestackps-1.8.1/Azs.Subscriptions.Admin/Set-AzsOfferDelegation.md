---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908638"
---
# <span data-ttu-id="45bf4-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="45bf4-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="45bf4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="45bf4-103">Обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="45bf4-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="45bf4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45bf4-104">SYNTAX</span></span>

### <span data-ttu-id="45bf4-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45bf4-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45bf4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="45bf4-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45bf4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="45bf4-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45bf4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45bf4-108">DESCRIPTION</span></span>
<span data-ttu-id="45bf4-109">Обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="45bf4-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="45bf4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45bf4-110">EXAMPLES</span></span>

### <span data-ttu-id="45bf4-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45bf4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="45bf4-112">Обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="45bf4-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="45bf4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45bf4-113">PARAMETERS</span></span>

### <span data-ttu-id="45bf4-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45bf4-114">-InputObject</span></span>
<span data-ttu-id="45bf4-115">Входной объект типа Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="45bf4-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45bf4-116">-Location</span><span class="sxs-lookup"><span data-stu-id="45bf4-116">-Location</span></span>
<span data-ttu-id="45bf4-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="45bf4-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45bf4-118">-Name</span></span>
<span data-ttu-id="45bf4-119">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="45bf4-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf4-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="45bf4-120">-OfferName</span></span>
<span data-ttu-id="45bf4-121">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="45bf4-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bf4-122">-ResourceGroupName</span></span>
<span data-ttu-id="45bf4-123">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="45bf4-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45bf4-124">-ResourceId</span></span>
<span data-ttu-id="45bf4-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="45bf4-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45bf4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45bf4-126">-SubscriptionId</span></span>
<span data-ttu-id="45bf4-127">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="45bf4-127">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bf4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45bf4-128">-Confirm</span></span>
<span data-ttu-id="45bf4-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45bf4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45bf4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45bf4-130">-WhatIf</span></span>
<span data-ttu-id="45bf4-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45bf4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45bf4-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45bf4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45bf4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bf4-133">CommonParameters</span></span>
<span data-ttu-id="45bf4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45bf4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bf4-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45bf4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bf4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45bf4-136">INPUTS</span></span>

## <span data-ttu-id="45bf4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45bf4-137">OUTPUTS</span></span>

### <span data-ttu-id="45bf4-138">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="45bf4-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="45bf4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="45bf4-139">NOTES</span></span>

## <span data-ttu-id="45bf4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45bf4-140">RELATED LINKS</span></span>

