---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075115"
---
# <span data-ttu-id="04821-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="04821-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="04821-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04821-102">SYNOPSIS</span></span>
<span data-ttu-id="04821-103">Удаление указанного делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="04821-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="04821-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04821-104">SYNTAX</span></span>

### <span data-ttu-id="04821-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04821-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04821-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="04821-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04821-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04821-107">DESCRIPTION</span></span>
<span data-ttu-id="04821-108">Удаление указанного делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="04821-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="04821-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04821-109">EXAMPLES</span></span>

### <span data-ttu-id="04821-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="04821-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="04821-111">Удаление делегирования предложения</span><span class="sxs-lookup"><span data-stu-id="04821-111">Removes the offer delegation</span></span>

## <span data-ttu-id="04821-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04821-112">PARAMETERS</span></span>

### <span data-ttu-id="04821-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04821-113">-DefaultProfile</span></span>
<span data-ttu-id="04821-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04821-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04821-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04821-115">-InputObject</span></span>
<span data-ttu-id="04821-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="04821-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="04821-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04821-117">-Name</span></span>
<span data-ttu-id="04821-118">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="04821-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="04821-119">-OfferName</span><span class="sxs-lookup"><span data-stu-id="04821-119">-OfferName</span></span>
<span data-ttu-id="04821-120">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="04821-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="04821-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04821-121">-PassThru</span></span>
<span data-ttu-id="04821-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="04821-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="04821-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04821-123">-ResourceGroupName</span></span>
<span data-ttu-id="04821-124">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="04821-124">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="04821-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04821-125">-SubscriptionId</span></span>
<span data-ttu-id="04821-126">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="04821-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="04821-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04821-127">-Confirm</span></span>
<span data-ttu-id="04821-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04821-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04821-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04821-129">-WhatIf</span></span>
<span data-ttu-id="04821-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04821-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04821-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04821-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04821-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04821-132">CommonParameters</span></span>
<span data-ttu-id="04821-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04821-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04821-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04821-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04821-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04821-135">INPUTS</span></span>

### <span data-ttu-id="04821-136">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="04821-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="04821-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04821-137">OUTPUTS</span></span>

### <span data-ttu-id="04821-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04821-138">System.Boolean</span></span>

<span data-ttu-id="04821-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="04821-139">ALIASES</span></span>

## <span data-ttu-id="04821-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="04821-140">NOTES</span></span>

<span data-ttu-id="04821-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="04821-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04821-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="04821-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="04821-143">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="04821-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04821-144">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="04821-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="04821-145">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="04821-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="04821-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="04821-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04821-147">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="04821-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="04821-148">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="04821-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="04821-149">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="04821-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="04821-150">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="04821-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="04821-151">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="04821-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="04821-152">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="04821-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="04821-153">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="04821-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="04821-154">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="04821-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="04821-155">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="04821-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="04821-156">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="04821-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="04821-157">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="04821-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="04821-158">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="04821-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="04821-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04821-159">RELATED LINKS</span></span>

