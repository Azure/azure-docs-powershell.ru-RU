---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076972"
---
# <span data-ttu-id="c6c90-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c6c90-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="c6c90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6c90-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c90-103">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="c6c90-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c6c90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6c90-104">SYNTAX</span></span>

### <span data-ttu-id="c6c90-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6c90-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6c90-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c6c90-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="c6c90-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c90-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c6c90-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6c90-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c90-109">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="c6c90-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c6c90-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6c90-110">EXAMPLES</span></span>

### <span data-ttu-id="c6c90-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c6c90-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="c6c90-112">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="c6c90-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c6c90-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6c90-113">PARAMETERS</span></span>

### <span data-ttu-id="c6c90-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6c90-114">-Name</span></span>
<span data-ttu-id="c6c90-115">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="c6c90-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="c6c90-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c6c90-116">-OfferName</span></span>
<span data-ttu-id="c6c90-117">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="c6c90-117">Name of an offer.</span></span>

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

### <span data-ttu-id="c6c90-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c90-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6c90-119">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c6c90-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c6c90-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6c90-120">-ResourceId</span></span>
<span data-ttu-id="c6c90-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6c90-121">The resource id.</span></span>

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

### <span data-ttu-id="c6c90-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="c6c90-122">-Skip</span></span>
<span data-ttu-id="c6c90-123">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="c6c90-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c6c90-124">-Top</span><span class="sxs-lookup"><span data-stu-id="c6c90-124">-Top</span></span>
<span data-ttu-id="c6c90-125">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="c6c90-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c6c90-126">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="c6c90-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c6c90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c90-127">CommonParameters</span></span>
<span data-ttu-id="c6c90-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6c90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c90-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c90-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c90-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6c90-130">INPUTS</span></span>

## <span data-ttu-id="c6c90-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6c90-131">OUTPUTS</span></span>

### <span data-ttu-id="c6c90-132">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c6c90-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="c6c90-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6c90-133">NOTES</span></span>

## <span data-ttu-id="c6c90-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6c90-134">RELATED LINKS</span></span>

