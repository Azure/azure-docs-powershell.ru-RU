---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075198"
---
# <span data-ttu-id="3435e-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="3435e-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="3435e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3435e-102">SYNOPSIS</span></span>


## <span data-ttu-id="3435e-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3435e-103">SYNTAX</span></span>

### <span data-ttu-id="3435e-104">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3435e-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3435e-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3435e-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3435e-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3435e-106">DESCRIPTION</span></span>


## <span data-ttu-id="3435e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3435e-107">EXAMPLES</span></span>

### <span data-ttu-id="3435e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3435e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="3435e-109">Удалите указанную подписку клиента.</span><span class="sxs-lookup"><span data-stu-id="3435e-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="3435e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3435e-110">PARAMETERS</span></span>

### <span data-ttu-id="3435e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3435e-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="3435e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3435e-112">-Force</span></span>


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

### <span data-ttu-id="3435e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3435e-113">-InputObject</span></span>
<span data-ttu-id="3435e-114">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3435e-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3435e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3435e-115">-PassThru</span></span>


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

### <span data-ttu-id="3435e-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3435e-116">-SubscriptionId</span></span>


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

### <span data-ttu-id="3435e-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3435e-117">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="3435e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3435e-118">-Confirm</span></span>
<span data-ttu-id="3435e-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3435e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3435e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3435e-120">-WhatIf</span></span>
<span data-ttu-id="3435e-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3435e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3435e-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3435e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3435e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3435e-123">CommonParameters</span></span>
<span data-ttu-id="3435e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3435e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3435e-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3435e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3435e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3435e-126">INPUTS</span></span>

### <span data-ttu-id="3435e-127">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3435e-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3435e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3435e-128">OUTPUTS</span></span>

### <span data-ttu-id="3435e-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3435e-129">System.Boolean</span></span>

<span data-ttu-id="3435e-130">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3435e-130">ALIASES</span></span>

## <span data-ttu-id="3435e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3435e-131">NOTES</span></span>

<span data-ttu-id="3435e-132">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3435e-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3435e-133">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3435e-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3435e-134">INPUTOBJECT <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="3435e-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="3435e-135">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3435e-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3435e-136">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="3435e-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3435e-137">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3435e-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3435e-138">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="3435e-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3435e-139">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="3435e-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3435e-140">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3435e-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3435e-141">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="3435e-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3435e-142">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="3435e-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3435e-143">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="3435e-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3435e-144">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="3435e-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3435e-145">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="3435e-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3435e-146">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="3435e-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3435e-147">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3435e-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3435e-148">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="3435e-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3435e-149">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="3435e-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="3435e-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3435e-150">RELATED LINKS</span></span>

