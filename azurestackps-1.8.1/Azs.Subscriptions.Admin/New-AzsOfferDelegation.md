---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908754"
---
# <span data-ttu-id="b5252-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="b5252-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="b5252-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5252-102">SYNOPSIS</span></span>
<span data-ttu-id="b5252-103">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="b5252-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="b5252-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5252-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5252-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5252-105">DESCRIPTION</span></span>
<span data-ttu-id="b5252-106">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="b5252-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="b5252-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5252-107">EXAMPLES</span></span>

### <span data-ttu-id="b5252-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b5252-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="b5252-109">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="b5252-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="b5252-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5252-110">PARAMETERS</span></span>

### <span data-ttu-id="b5252-111">-Location</span><span class="sxs-lookup"><span data-stu-id="b5252-111">-Location</span></span>
<span data-ttu-id="b5252-112">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b5252-112">Location of the resource.</span></span>

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

### <span data-ttu-id="b5252-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5252-113">-Name</span></span>
<span data-ttu-id="b5252-114">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="b5252-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="b5252-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="b5252-115">-OfferName</span></span>
<span data-ttu-id="b5252-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="b5252-116">Name of an offer.</span></span>

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

### <span data-ttu-id="b5252-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5252-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5252-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="b5252-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="b5252-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5252-119">-SubscriptionId</span></span>
<span data-ttu-id="b5252-120">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="b5252-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="b5252-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5252-121">-Confirm</span></span>
<span data-ttu-id="b5252-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5252-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5252-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5252-123">-WhatIf</span></span>
<span data-ttu-id="b5252-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5252-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5252-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5252-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5252-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5252-126">CommonParameters</span></span>
<span data-ttu-id="b5252-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5252-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5252-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5252-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5252-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5252-129">INPUTS</span></span>

## <span data-ttu-id="b5252-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5252-130">OUTPUTS</span></span>

### <span data-ttu-id="b5252-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="b5252-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="b5252-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5252-132">NOTES</span></span>

## <span data-ttu-id="b5252-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5252-133">RELATED LINKS</span></span>

