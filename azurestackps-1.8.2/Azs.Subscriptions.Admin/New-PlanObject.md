---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077164"
---
# <span data-ttu-id="c0caa-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="c0caa-101">New-PlanObject</span></span>

## <span data-ttu-id="c0caa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0caa-102">SYNOPSIS</span></span>
<span data-ttu-id="c0caa-103">План представляет пакет квот и возможностей, которые предлагаются клиентам.</span><span class="sxs-lookup"><span data-stu-id="c0caa-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="c0caa-104">Клиент может получить этот план посредством предложения по обновлению доступа к основным облачным службам.</span><span class="sxs-lookup"><span data-stu-id="c0caa-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="c0caa-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0caa-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="c0caa-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0caa-106">DESCRIPTION</span></span>
<span data-ttu-id="c0caa-107">План представляет пакет квот и возможностей, которые предлагаются клиентам.</span><span class="sxs-lookup"><span data-stu-id="c0caa-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="c0caa-108">Клиент может получить этот план посредством предложения по обновлению доступа к основным облачным службам.</span><span class="sxs-lookup"><span data-stu-id="c0caa-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="c0caa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0caa-109">EXAMPLES</span></span>

### <span data-ttu-id="c0caa-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0caa-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c0caa-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="c0caa-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="c0caa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0caa-112">PARAMETERS</span></span>

### <span data-ttu-id="c0caa-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="c0caa-113">-Description</span></span>
<span data-ttu-id="c0caa-114">Описание плана.</span><span class="sxs-lookup"><span data-stu-id="c0caa-114">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c0caa-115">-DisplayName</span></span>
<span data-ttu-id="c0caa-116">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="c0caa-116">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c0caa-117">-ExternalReferenceId</span></span>
<span data-ttu-id="c0caa-118">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="c0caa-118">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-119">-ID</span><span class="sxs-lookup"><span data-stu-id="c0caa-119">-Id</span></span>
<span data-ttu-id="c0caa-120">URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="c0caa-120">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-121">-Location</span><span class="sxs-lookup"><span data-stu-id="c0caa-121">-Location</span></span>
<span data-ttu-id="c0caa-122">Расположение, в котором расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="c0caa-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0caa-123">-Name</span></span>
<span data-ttu-id="c0caa-124">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="c0caa-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="c0caa-125">-QuotaIds</span></span>
<span data-ttu-id="c0caa-126">Идентификаторы квот в плане.</span><span class="sxs-lookup"><span data-stu-id="c0caa-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="c0caa-127">-SkuIds</span></span>
<span data-ttu-id="c0caa-128">Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="c0caa-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="c0caa-129">-SubscriptionCount</span></span>
<span data-ttu-id="c0caa-130">Число подписок.</span><span class="sxs-lookup"><span data-stu-id="c0caa-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-131">-Теги</span><span class="sxs-lookup"><span data-stu-id="c0caa-131">-Tags</span></span>
<span data-ttu-id="c0caa-132">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="c0caa-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-133">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="c0caa-133">-Type</span></span>
<span data-ttu-id="c0caa-134">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="c0caa-134">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0caa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0caa-135">CommonParameters</span></span>
<span data-ttu-id="c0caa-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0caa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0caa-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0caa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0caa-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0caa-138">INPUTS</span></span>

## <span data-ttu-id="c0caa-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0caa-139">OUTPUTS</span></span>

## <span data-ttu-id="c0caa-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0caa-140">NOTES</span></span>

## <span data-ttu-id="c0caa-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0caa-141">RELATED LINKS</span></span>

