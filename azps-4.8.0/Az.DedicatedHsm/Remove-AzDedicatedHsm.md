---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244553"
---
# <span data-ttu-id="13bee-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="13bee-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="13bee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13bee-102">SYNOPSIS</span></span>
<span data-ttu-id="13bee-103">Удаляет указанный выделенный HSM службы Azure.</span><span class="sxs-lookup"><span data-stu-id="13bee-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="13bee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13bee-104">SYNTAX</span></span>

### <span data-ttu-id="13bee-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13bee-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13bee-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="13bee-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13bee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13bee-107">DESCRIPTION</span></span>
<span data-ttu-id="13bee-108">Удаляет указанный выделенный HSM службы Azure.</span><span class="sxs-lookup"><span data-stu-id="13bee-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="13bee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13bee-109">EXAMPLES</span></span>

### <span data-ttu-id="13bee-110">Пример 1: Удаление выделенного HSM-кода по имени</span><span class="sxs-lookup"><span data-stu-id="13bee-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="13bee-111">Этот commnad удаляет аппаратный модуль безопасности (HSM) по имени.</span><span class="sxs-lookup"><span data-stu-id="13bee-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="13bee-112">Пример 2: Удаление выделенного HSM-кода с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="13bee-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="13bee-113">Этот commnad удаляет выделенный HSM-объект по объекту.</span><span class="sxs-lookup"><span data-stu-id="13bee-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="13bee-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13bee-114">PARAMETERS</span></span>

### <span data-ttu-id="13bee-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13bee-115">-AsJob</span></span>
<span data-ttu-id="13bee-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="13bee-116">Run the command as a job</span></span>

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

### <span data-ttu-id="13bee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13bee-117">-DefaultProfile</span></span>
<span data-ttu-id="13bee-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13bee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13bee-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13bee-119">-InputObject</span></span>
<span data-ttu-id="13bee-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="13bee-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13bee-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13bee-121">-Name</span></span>
<span data-ttu-id="13bee-122">Имя выделенного HSM – файла, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="13bee-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="13bee-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="13bee-123">-NoWait</span></span>
<span data-ttu-id="13bee-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="13bee-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13bee-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13bee-125">-PassThru</span></span>
<span data-ttu-id="13bee-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="13bee-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="13bee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13bee-127">-ResourceGroupName</span></span>
<span data-ttu-id="13bee-128">Имя группы ресурсов, к которой принадлежит выделенный HSM.</span><span class="sxs-lookup"><span data-stu-id="13bee-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="13bee-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13bee-129">-SubscriptionId</span></span>
<span data-ttu-id="13bee-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="13bee-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="13bee-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="13bee-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="13bee-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13bee-132">-Confirm</span></span>
<span data-ttu-id="13bee-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13bee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13bee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13bee-134">-WhatIf</span></span>
<span data-ttu-id="13bee-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13bee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13bee-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13bee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13bee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bee-137">CommonParameters</span></span>
<span data-ttu-id="13bee-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13bee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bee-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13bee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bee-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13bee-140">INPUTS</span></span>

### <span data-ttu-id="13bee-141">Microsoft. Azure. PowerShell. командлеты. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="13bee-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="13bee-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13bee-142">OUTPUTS</span></span>

### <span data-ttu-id="13bee-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13bee-143">System.Boolean</span></span>

## <span data-ttu-id="13bee-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="13bee-144">NOTES</span></span>

<span data-ttu-id="13bee-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="13bee-145">ALIASES</span></span>

<span data-ttu-id="13bee-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="13bee-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13bee-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="13bee-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13bee-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13bee-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13bee-149">INPUTOBJECT <IDedicatedHsmIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="13bee-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13bee-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="13bee-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13bee-151">`[Name <String>]`: Имя выделенного HSM.</span><span class="sxs-lookup"><span data-stu-id="13bee-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="13bee-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="13bee-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="13bee-153">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="13bee-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="13bee-154">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="13bee-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="13bee-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13bee-155">RELATED LINKS</span></span>
