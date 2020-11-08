---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076856"
---
# <span data-ttu-id="1d8d1-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="1d8d1-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="1d8d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8d1-103">Восстанавливает оповещение.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-103">Repairs an alert.</span></span>

## <span data-ttu-id="1d8d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d8d1-104">SYNTAX</span></span>

### <span data-ttu-id="1d8d1-105">Восстановление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d8d1-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1d8d1-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1d8d1-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1d8d1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d8d1-107">DESCRIPTION</span></span>
<span data-ttu-id="1d8d1-108">Восстанавливает оповещение.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-108">Repairs an alert.</span></span>

## <span data-ttu-id="1d8d1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d8d1-109">EXAMPLES</span></span>

### <span data-ttu-id="1d8d1-110">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="1d8d1-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="1d8d1-111">Восстанавливает оповещение по имени.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="1d8d1-112">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="1d8d1-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="1d8d1-113">Восстанавливает оповещение с помощью трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="1d8d1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d8d1-114">PARAMETERS</span></span>

### <span data-ttu-id="1d8d1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d8d1-115">-AsJob</span></span>
<span data-ttu-id="1d8d1-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1d8d1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1d8d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8d1-117">-DefaultProfile</span></span>
<span data-ttu-id="1d8d1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d8d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d8d1-119">-InputObject</span></span>
<span data-ttu-id="1d8d1-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1d8d1-121">-Location</span><span class="sxs-lookup"><span data-stu-id="1d8d1-121">-Location</span></span>
<span data-ttu-id="1d8d1-122">Название региона</span><span class="sxs-lookup"><span data-stu-id="1d8d1-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1d8d1-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d8d1-123">-Name</span></span>
<span data-ttu-id="1d8d1-124">Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1d8d1-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="1d8d1-125">-NoWait</span></span>
<span data-ttu-id="1d8d1-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="1d8d1-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1d8d1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d8d1-127">-PassThru</span></span>
<span data-ttu-id="1d8d1-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1d8d1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8d1-129">-ResourceGroupName</span></span>
<span data-ttu-id="1d8d1-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1d8d1-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d8d1-131">-SubscriptionId</span></span>
<span data-ttu-id="1d8d1-132">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1d8d1-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1d8d1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d8d1-134">-Confirm</span></span>
<span data-ttu-id="1d8d1-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8d1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8d1-136">-WhatIf</span></span>
<span data-ttu-id="1d8d1-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8d1-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8d1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8d1-139">CommonParameters</span></span>
<span data-ttu-id="1d8d1-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8d1-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d8d1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8d1-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d8d1-142">INPUTS</span></span>

### <span data-ttu-id="1d8d1-143">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1d8d1-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="1d8d1-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d8d1-144">OUTPUTS</span></span>

### <span data-ttu-id="1d8d1-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d8d1-145">System.Boolean</span></span>



## <span data-ttu-id="1d8d1-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d8d1-146">NOTES</span></span>

<span data-ttu-id="1d8d1-147">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1d8d1-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1d8d1-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1d8d1-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1d8d1-150">`[AlertName <String>]`: Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="1d8d1-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1d8d1-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1d8d1-152">`[Location <String>]`: Имя области</span><span class="sxs-lookup"><span data-stu-id="1d8d1-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="1d8d1-153">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1d8d1-154">`[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="1d8d1-155">`[ServiceHealth <String>]`: Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="1d8d1-156">`[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="1d8d1-157">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1d8d1-158">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1d8d1-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d8d1-159">RELATED LINKS</span></span>

