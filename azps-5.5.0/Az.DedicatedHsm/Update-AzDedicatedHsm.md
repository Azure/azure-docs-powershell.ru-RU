---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232092"
---
# <span data-ttu-id="e062a-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e062a-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="e062a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e062a-102">SYNOPSIS</span></span>
<span data-ttu-id="e062a-103">Обновим выделенную службу HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="e062a-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="e062a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e062a-104">SYNTAX</span></span>

### <span data-ttu-id="e062a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e062a-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e062a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e062a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e062a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e062a-107">DESCRIPTION</span></span>
<span data-ttu-id="e062a-108">Обновим выделенную службу HSM в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="e062a-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="e062a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e062a-109">EXAMPLES</span></span>

### <span data-ttu-id="e062a-110">Пример 1. Обновление тега параметра dedicated HSM по имени</span><span class="sxs-lookup"><span data-stu-id="e062a-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e062a-111">Эта команда обновляет тег параметра "Выделенный HSM по имени"</span><span class="sxs-lookup"><span data-stu-id="e062a-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="e062a-112">Пример 2. Обновление тега параметра "Выделенный HSM по объекту"</span><span class="sxs-lookup"><span data-stu-id="e062a-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e062a-113">Эта команда обновляет тег параметра "Выделенный HSM по объекту"</span><span class="sxs-lookup"><span data-stu-id="e062a-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="e062a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e062a-114">PARAMETERS</span></span>

### <span data-ttu-id="e062a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e062a-115">-AsJob</span></span>
<span data-ttu-id="e062a-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e062a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e062a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e062a-117">-DefaultProfile</span></span>
<span data-ttu-id="e062a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e062a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e062a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e062a-119">-InputObject</span></span>
<span data-ttu-id="e062a-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="e062a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e062a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e062a-121">-Name</span></span>
<span data-ttu-id="e062a-122">Название выделенной HSM-части</span><span class="sxs-lookup"><span data-stu-id="e062a-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="e062a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e062a-123">-NoWait</span></span>
<span data-ttu-id="e062a-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e062a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e062a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e062a-125">-ResourceGroupName</span></span>
<span data-ttu-id="e062a-126">Имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="e062a-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="e062a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e062a-127">-SubscriptionId</span></span>
<span data-ttu-id="e062a-128">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e062a-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e062a-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="e062a-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e062a-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e062a-130">-Tag</span></span>
<span data-ttu-id="e062a-131">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="e062a-131">Resource tags</span></span>

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

### <span data-ttu-id="e062a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e062a-132">-Confirm</span></span>
<span data-ttu-id="e062a-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e062a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e062a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e062a-134">-WhatIf</span></span>
<span data-ttu-id="e062a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e062a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e062a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e062a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e062a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e062a-137">CommonParameters</span></span>
<span data-ttu-id="e062a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e062a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e062a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e062a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e062a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e062a-140">INPUTS</span></span>

### <span data-ttu-id="e062a-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="e062a-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="e062a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e062a-142">OUTPUTS</span></span>

### <span data-ttu-id="e062a-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e062a-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="e062a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e062a-144">NOTES</span></span>

<span data-ttu-id="e062a-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e062a-145">ALIASES</span></span>

<span data-ttu-id="e062a-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e062a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e062a-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e062a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e062a-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e062a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e062a-149">INPUTOBJECT <IDedicatedHsmIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="e062a-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e062a-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e062a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e062a-151">`[Name <String>]`: название выделенного HSM</span><span class="sxs-lookup"><span data-stu-id="e062a-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="e062a-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="e062a-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="e062a-153">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e062a-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e062a-154">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="e062a-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e062a-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e062a-155">RELATED LINKS</span></span>

