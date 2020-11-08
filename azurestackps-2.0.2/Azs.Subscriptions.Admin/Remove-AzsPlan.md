---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076928"
---
# <span data-ttu-id="e1521-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="e1521-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="e1521-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1521-102">SYNOPSIS</span></span>
<span data-ttu-id="e1521-103">Удаление указанного плана.</span><span class="sxs-lookup"><span data-stu-id="e1521-103">Delete the specified plan.</span></span>

## <span data-ttu-id="e1521-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1521-104">SYNTAX</span></span>

### <span data-ttu-id="e1521-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1521-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1521-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e1521-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e1521-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1521-107">DESCRIPTION</span></span>
<span data-ttu-id="e1521-108">Удаление указанного плана.</span><span class="sxs-lookup"><span data-stu-id="e1521-108">Delete the specified plan.</span></span>

## <span data-ttu-id="e1521-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1521-109">EXAMPLES</span></span>

### <span data-ttu-id="e1521-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1521-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

<span data-ttu-id="e1521-111">Удаление указанного плана</span><span class="sxs-lookup"><span data-stu-id="e1521-111">Delete the specified plan</span></span>

## <span data-ttu-id="e1521-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1521-112">PARAMETERS</span></span>

### <span data-ttu-id="e1521-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1521-113">-DefaultProfile</span></span>
<span data-ttu-id="e1521-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1521-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1521-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1521-115">-InputObject</span></span>
<span data-ttu-id="e1521-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e1521-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e1521-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1521-117">-Name</span></span>
<span data-ttu-id="e1521-118">Название плана.</span><span class="sxs-lookup"><span data-stu-id="e1521-118">Name of the plan.</span></span>

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

### <span data-ttu-id="e1521-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1521-119">-PassThru</span></span>
<span data-ttu-id="e1521-120">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e1521-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e1521-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1521-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1521-122">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="e1521-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e1521-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1521-123">-SubscriptionId</span></span>
<span data-ttu-id="e1521-124">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e1521-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e1521-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1521-125">-Confirm</span></span>
<span data-ttu-id="e1521-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1521-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1521-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1521-127">-WhatIf</span></span>
<span data-ttu-id="e1521-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1521-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1521-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1521-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1521-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1521-130">CommonParameters</span></span>
<span data-ttu-id="e1521-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1521-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1521-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1521-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1521-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1521-133">INPUTS</span></span>

### <span data-ttu-id="e1521-134">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e1521-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e1521-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1521-135">OUTPUTS</span></span>

### <span data-ttu-id="e1521-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1521-136">System.Boolean</span></span>

<span data-ttu-id="e1521-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e1521-137">ALIASES</span></span>

## <span data-ttu-id="e1521-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1521-138">NOTES</span></span>

<span data-ttu-id="e1521-139">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e1521-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1521-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1521-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e1521-141">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e1521-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e1521-142">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e1521-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e1521-143">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="e1521-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e1521-144">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e1521-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1521-145">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="e1521-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e1521-146">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="e1521-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e1521-147">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="e1521-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e1521-148">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="e1521-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e1521-149">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="e1521-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e1521-150">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="e1521-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e1521-151">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="e1521-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e1521-152">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="e1521-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e1521-153">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="e1521-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e1521-154">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e1521-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e1521-155">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e1521-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e1521-156">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1521-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e1521-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1521-157">RELATED LINKS</span></span>
