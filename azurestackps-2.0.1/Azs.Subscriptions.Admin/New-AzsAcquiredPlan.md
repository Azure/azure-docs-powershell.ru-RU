---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075337"
---
# <span data-ttu-id="e7447-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="e7447-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="e7447-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7447-102">SYNOPSIS</span></span>


## <span data-ttu-id="e7447-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7447-103">SYNTAX</span></span>

### <span data-ttu-id="e7447-104">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7447-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e7447-105">Заново</span><span class="sxs-lookup"><span data-stu-id="e7447-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e7447-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7447-106">DESCRIPTION</span></span>


## <span data-ttu-id="e7447-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7447-107">EXAMPLES</span></span>

### <span data-ttu-id="e7447-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7447-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="e7447-109">Создание плана подписки.</span><span class="sxs-lookup"><span data-stu-id="e7447-109">Create a subscription plan.</span></span>

## <span data-ttu-id="e7447-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7447-110">PARAMETERS</span></span>

### <span data-ttu-id="e7447-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="e7447-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="e7447-112">Для конструирования ознакомьтесь с разделом "Заметки" для свойств ACQUIREDPLANDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e7447-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e7447-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="e7447-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7447-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7447-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="e7447-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="e7447-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7447-116">-ID</span><span class="sxs-lookup"><span data-stu-id="e7447-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7447-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="e7447-117">-PlanAcquisitionId</span></span>


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

### <span data-ttu-id="e7447-118">-PlanId</span><span class="sxs-lookup"><span data-stu-id="e7447-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7447-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="e7447-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7447-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7447-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7447-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7447-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="e7447-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7447-122">-Confirm</span></span>
<span data-ttu-id="e7447-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7447-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7447-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7447-124">-WhatIf</span></span>
<span data-ttu-id="e7447-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7447-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7447-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7447-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7447-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7447-127">CommonParameters</span></span>
<span data-ttu-id="e7447-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7447-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7447-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7447-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7447-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7447-130">INPUTS</span></span>

### <span data-ttu-id="e7447-131">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="e7447-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="e7447-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7447-132">OUTPUTS</span></span>

### <span data-ttu-id="e7447-133">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="e7447-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="e7447-134">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e7447-134">ALIASES</span></span>

<span data-ttu-id="e7447-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="e7447-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="e7447-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7447-136">NOTES</span></span>

<span data-ttu-id="e7447-137">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7447-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7447-138">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e7447-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e7447-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="e7447-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="e7447-140">`[AcquisitionId <String>]`: Идентификатор приобретения.</span><span class="sxs-lookup"><span data-stu-id="e7447-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="e7447-141">`[AcquisitionTime <DateTime?>]`: Время приобретения.</span><span class="sxs-lookup"><span data-stu-id="e7447-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="e7447-142">`[ExternalReferenceId <String>]`: Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="e7447-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="e7447-143">`[Id <String>]`: Идентификатор в контексте подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="e7447-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="e7447-144">`[PlanId <String>]`: Идентификатор плана в контексте подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="e7447-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="e7447-145">`[ProvisioningState <ProvisioningState?>]`: Состояние подготовки.</span><span class="sxs-lookup"><span data-stu-id="e7447-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="e7447-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7447-146">RELATED LINKS</span></span>

