---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e0c752c3ffd266a3615fdd5a1f5193e0202b29a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555484"
---
# <span data-ttu-id="42d96-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="42d96-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="42d96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42d96-102">SYNOPSIS</span></span>
<span data-ttu-id="42d96-103">Обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="42d96-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="42d96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42d96-104">SYNTAX</span></span>

### <span data-ttu-id="42d96-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42d96-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d96-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="42d96-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d96-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42d96-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d96-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42d96-108">DESCRIPTION</span></span>
<span data-ttu-id="42d96-109">Обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="42d96-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="42d96-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42d96-110">EXAMPLES</span></span>

### <span data-ttu-id="42d96-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="42d96-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="42d96-112">Обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="42d96-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="42d96-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42d96-113">PARAMETERS</span></span>

### <span data-ttu-id="42d96-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42d96-114">-InputObject</span></span>
<span data-ttu-id="42d96-115">Входной объект типа Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="42d96-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

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

### <span data-ttu-id="42d96-116">-Location</span><span class="sxs-lookup"><span data-stu-id="42d96-116">-Location</span></span>
<span data-ttu-id="42d96-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="42d96-117">Location of the resource.</span></span>

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

### <span data-ttu-id="42d96-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42d96-118">-Name</span></span>
<span data-ttu-id="42d96-119">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="42d96-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="42d96-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="42d96-120">-OfferName</span></span>
<span data-ttu-id="42d96-121">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="42d96-121">Name of an offer.</span></span>

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

### <span data-ttu-id="42d96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d96-122">-ResourceGroupName</span></span>
<span data-ttu-id="42d96-123">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="42d96-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="42d96-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42d96-124">-ResourceId</span></span>
<span data-ttu-id="42d96-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="42d96-125">The resource id.</span></span>

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

### <span data-ttu-id="42d96-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42d96-126">-SubscriptionId</span></span>
<span data-ttu-id="42d96-127">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="42d96-127">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="42d96-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42d96-128">-Confirm</span></span>
<span data-ttu-id="42d96-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42d96-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d96-130">-WhatIf</span></span>
<span data-ttu-id="42d96-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42d96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d96-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42d96-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d96-133">CommonParameters</span></span>
<span data-ttu-id="42d96-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42d96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d96-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d96-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d96-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42d96-136">INPUTS</span></span>

## <span data-ttu-id="42d96-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42d96-137">OUTPUTS</span></span>

### <span data-ttu-id="42d96-138">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="42d96-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="42d96-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="42d96-139">NOTES</span></span>

## <span data-ttu-id="42d96-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42d96-140">RELATED LINKS</span></span>

