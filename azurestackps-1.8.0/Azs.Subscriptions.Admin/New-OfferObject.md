---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908062"
---
# <span data-ttu-id="f2d09-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="f2d09-101">New-OfferObject</span></span>

## <span data-ttu-id="f2d09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2d09-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d09-103">Представляет предложение служб, для которых можно создать подписку.</span><span class="sxs-lookup"><span data-stu-id="f2d09-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="f2d09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2d09-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="f2d09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2d09-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d09-106">Представляет предложение служб, для которых можно создать подписку.</span><span class="sxs-lookup"><span data-stu-id="f2d09-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="f2d09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2d09-107">EXAMPLES</span></span>

### <span data-ttu-id="f2d09-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2d09-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f2d09-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="f2d09-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f2d09-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2d09-110">PARAMETERS</span></span>

### <span data-ttu-id="f2d09-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="f2d09-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="f2d09-112">Ссылки на планы надстроек, с помощью которых клиент может дополнительно получить как часть предложения.</span><span class="sxs-lookup"><span data-stu-id="f2d09-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="f2d09-113">-BasePlanIds</span></span>
<span data-ttu-id="f2d09-114">Идентификаторы базовых планов, которые будут доступны клиенту немедленно, когда клиент подписывается на предложение.</span><span class="sxs-lookup"><span data-stu-id="f2d09-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="f2d09-115">-Description</span></span>
<span data-ttu-id="f2d09-116">Описание предложения.</span><span class="sxs-lookup"><span data-stu-id="f2d09-116">Description of offer.</span></span>

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

### <span data-ttu-id="f2d09-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2d09-117">-DisplayName</span></span>
<span data-ttu-id="f2d09-118">Отображаемое имя предложения.</span><span class="sxs-lookup"><span data-stu-id="f2d09-118">Display name of offer.</span></span>

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

### <span data-ttu-id="f2d09-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f2d09-119">-ExternalReferenceId</span></span>
<span data-ttu-id="f2d09-120">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="f2d09-120">External reference identifier.</span></span>

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

### <span data-ttu-id="f2d09-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f2d09-121">-Id</span></span>
<span data-ttu-id="f2d09-122">URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2d09-122">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f2d09-123">-Location</span></span>
<span data-ttu-id="f2d09-124">Расположение, в котором расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="f2d09-124">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="f2d09-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="f2d09-126">Максимальное количество подписок на одну учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f2d09-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2d09-127">-Name</span></span>
<span data-ttu-id="f2d09-128">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2d09-128">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-129">-State</span><span class="sxs-lookup"><span data-stu-id="f2d09-129">-State</span></span>
<span data-ttu-id="f2d09-130">Предоставление поддержки специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="f2d09-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="f2d09-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="f2d09-131">-SubscriptionCount</span></span>
<span data-ttu-id="f2d09-132">Текущее число подписок.</span><span class="sxs-lookup"><span data-stu-id="f2d09-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-133">-Теги</span><span class="sxs-lookup"><span data-stu-id="f2d09-133">-Tags</span></span>
<span data-ttu-id="f2d09-134">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="f2d09-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2d09-135">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f2d09-135">-Type</span></span>
<span data-ttu-id="f2d09-136">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="f2d09-136">Type of resource.</span></span>

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

### <span data-ttu-id="f2d09-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d09-137">CommonParameters</span></span>
<span data-ttu-id="f2d09-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2d09-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d09-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d09-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d09-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2d09-140">INPUTS</span></span>

## <span data-ttu-id="f2d09-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2d09-141">OUTPUTS</span></span>

## <span data-ttu-id="f2d09-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2d09-142">NOTES</span></span>

## <span data-ttu-id="f2d09-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2d09-143">RELATED LINKS</span></span>

