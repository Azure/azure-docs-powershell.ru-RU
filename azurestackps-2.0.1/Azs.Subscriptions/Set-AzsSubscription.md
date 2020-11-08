---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075250"
---
# <span data-ttu-id="3e93d-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="3e93d-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="3e93d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e93d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e93d-103">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="3e93d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e93d-104">SYNTAX</span></span>

### <span data-ttu-id="3e93d-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e93d-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3e93d-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="3e93d-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3e93d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e93d-107">DESCRIPTION</span></span>
<span data-ttu-id="3e93d-108">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="3e93d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e93d-109">EXAMPLES</span></span>

### <span data-ttu-id="3e93d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e93d-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="3e93d-111">Обновляет подписку.</span><span class="sxs-lookup"><span data-stu-id="3e93d-111">Updates a subscription.</span></span>

## <span data-ttu-id="3e93d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e93d-112">PARAMETERS</span></span>

### <span data-ttu-id="3e93d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e93d-113">-DefaultProfile</span></span>
<span data-ttu-id="3e93d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e93d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e93d-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3e93d-115">-DisplayName</span></span>
<span data-ttu-id="3e93d-116">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e93d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="3e93d-117">-Id</span></span>
<span data-ttu-id="3e93d-118">Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3e93d-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e93d-119">-OfferId</span><span class="sxs-lookup"><span data-stu-id="3e93d-119">-OfferId</span></span>
<span data-ttu-id="3e93d-120">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="3e93d-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e93d-121">-State</span><span class="sxs-lookup"><span data-stu-id="3e93d-121">-State</span></span>
<span data-ttu-id="3e93d-122">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e93d-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="3e93d-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="3e93d-124">Список поддерживаемых операций.</span><span class="sxs-lookup"><span data-stu-id="3e93d-124">List of supported operations.</span></span>
<span data-ttu-id="3e93d-125">Для конструирования ознакомьтесь с разделом "Заметки" для свойств SUBSCRIPTIONDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3e93d-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3e93d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e93d-126">-SubscriptionId</span></span>
<span data-ttu-id="3e93d-127">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e93d-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="3e93d-128">-TenantId</span></span>
<span data-ttu-id="3e93d-129">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="3e93d-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e93d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e93d-130">-Confirm</span></span>
<span data-ttu-id="3e93d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e93d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e93d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e93d-132">-WhatIf</span></span>
<span data-ttu-id="3e93d-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e93d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e93d-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e93d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e93d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e93d-135">CommonParameters</span></span>
<span data-ttu-id="3e93d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e93d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e93d-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e93d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e93d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e93d-138">INPUTS</span></span>

### <span data-ttu-id="3e93d-139">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="3e93d-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="3e93d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e93d-140">OUTPUTS</span></span>

### <span data-ttu-id="3e93d-141">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="3e93d-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="3e93d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e93d-142">NOTES</span></span>

<span data-ttu-id="3e93d-143">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e93d-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e93d-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e93d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e93d-145">SUBSCRIPTIONDEFINITION <ISubscription> : список поддерживаемых операций.</span><span class="sxs-lookup"><span data-stu-id="3e93d-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="3e93d-146">`[DisplayName <String>]`: Имя подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="3e93d-147">`[Id <String>]`: Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3e93d-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="3e93d-148">`[OfferId <String>]`: Идентификатор предложения в рамках области поставщика с делегированными полномочиями.</span><span class="sxs-lookup"><span data-stu-id="3e93d-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="3e93d-149">`[State <SubscriptionState?>]`: Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="3e93d-150">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="3e93d-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="3e93d-151">`[TenantId <String>]`: Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="3e93d-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="3e93d-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e93d-152">RELATED LINKS</span></span>

