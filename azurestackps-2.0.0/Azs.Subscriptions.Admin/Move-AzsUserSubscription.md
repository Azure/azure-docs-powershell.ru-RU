---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/move-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 51ad63ef1531e7494b3929b8508e88e988155081
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075147"
---
# <span data-ttu-id="1f0f6-101">Move-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="1f0f6-101">Move-AzsUserSubscription</span></span>

## <span data-ttu-id="1f0f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0f6-103">Перемещение подписок между предлагаемыми поставщиками делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="1f0f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f0f6-104">SYNTAX</span></span>

### <span data-ttu-id="1f0f6-105">MoveExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f0f6-105">MoveExpanded (Default)</span></span>
```
Move-AzsUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f0f6-106">Перемещение</span><span class="sxs-lookup"><span data-stu-id="1f0f6-106">Move</span></span>
```
Move-AzsUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1f0f6-107">MoveViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f0f6-107">MoveViaIdentity</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f0f6-108">MoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1f0f6-108">MoveViaIdentityExpanded</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f0f6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f0f6-109">DESCRIPTION</span></span>
<span data-ttu-id="1f0f6-110">Перемещение подписок между предлагаемыми поставщиками делегированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-110">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="1f0f6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f0f6-111">EXAMPLES</span></span>

### <span data-ttu-id="1f0f6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f0f6-112">Example 1</span></span>
```powershell
PS C:\> Move-AzsSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

{{ Add output here }}
```

<span data-ttu-id="1f0f6-113">Перемещение подписок на пользователей в предложение делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-113">Move user subscriptions to a delegated provider offer.</span></span>

### <span data-ttu-id="1f0f6-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1f0f6-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id
Move-AzsSubscription -ResourceId $resourceIds

{{ Add output here }}
```

<span data-ttu-id="1f0f6-115">Перемещение подписок на пользователей из делегированного поставщика в поставщик по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-115">Move user subscriptions from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="1f0f6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f0f6-116">PARAMETERS</span></span>

### <span data-ttu-id="1f0f6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f0f6-117">-AsJob</span></span>
<span data-ttu-id="1f0f6-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1f0f6-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0f6-119">-DefaultProfile</span></span>
<span data-ttu-id="1f0f6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f0f6-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="1f0f6-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="1f0f6-122">Идентификатор предложения делегированного поставщика (из контекста администратора), на который будут перемещены подписки.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f0f6-123">-InputObject</span></span>
<span data-ttu-id="1f0f6-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: MoveViaIdentity, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="1f0f6-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="1f0f6-126">Определение действия "переместить подписку" для создания свойств MOVESUBSCRIPTIONSDEFINITION и создания хэш-таблицы см. раздел "Заметки".</span><span class="sxs-lookup"><span data-stu-id="1f0f6-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Move, MoveViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="1f0f6-127">-NoWait</span></span>
<span data-ttu-id="1f0f6-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="1f0f6-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f0f6-129">-PassThru</span></span>
<span data-ttu-id="1f0f6-130">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f0f6-131">-ResourceId</span></span>
<span data-ttu-id="1f0f6-132">Коллекция подписок для перехода к целевому поставщику предложения с делегированными поставщиками.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f0f6-133">-SubscriptionId</span></span>
<span data-ttu-id="1f0f6-134">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Move, MoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f0f6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f0f6-135">-Confirm</span></span>
<span data-ttu-id="1f0f6-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f0f6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f0f6-137">-WhatIf</span></span>
<span data-ttu-id="1f0f6-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f0f6-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f0f6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0f6-140">CommonParameters</span></span>
<span data-ttu-id="1f0f6-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0f6-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f0f6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0f6-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f0f6-143">INPUTS</span></span>

### <span data-ttu-id="1f0f6-144">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="1f0f6-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="1f0f6-145">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1f0f6-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="1f0f6-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f0f6-146">OUTPUTS</span></span>

### <span data-ttu-id="1f0f6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f0f6-147">System.Boolean</span></span>

<span data-ttu-id="1f0f6-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1f0f6-148">ALIASES</span></span>

## <span data-ttu-id="1f0f6-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f0f6-149">NOTES</span></span>

<span data-ttu-id="1f0f6-150">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f0f6-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1f0f6-152">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1f0f6-152">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f0f6-153">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-153">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="1f0f6-154">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-154">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="1f0f6-155">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1f0f6-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f0f6-156">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-156">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="1f0f6-157">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-157">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="1f0f6-158">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-158">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="1f0f6-159">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-159">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="1f0f6-160">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-160">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="1f0f6-161">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-161">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="1f0f6-162">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="1f0f6-162">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="1f0f6-163">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-163">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1f0f6-164">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-164">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="1f0f6-165">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-165">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1f0f6-166">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-166">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="1f0f6-167">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-167">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="1f0f6-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : определение действия перемещения подписки</span><span class="sxs-lookup"><span data-stu-id="1f0f6-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="1f0f6-169">`Resources <String[]>`: Коллекция подписок, которые нужно переместить в предложение целевого поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-169">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="1f0f6-170">`[TargetDelegatedProviderOffer <String>]`: Идентификатор предложения для делегированного поставщика (из контекста администратора), на который будут перемещены подписки.</span><span class="sxs-lookup"><span data-stu-id="1f0f6-170">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="1f0f6-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f0f6-171">RELATED LINKS</span></span>

