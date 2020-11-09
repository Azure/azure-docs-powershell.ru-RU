---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312767"
---
# <span data-ttu-id="28ab3-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="28ab3-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="28ab3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="28ab3-103">Обновите Специальный HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="28ab3-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="28ab3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28ab3-104">SYNTAX</span></span>

### <span data-ttu-id="28ab3-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28ab3-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28ab3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="28ab3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28ab3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28ab3-107">DESCRIPTION</span></span>
<span data-ttu-id="28ab3-108">Обновите Специальный HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="28ab3-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="28ab3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28ab3-109">EXAMPLES</span></span>

### <span data-ttu-id="28ab3-110">Пример 1: обновление тега параметра выделенного HSM по имени</span><span class="sxs-lookup"><span data-stu-id="28ab3-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="28ab3-111">Эта команда обновляет тег параметра выделенного HSM по имени.</span><span class="sxs-lookup"><span data-stu-id="28ab3-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="28ab3-112">Пример 2: обновление тега параметра выделенного HSM по объекту</span><span class="sxs-lookup"><span data-stu-id="28ab3-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="28ab3-113">Эта команда обновляет тег параметра выделенного HSM по объекту.</span><span class="sxs-lookup"><span data-stu-id="28ab3-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="28ab3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28ab3-114">PARAMETERS</span></span>

### <span data-ttu-id="28ab3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28ab3-115">-AsJob</span></span>
<span data-ttu-id="28ab3-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="28ab3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="28ab3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ab3-117">-DefaultProfile</span></span>
<span data-ttu-id="28ab3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28ab3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28ab3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28ab3-119">-InputObject</span></span>
<span data-ttu-id="28ab3-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="28ab3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28ab3-121">-Name</span></span>
<span data-ttu-id="28ab3-122">Имя выделенного HSM.</span><span class="sxs-lookup"><span data-stu-id="28ab3-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="28ab3-123">-NoWait</span></span>
<span data-ttu-id="28ab3-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="28ab3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="28ab3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ab3-125">-ResourceGroupName</span></span>
<span data-ttu-id="28ab3-126">Имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="28ab3-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28ab3-127">-SubscriptionId</span></span>
<span data-ttu-id="28ab3-128">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="28ab3-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="28ab3-129">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="28ab3-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="28ab3-130">-Tag</span></span>
<span data-ttu-id="28ab3-131">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="28ab3-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ab3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28ab3-132">-Confirm</span></span>
<span data-ttu-id="28ab3-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28ab3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28ab3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28ab3-134">-WhatIf</span></span>
<span data-ttu-id="28ab3-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28ab3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28ab3-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28ab3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28ab3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ab3-137">CommonParameters</span></span>
<span data-ttu-id="28ab3-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28ab3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ab3-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28ab3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ab3-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28ab3-140">INPUTS</span></span>

### <span data-ttu-id="28ab3-141">Microsoft. Azure. PowerShell. командлеты. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="28ab3-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="28ab3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28ab3-142">OUTPUTS</span></span>

### <span data-ttu-id="28ab3-143">Microsoft. Azure. PowerShell. командлеты. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="28ab3-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="28ab3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="28ab3-144">NOTES</span></span>

<span data-ttu-id="28ab3-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="28ab3-145">ALIASES</span></span>

<span data-ttu-id="28ab3-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="28ab3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28ab3-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="28ab3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28ab3-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28ab3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28ab3-149">INPUTOBJECT <IDedicatedHsmIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="28ab3-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28ab3-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="28ab3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28ab3-151">`[Name <String>]`: Имя выделенного HSM.</span><span class="sxs-lookup"><span data-stu-id="28ab3-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="28ab3-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="28ab3-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="28ab3-153">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="28ab3-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="28ab3-154">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="28ab3-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="28ab3-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28ab3-155">RELATED LINKS</span></span>

