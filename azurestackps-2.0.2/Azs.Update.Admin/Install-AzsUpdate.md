---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076924"
---
# <span data-ttu-id="90ecb-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="90ecb-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="90ecb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="90ecb-103">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="90ecb-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="90ecb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90ecb-104">SYNTAX</span></span>

### <span data-ttu-id="90ecb-105">Apply (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90ecb-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90ecb-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90ecb-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90ecb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90ecb-107">DESCRIPTION</span></span>
<span data-ttu-id="90ecb-108">Применение определенного обновления на расположении обновления.</span><span class="sxs-lookup"><span data-stu-id="90ecb-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="90ecb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90ecb-109">EXAMPLES</span></span>

### <span data-ttu-id="90ecb-110">Пример 1: Install-AzsUpdate по имени</span><span class="sxs-lookup"><span data-stu-id="90ecb-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="90ecb-111">Unifiedgroup позволяет устанавливать конкретные обновления по имени.</span><span class="sxs-lookup"><span data-stu-id="90ecb-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="90ecb-112">Обратите внимание на то, что версия обновления строго превышает текущую версию.</span><span class="sxs-lookup"><span data-stu-id="90ecb-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="90ecb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90ecb-113">PARAMETERS</span></span>

### <span data-ttu-id="90ecb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90ecb-114">-AsJob</span></span>
<span data-ttu-id="90ecb-115">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="90ecb-115">Run the command as a job</span></span>

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

### <span data-ttu-id="90ecb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ecb-116">-DefaultProfile</span></span>
<span data-ttu-id="90ecb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90ecb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90ecb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90ecb-118">-InputObject</span></span>
<span data-ttu-id="90ecb-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="90ecb-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90ecb-120">-Location</span><span class="sxs-lookup"><span data-stu-id="90ecb-120">-Location</span></span>
<span data-ttu-id="90ecb-121">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="90ecb-121">The name of the update location.</span></span>

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

### <span data-ttu-id="90ecb-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90ecb-122">-Name</span></span>
<span data-ttu-id="90ecb-123">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="90ecb-123">Name of the update.</span></span>

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

### <span data-ttu-id="90ecb-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="90ecb-124">-NoWait</span></span>
<span data-ttu-id="90ecb-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="90ecb-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="90ecb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ecb-126">-ResourceGroupName</span></span>
<span data-ttu-id="90ecb-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90ecb-127">Resource group name.</span></span>

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

### <span data-ttu-id="90ecb-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90ecb-128">-SubscriptionId</span></span>
<span data-ttu-id="90ecb-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90ecb-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="90ecb-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="90ecb-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="90ecb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90ecb-131">-Confirm</span></span>
<span data-ttu-id="90ecb-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90ecb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ecb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ecb-133">-WhatIf</span></span>
<span data-ttu-id="90ecb-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90ecb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ecb-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90ecb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ecb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ecb-136">CommonParameters</span></span>
<span data-ttu-id="90ecb-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90ecb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ecb-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90ecb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ecb-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90ecb-139">INPUTS</span></span>

### <span data-ttu-id="90ecb-140">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="90ecb-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="90ecb-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90ecb-141">OUTPUTS</span></span>

### <span data-ttu-id="90ecb-142">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="90ecb-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="90ecb-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="90ecb-143">NOTES</span></span>

<span data-ttu-id="90ecb-144">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="90ecb-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90ecb-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90ecb-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="90ecb-146">INPUTOBJECT <IUpdateAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="90ecb-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90ecb-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="90ecb-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90ecb-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90ecb-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="90ecb-149">`[RunName <String>]`: Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="90ecb-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="90ecb-150">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90ecb-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="90ecb-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="90ecb-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="90ecb-152">`[UpdateLocation <String>]`: Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="90ecb-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="90ecb-153">`[UpdateName <String>]`: Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="90ecb-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="90ecb-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90ecb-154">RELATED LINKS</span></span>
