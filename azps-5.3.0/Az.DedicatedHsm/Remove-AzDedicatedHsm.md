---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516902"
---
# <span data-ttu-id="b3b43-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b3b43-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="b3b43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b43-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b43-103">Удаляет указанную службу azure Dedicated HSM.</span><span class="sxs-lookup"><span data-stu-id="b3b43-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="b3b43-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3b43-104">SYNTAX</span></span>

### <span data-ttu-id="b3b43-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3b43-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3b43-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3b43-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3b43-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3b43-107">DESCRIPTION</span></span>
<span data-ttu-id="b3b43-108">Удаляет указанную службу azure Dedicated HSM.</span><span class="sxs-lookup"><span data-stu-id="b3b43-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="b3b43-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3b43-109">EXAMPLES</span></span>

### <span data-ttu-id="b3b43-110">Пример 1. Удаление выделенной HSM по имени</span><span class="sxs-lookup"><span data-stu-id="b3b43-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="b3b43-111">Эта компания удаляет модуль безопасности оборудования (HSM) по имени.</span><span class="sxs-lookup"><span data-stu-id="b3b43-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="b3b43-112">Пример 2. Удаление выделенной HSM-объекта</span><span class="sxs-lookup"><span data-stu-id="b3b43-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="b3b43-113">Эта команда удаляет выделенный HSM-объект.</span><span class="sxs-lookup"><span data-stu-id="b3b43-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="b3b43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3b43-114">PARAMETERS</span></span>

### <span data-ttu-id="b3b43-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3b43-115">-AsJob</span></span>
<span data-ttu-id="b3b43-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b3b43-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3b43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b43-117">-DefaultProfile</span></span>
<span data-ttu-id="b3b43-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b43-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b43-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b43-119">-InputObject</span></span>
<span data-ttu-id="b3b43-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b3b43-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b3b43-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b3b43-121">-Name</span></span>
<span data-ttu-id="b3b43-122">Название выделенной HSM-части, удаляемой</span><span class="sxs-lookup"><span data-stu-id="b3b43-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="b3b43-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3b43-123">-NoWait</span></span>
<span data-ttu-id="b3b43-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="b3b43-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3b43-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3b43-125">-PassThru</span></span>
<span data-ttu-id="b3b43-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="b3b43-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3b43-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b43-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3b43-128">Имя группы ресурсов, к которой принадлежит выделенная HSM.</span><span class="sxs-lookup"><span data-stu-id="b3b43-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="b3b43-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3b43-129">-SubscriptionId</span></span>
<span data-ttu-id="b3b43-130">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b43-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b3b43-131">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b3b43-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b3b43-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3b43-132">-Confirm</span></span>
<span data-ttu-id="b3b43-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3b43-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b43-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b43-134">-WhatIf</span></span>
<span data-ttu-id="b3b43-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3b43-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3b43-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b3b43-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b43-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b43-137">CommonParameters</span></span>
<span data-ttu-id="b3b43-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b43-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b43-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3b43-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b43-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3b43-140">INPUTS</span></span>

### <span data-ttu-id="b3b43-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="b3b43-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="b3b43-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3b43-142">OUTPUTS</span></span>

### <span data-ttu-id="b3b43-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3b43-143">System.Boolean</span></span>

## <span data-ttu-id="b3b43-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3b43-144">NOTES</span></span>

<span data-ttu-id="b3b43-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b3b43-145">ALIASES</span></span>

<span data-ttu-id="b3b43-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b3b43-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3b43-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b3b43-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3b43-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3b43-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3b43-149">INPUTOBJECT <IDedicatedHsmIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b3b43-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3b43-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b3b43-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3b43-151">`[Name <String>]`: название выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="b3b43-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="b3b43-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="b3b43-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="b3b43-153">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b43-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b3b43-154">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b3b43-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b3b43-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3b43-155">RELATED LINKS</span></span>

