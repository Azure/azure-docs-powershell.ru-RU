---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075175"
---
# <span data-ttu-id="c34da-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="c34da-101">New-AzsSubscription</span></span>

## <span data-ttu-id="c34da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c34da-102">SYNOPSIS</span></span>
<span data-ttu-id="c34da-103">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="c34da-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="c34da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c34da-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c34da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c34da-105">DESCRIPTION</span></span>
<span data-ttu-id="c34da-106">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="c34da-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="c34da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c34da-107">EXAMPLES</span></span>

### <span data-ttu-id="c34da-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c34da-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="c34da-109">Создайте подписку.</span><span class="sxs-lookup"><span data-stu-id="c34da-109">Create a subscription.</span></span>

## <span data-ttu-id="c34da-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c34da-110">PARAMETERS</span></span>

### <span data-ttu-id="c34da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34da-111">-DefaultProfile</span></span>
<span data-ttu-id="c34da-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c34da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c34da-113">-DisplayName</span></span>
<span data-ttu-id="c34da-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="c34da-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c34da-115">-Id</span></span>
<span data-ttu-id="c34da-116">Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c34da-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="c34da-117">-OfferId</span></span>
<span data-ttu-id="c34da-118">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="c34da-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-119">-State</span><span class="sxs-lookup"><span data-stu-id="c34da-119">-State</span></span>
<span data-ttu-id="c34da-120">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="c34da-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c34da-121">-SubscriptionId</span></span>
<span data-ttu-id="c34da-122">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c34da-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-123">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c34da-123">-TenantId</span></span>
<span data-ttu-id="c34da-124">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="c34da-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c34da-125">-Confirm</span></span>
<span data-ttu-id="c34da-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c34da-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c34da-127">-WhatIf</span></span>
<span data-ttu-id="c34da-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c34da-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c34da-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c34da-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c34da-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34da-130">CommonParameters</span></span>
<span data-ttu-id="c34da-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c34da-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34da-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c34da-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34da-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c34da-133">INPUTS</span></span>

## <span data-ttu-id="c34da-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c34da-134">OUTPUTS</span></span>

### <span data-ttu-id="c34da-135">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="c34da-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="c34da-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c34da-136">NOTES</span></span>

## <span data-ttu-id="c34da-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c34da-137">RELATED LINKS</span></span>

