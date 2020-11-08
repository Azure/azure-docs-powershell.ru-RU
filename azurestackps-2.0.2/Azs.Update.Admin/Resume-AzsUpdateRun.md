---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076745"
---
# <span data-ttu-id="67c5d-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="67c5d-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="67c5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="67c5d-103">Возобновление сбоя.</span><span class="sxs-lookup"><span data-stu-id="67c5d-103">Resume a failed update.</span></span>

## <span data-ttu-id="67c5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67c5d-104">SYNTAX</span></span>

### <span data-ttu-id="67c5d-105">Повторный запуск (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67c5d-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67c5d-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67c5d-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67c5d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67c5d-107">DESCRIPTION</span></span>
<span data-ttu-id="67c5d-108">Возобновление сбоя.</span><span class="sxs-lookup"><span data-stu-id="67c5d-108">Resume a failed update.</span></span>

## <span data-ttu-id="67c5d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67c5d-109">EXAMPLES</span></span>

### <span data-ttu-id="67c5d-110">Пример 1: Resume-AzsUpdateRun по имени и UpdateName</span><span class="sxs-lookup"><span data-stu-id="67c5d-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="67c5d-111">Unifiedgroup позволяет повторно выполнить определенное сбойное обновление.</span><span class="sxs-lookup"><span data-stu-id="67c5d-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="67c5d-112">Обратите внимание на то, что версия обновления строго превышает текущую версию.</span><span class="sxs-lookup"><span data-stu-id="67c5d-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="67c5d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67c5d-113">PARAMETERS</span></span>

### <span data-ttu-id="67c5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c5d-114">-DefaultProfile</span></span>
<span data-ttu-id="67c5d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67c5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67c5d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67c5d-116">-InputObject</span></span>
<span data-ttu-id="67c5d-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="67c5d-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="67c5d-118">-Location</span><span class="sxs-lookup"><span data-stu-id="67c5d-118">-Location</span></span>
<span data-ttu-id="67c5d-119">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="67c5d-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67c5d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67c5d-120">-Name</span></span>
<span data-ttu-id="67c5d-121">Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="67c5d-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67c5d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67c5d-122">-PassThru</span></span>
<span data-ttu-id="67c5d-123">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="67c5d-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="67c5d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c5d-124">-ResourceGroupName</span></span>
<span data-ttu-id="67c5d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67c5d-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67c5d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67c5d-126">-SubscriptionId</span></span>
<span data-ttu-id="67c5d-127">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67c5d-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="67c5d-128">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="67c5d-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67c5d-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="67c5d-129">-UpdateName</span></span>
<span data-ttu-id="67c5d-130">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="67c5d-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="67c5d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67c5d-131">-Confirm</span></span>
<span data-ttu-id="67c5d-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67c5d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c5d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c5d-133">-WhatIf</span></span>
<span data-ttu-id="67c5d-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67c5d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67c5d-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67c5d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c5d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c5d-136">CommonParameters</span></span>
<span data-ttu-id="67c5d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67c5d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c5d-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67c5d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c5d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67c5d-139">INPUTS</span></span>

### <span data-ttu-id="67c5d-140">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="67c5d-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="67c5d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67c5d-141">OUTPUTS</span></span>

### <span data-ttu-id="67c5d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67c5d-142">System.Boolean</span></span>



## <span data-ttu-id="67c5d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="67c5d-143">NOTES</span></span>

<span data-ttu-id="67c5d-144">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="67c5d-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67c5d-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67c5d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="67c5d-146">INPUTOBJECT <IUpdateAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="67c5d-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67c5d-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="67c5d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67c5d-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67c5d-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="67c5d-149">`[RunName <String>]`: Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="67c5d-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="67c5d-150">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67c5d-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="67c5d-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="67c5d-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="67c5d-152">`[UpdateLocation <String>]`: Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="67c5d-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="67c5d-153">`[UpdateName <String>]`: Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="67c5d-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="67c5d-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67c5d-154">RELATED LINKS</span></span>
