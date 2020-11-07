---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908689"
---
# <span data-ttu-id="a8a51-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="a8a51-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="a8a51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8a51-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a51-103">Список поддерживаемых операций.</span><span class="sxs-lookup"><span data-stu-id="a8a51-103">List of supported operations.</span></span>

## <span data-ttu-id="a8a51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8a51-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a8a51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8a51-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a51-106">Список поддерживаемых операций.</span><span class="sxs-lookup"><span data-stu-id="a8a51-106">List of supported operations.</span></span>

## <span data-ttu-id="a8a51-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8a51-107">EXAMPLES</span></span>

### <span data-ttu-id="a8a51-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8a51-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a8a51-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="a8a51-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="a8a51-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8a51-110">PARAMETERS</span></span>

### <span data-ttu-id="a8a51-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8a51-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="a8a51-112">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="a8a51-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="a8a51-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8a51-113">-DisplayName</span></span>
<span data-ttu-id="a8a51-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="a8a51-114">Subscription name.</span></span>

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

### <span data-ttu-id="a8a51-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="a8a51-115">-ExternalReferenceId</span></span>
<span data-ttu-id="a8a51-116">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="a8a51-116">External reference identifier.</span></span>

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

### <span data-ttu-id="a8a51-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a8a51-117">-Id</span></span>
<span data-ttu-id="a8a51-118">Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a8a51-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="a8a51-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a8a51-119">-Name</span></span>
<span data-ttu-id="a8a51-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a8a51-120">Name of the resource.</span></span>

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

### <span data-ttu-id="a8a51-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="a8a51-121">-OfferId</span></span>
<span data-ttu-id="a8a51-122">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="a8a51-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="a8a51-123">-Владелец</span><span class="sxs-lookup"><span data-stu-id="a8a51-123">-Owner</span></span>
<span data-ttu-id="a8a51-124">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="a8a51-124">Subscription owner.</span></span>

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

### <span data-ttu-id="a8a51-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="a8a51-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="a8a51-126">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="a8a51-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="a8a51-127">-State</span><span class="sxs-lookup"><span data-stu-id="a8a51-127">-State</span></span>
<span data-ttu-id="a8a51-128">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="a8a51-128">Subscription state.</span></span>

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

### <span data-ttu-id="a8a51-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8a51-129">-SubscriptionId</span></span>
<span data-ttu-id="a8a51-130">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="a8a51-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="a8a51-131">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a8a51-131">-TenantId</span></span>
<span data-ttu-id="a8a51-132">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="a8a51-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="a8a51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a51-133">CommonParameters</span></span>
<span data-ttu-id="a8a51-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8a51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a51-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a51-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a51-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8a51-136">INPUTS</span></span>

## <span data-ttu-id="a8a51-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8a51-137">OUTPUTS</span></span>

## <span data-ttu-id="a8a51-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8a51-138">NOTES</span></span>

## <span data-ttu-id="a8a51-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8a51-139">RELATED LINKS</span></span>

