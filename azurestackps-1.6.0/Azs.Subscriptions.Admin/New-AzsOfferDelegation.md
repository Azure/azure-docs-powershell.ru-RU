---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36a4ddec5825be1e1f897cb3a12e7bc26a2c6817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555444"
---
# <span data-ttu-id="e6615-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e6615-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="e6615-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6615-102">SYNOPSIS</span></span>
<span data-ttu-id="e6615-103">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="e6615-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="e6615-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6615-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6615-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6615-105">DESCRIPTION</span></span>
<span data-ttu-id="e6615-106">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="e6615-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="e6615-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6615-107">EXAMPLES</span></span>

### <span data-ttu-id="e6615-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6615-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e6615-109">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="e6615-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="e6615-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6615-110">PARAMETERS</span></span>

### <span data-ttu-id="e6615-111">-Location</span><span class="sxs-lookup"><span data-stu-id="e6615-111">-Location</span></span>
<span data-ttu-id="e6615-112">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6615-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6615-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6615-113">-Name</span></span>
<span data-ttu-id="e6615-114">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="e6615-114">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6615-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="e6615-115">-OfferName</span></span>
<span data-ttu-id="e6615-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="e6615-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6615-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6615-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6615-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="e6615-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6615-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6615-119">-SubscriptionId</span></span>
<span data-ttu-id="e6615-120">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="e6615-120">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6615-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6615-121">-Confirm</span></span>
<span data-ttu-id="e6615-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6615-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6615-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6615-123">-WhatIf</span></span>
<span data-ttu-id="e6615-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6615-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6615-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6615-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6615-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6615-126">CommonParameters</span></span>
<span data-ttu-id="e6615-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6615-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6615-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6615-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6615-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6615-129">INPUTS</span></span>

## <span data-ttu-id="e6615-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6615-130">OUTPUTS</span></span>

### <span data-ttu-id="e6615-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e6615-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="e6615-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6615-132">NOTES</span></span>

## <span data-ttu-id="e6615-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6615-133">RELATED LINKS</span></span>

