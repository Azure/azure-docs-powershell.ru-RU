---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908414"
---
# <span data-ttu-id="82a26-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="82a26-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="82a26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82a26-102">SYNOPSIS</span></span>
<span data-ttu-id="82a26-103">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="82a26-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="82a26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82a26-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82a26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82a26-105">DESCRIPTION</span></span>
<span data-ttu-id="82a26-106">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="82a26-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="82a26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82a26-107">EXAMPLES</span></span>

### <span data-ttu-id="82a26-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="82a26-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="82a26-109">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="82a26-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="82a26-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82a26-110">PARAMETERS</span></span>

### <span data-ttu-id="82a26-111">-Location</span><span class="sxs-lookup"><span data-stu-id="82a26-111">-Location</span></span>
<span data-ttu-id="82a26-112">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="82a26-112">Location of the resource.</span></span>

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

### <span data-ttu-id="82a26-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82a26-113">-Name</span></span>
<span data-ttu-id="82a26-114">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="82a26-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="82a26-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="82a26-115">-OfferName</span></span>
<span data-ttu-id="82a26-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="82a26-116">Name of an offer.</span></span>

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

### <span data-ttu-id="82a26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a26-117">-ResourceGroupName</span></span>
<span data-ttu-id="82a26-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="82a26-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="82a26-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82a26-119">-SubscriptionId</span></span>
<span data-ttu-id="82a26-120">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="82a26-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="82a26-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82a26-121">-Confirm</span></span>
<span data-ttu-id="82a26-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82a26-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82a26-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a26-123">-WhatIf</span></span>
<span data-ttu-id="82a26-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82a26-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a26-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82a26-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82a26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a26-126">CommonParameters</span></span>
<span data-ttu-id="82a26-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82a26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a26-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a26-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a26-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82a26-129">INPUTS</span></span>

## <span data-ttu-id="82a26-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82a26-130">OUTPUTS</span></span>

### <span data-ttu-id="82a26-131">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="82a26-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="82a26-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="82a26-132">NOTES</span></span>

## <span data-ttu-id="82a26-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82a26-133">RELATED LINKS</span></span>

