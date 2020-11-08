---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077080"
---
# <span data-ttu-id="da8ee-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="da8ee-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="da8ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="da8ee-103">Удаляет приобретенный план.</span><span class="sxs-lookup"><span data-stu-id="da8ee-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="da8ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da8ee-104">SYNTAX</span></span>

### <span data-ttu-id="da8ee-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da8ee-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da8ee-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da8ee-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da8ee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da8ee-107">DESCRIPTION</span></span>
<span data-ttu-id="da8ee-108">Удаляет приобретенный план.</span><span class="sxs-lookup"><span data-stu-id="da8ee-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="da8ee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da8ee-109">EXAMPLES</span></span>

### <span data-ttu-id="da8ee-110">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="da8ee-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="da8ee-111">Удаление приобретенного плана.</span><span class="sxs-lookup"><span data-stu-id="da8ee-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="da8ee-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da8ee-112">PARAMETERS</span></span>

### <span data-ttu-id="da8ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8ee-113">-DefaultProfile</span></span>
<span data-ttu-id="da8ee-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da8ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da8ee-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da8ee-115">-InputObject</span></span>
<span data-ttu-id="da8ee-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="da8ee-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="da8ee-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da8ee-117">-PassThru</span></span>
<span data-ttu-id="da8ee-118">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="da8ee-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="da8ee-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="da8ee-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="da8ee-120">Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="da8ee-120">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="da8ee-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da8ee-121">-SubscriptionId</span></span>
<span data-ttu-id="da8ee-122">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="da8ee-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="da8ee-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da8ee-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="da8ee-124">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="da8ee-124">The target subscription ID.</span></span>

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

### <span data-ttu-id="da8ee-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da8ee-125">-Confirm</span></span>
<span data-ttu-id="da8ee-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da8ee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da8ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da8ee-127">-WhatIf</span></span>
<span data-ttu-id="da8ee-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da8ee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da8ee-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da8ee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da8ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8ee-130">CommonParameters</span></span>
<span data-ttu-id="da8ee-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da8ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8ee-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da8ee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8ee-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da8ee-133">INPUTS</span></span>

### <span data-ttu-id="da8ee-134">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="da8ee-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="da8ee-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da8ee-135">OUTPUTS</span></span>

### <span data-ttu-id="da8ee-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da8ee-136">System.Boolean</span></span>

<span data-ttu-id="da8ee-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="da8ee-137">ALIASES</span></span>

### <span data-ttu-id="da8ee-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="da8ee-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="da8ee-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="da8ee-139">NOTES</span></span>

<span data-ttu-id="da8ee-140">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="da8ee-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da8ee-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da8ee-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="da8ee-142">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="da8ee-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da8ee-143">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="da8ee-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="da8ee-144">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="da8ee-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="da8ee-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="da8ee-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da8ee-146">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="da8ee-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="da8ee-147">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="da8ee-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="da8ee-148">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="da8ee-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="da8ee-149">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="da8ee-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="da8ee-150">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="da8ee-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="da8ee-151">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="da8ee-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="da8ee-152">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="da8ee-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="da8ee-153">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="da8ee-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="da8ee-154">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="da8ee-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="da8ee-155">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="da8ee-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="da8ee-156">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="da8ee-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="da8ee-157">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="da8ee-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="da8ee-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da8ee-158">RELATED LINKS</span></span>

