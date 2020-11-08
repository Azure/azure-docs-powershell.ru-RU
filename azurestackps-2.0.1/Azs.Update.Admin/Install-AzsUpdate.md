---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075324"
---
# <span data-ttu-id="e6f31-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="e6f31-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="e6f31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6f31-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f31-103">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="e6f31-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="e6f31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6f31-104">SYNTAX</span></span>

### <span data-ttu-id="e6f31-105">Apply (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6f31-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e6f31-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6f31-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6f31-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6f31-107">DESCRIPTION</span></span>
<span data-ttu-id="e6f31-108">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="e6f31-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="e6f31-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6f31-109">EXAMPLES</span></span>

### <span data-ttu-id="e6f31-110">Пример 1: Install-AzsUpdate по имени</span><span class="sxs-lookup"><span data-stu-id="e6f31-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="e6f31-111">Unifiedgroup позволяет устанавливать конкретные обновления по имени.</span><span class="sxs-lookup"><span data-stu-id="e6f31-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="e6f31-112">Обратите внимание на то, что версия обновления строго превышает текущую версию.</span><span class="sxs-lookup"><span data-stu-id="e6f31-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="e6f31-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6f31-113">PARAMETERS</span></span>

### <span data-ttu-id="e6f31-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6f31-114">-AsJob</span></span>
<span data-ttu-id="e6f31-115">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e6f31-115">Run the command as a job</span></span>

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

### <span data-ttu-id="e6f31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f31-116">-DefaultProfile</span></span>
<span data-ttu-id="e6f31-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f31-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f31-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f31-118">-InputObject</span></span>
<span data-ttu-id="e6f31-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e6f31-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e6f31-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e6f31-120">-Location</span></span>
<span data-ttu-id="e6f31-121">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="e6f31-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e6f31-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6f31-122">-Name</span></span>
<span data-ttu-id="e6f31-123">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="e6f31-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e6f31-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="e6f31-124">-NoWait</span></span>
<span data-ttu-id="e6f31-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="e6f31-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e6f31-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f31-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6f31-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6f31-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e6f31-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6f31-128">-SubscriptionId</span></span>
<span data-ttu-id="e6f31-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f31-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e6f31-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e6f31-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e6f31-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6f31-131">-Confirm</span></span>
<span data-ttu-id="e6f31-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6f31-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f31-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f31-133">-WhatIf</span></span>
<span data-ttu-id="e6f31-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6f31-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f31-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6f31-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f31-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f31-136">CommonParameters</span></span>
<span data-ttu-id="e6f31-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6f31-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f31-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6f31-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f31-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6f31-139">INPUTS</span></span>

### <span data-ttu-id="e6f31-140">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e6f31-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="e6f31-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6f31-141">OUTPUTS</span></span>

### <span data-ttu-id="e6f31-142">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="e6f31-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="e6f31-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6f31-143">NOTES</span></span>

<span data-ttu-id="e6f31-144">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e6f31-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6f31-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6f31-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e6f31-146">INPUTOBJECT <IUpdateAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e6f31-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6f31-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e6f31-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6f31-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6f31-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="e6f31-149">`[RunName <String>]`: Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="e6f31-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="e6f31-150">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f31-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="e6f31-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e6f31-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e6f31-152">`[UpdateLocation <String>]`: Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="e6f31-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="e6f31-153">`[UpdateName <String>]`: Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="e6f31-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="e6f31-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6f31-154">RELATED LINKS</span></span>

