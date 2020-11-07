---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907893"
---
# <span data-ttu-id="0f18a-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="0f18a-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="0f18a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f18a-102">SYNOPSIS</span></span>
<span data-ttu-id="0f18a-103">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="0f18a-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="0f18a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f18a-104">SYNTAX</span></span>

### <span data-ttu-id="0f18a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f18a-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f18a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0f18a-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="0f18a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f18a-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0f18a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f18a-108">DESCRIPTION</span></span>
<span data-ttu-id="0f18a-109">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="0f18a-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="0f18a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f18a-110">EXAMPLES</span></span>

### <span data-ttu-id="0f18a-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f18a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="0f18a-112">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="0f18a-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="0f18a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f18a-113">PARAMETERS</span></span>

### <span data-ttu-id="0f18a-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f18a-114">-Name</span></span>
<span data-ttu-id="0f18a-115">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="0f18a-115">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f18a-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="0f18a-116">-OfferName</span></span>
<span data-ttu-id="0f18a-117">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="0f18a-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f18a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f18a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f18a-119">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="0f18a-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f18a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f18a-120">-ResourceId</span></span>
<span data-ttu-id="0f18a-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f18a-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f18a-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="0f18a-122">-Skip</span></span>
<span data-ttu-id="0f18a-123">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="0f18a-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f18a-124">-Top</span><span class="sxs-lookup"><span data-stu-id="0f18a-124">-Top</span></span>
<span data-ttu-id="0f18a-125">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="0f18a-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0f18a-126">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="0f18a-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f18a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f18a-127">CommonParameters</span></span>
<span data-ttu-id="0f18a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f18a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f18a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f18a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f18a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f18a-130">INPUTS</span></span>

## <span data-ttu-id="0f18a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f18a-131">OUTPUTS</span></span>

### <span data-ttu-id="0f18a-132">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="0f18a-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="0f18a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f18a-133">NOTES</span></span>

## <span data-ttu-id="0f18a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f18a-134">RELATED LINKS</span></span>

