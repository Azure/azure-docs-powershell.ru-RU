---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb583ca37f610d47c880fd2e15ae3e7b8182b5ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555276"
---
# <span data-ttu-id="b8502-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="b8502-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="b8502-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8502-102">SYNOPSIS</span></span>
<span data-ttu-id="b8502-103">Получение коллекции всех приобретенных планов, к которым у подписки есть доступ.</span><span class="sxs-lookup"><span data-stu-id="b8502-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="b8502-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8502-104">SYNTAX</span></span>

### <span data-ttu-id="b8502-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8502-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8502-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b8502-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="b8502-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8502-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b8502-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8502-108">DESCRIPTION</span></span>
<span data-ttu-id="b8502-109">Получение коллекции всех приобретенных планов, к которым у подписки есть доступ.</span><span class="sxs-lookup"><span data-stu-id="b8502-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="b8502-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8502-110">EXAMPLES</span></span>

### <span data-ttu-id="b8502-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b8502-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="b8502-112">Получение коллекции всех приобретенных планов, к которым у подписки есть доступ.</span><span class="sxs-lookup"><span data-stu-id="b8502-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="b8502-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8502-113">PARAMETERS</span></span>

### <span data-ttu-id="b8502-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="b8502-114">-AcquisitionId</span></span>
<span data-ttu-id="b8502-115">Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="b8502-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8502-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8502-116">-ResourceId</span></span>
<span data-ttu-id="b8502-117">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8502-117">The resource id.</span></span>

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

### <span data-ttu-id="b8502-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="b8502-118">-Skip</span></span>
<span data-ttu-id="b8502-119">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="b8502-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b8502-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8502-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="b8502-121">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b8502-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8502-122">-Top</span><span class="sxs-lookup"><span data-stu-id="b8502-122">-Top</span></span>
<span data-ttu-id="b8502-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="b8502-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b8502-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="b8502-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b8502-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8502-125">CommonParameters</span></span>
<span data-ttu-id="b8502-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8502-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8502-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8502-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8502-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8502-128">INPUTS</span></span>

## <span data-ttu-id="b8502-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8502-129">OUTPUTS</span></span>

### <span data-ttu-id="b8502-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="b8502-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="b8502-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8502-131">NOTES</span></span>

## <span data-ttu-id="b8502-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8502-132">RELATED LINKS</span></span>

