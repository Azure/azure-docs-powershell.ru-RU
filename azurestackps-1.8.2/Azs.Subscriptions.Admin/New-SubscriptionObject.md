---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077163"
---
# <span data-ttu-id="7b810-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="7b810-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="7b810-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b810-102">SYNOPSIS</span></span>
<span data-ttu-id="7b810-103">Список поддерживаемых операций.</span><span class="sxs-lookup"><span data-stu-id="7b810-103">List of supported operations.</span></span>

## <span data-ttu-id="7b810-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b810-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7b810-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b810-105">DESCRIPTION</span></span>
<span data-ttu-id="7b810-106">Список поддерживаемых операций.</span><span class="sxs-lookup"><span data-stu-id="7b810-106">List of supported operations.</span></span>

## <span data-ttu-id="7b810-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b810-107">EXAMPLES</span></span>

### <span data-ttu-id="7b810-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b810-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7b810-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="7b810-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7b810-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b810-110">PARAMETERS</span></span>

### <span data-ttu-id="7b810-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b810-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="7b810-112">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="7b810-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="7b810-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7b810-113">-DisplayName</span></span>
<span data-ttu-id="7b810-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="7b810-114">Subscription name.</span></span>

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

### <span data-ttu-id="7b810-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="7b810-115">-ExternalReferenceId</span></span>
<span data-ttu-id="7b810-116">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="7b810-116">External reference identifier.</span></span>

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

### <span data-ttu-id="7b810-117">-ID</span><span class="sxs-lookup"><span data-stu-id="7b810-117">-Id</span></span>
<span data-ttu-id="7b810-118">Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7b810-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="7b810-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b810-119">-Name</span></span>
<span data-ttu-id="7b810-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="7b810-120">Name of the resource.</span></span>

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

### <span data-ttu-id="7b810-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="7b810-121">-OfferId</span></span>
<span data-ttu-id="7b810-122">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="7b810-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="7b810-123">-Владелец</span><span class="sxs-lookup"><span data-stu-id="7b810-123">-Owner</span></span>
<span data-ttu-id="7b810-124">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="7b810-124">Subscription owner.</span></span>

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

### <span data-ttu-id="7b810-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="7b810-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="7b810-126">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="7b810-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="7b810-127">-State</span><span class="sxs-lookup"><span data-stu-id="7b810-127">-State</span></span>
<span data-ttu-id="7b810-128">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="7b810-128">Subscription state.</span></span>

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

### <span data-ttu-id="7b810-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b810-129">-SubscriptionId</span></span>
<span data-ttu-id="7b810-130">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="7b810-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="7b810-131">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7b810-131">-TenantId</span></span>
<span data-ttu-id="7b810-132">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="7b810-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="7b810-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b810-133">CommonParameters</span></span>
<span data-ttu-id="7b810-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b810-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b810-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b810-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b810-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b810-136">INPUTS</span></span>

## <span data-ttu-id="7b810-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b810-137">OUTPUTS</span></span>

## <span data-ttu-id="7b810-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b810-138">NOTES</span></span>

## <span data-ttu-id="7b810-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b810-139">RELATED LINKS</span></span>

