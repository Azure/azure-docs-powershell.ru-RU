---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908453"
---
# <span data-ttu-id="c52fa-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c52fa-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="c52fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c52fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c52fa-103">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="c52fa-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c52fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c52fa-104">SYNTAX</span></span>

### <span data-ttu-id="c52fa-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c52fa-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c52fa-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c52fa-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="c52fa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c52fa-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c52fa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52fa-108">DESCRIPTION</span></span>
<span data-ttu-id="c52fa-109">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="c52fa-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c52fa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c52fa-110">EXAMPLES</span></span>

### <span data-ttu-id="c52fa-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c52fa-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="c52fa-112">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="c52fa-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c52fa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c52fa-113">PARAMETERS</span></span>

### <span data-ttu-id="c52fa-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c52fa-114">-Name</span></span>
<span data-ttu-id="c52fa-115">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="c52fa-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="c52fa-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c52fa-116">-OfferName</span></span>
<span data-ttu-id="c52fa-117">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="c52fa-117">Name of an offer.</span></span>

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

### <span data-ttu-id="c52fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c52fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="c52fa-119">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c52fa-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c52fa-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c52fa-120">-ResourceId</span></span>
<span data-ttu-id="c52fa-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c52fa-121">The resource id.</span></span>

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

### <span data-ttu-id="c52fa-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="c52fa-122">-Skip</span></span>
<span data-ttu-id="c52fa-123">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="c52fa-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c52fa-124">-Top</span><span class="sxs-lookup"><span data-stu-id="c52fa-124">-Top</span></span>
<span data-ttu-id="c52fa-125">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="c52fa-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c52fa-126">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="c52fa-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c52fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52fa-127">CommonParameters</span></span>
<span data-ttu-id="c52fa-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c52fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52fa-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52fa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52fa-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c52fa-130">INPUTS</span></span>

## <span data-ttu-id="c52fa-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c52fa-131">OUTPUTS</span></span>

### <span data-ttu-id="c52fa-132">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c52fa-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="c52fa-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c52fa-133">NOTES</span></span>

## <span data-ttu-id="c52fa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c52fa-134">RELATED LINKS</span></span>

