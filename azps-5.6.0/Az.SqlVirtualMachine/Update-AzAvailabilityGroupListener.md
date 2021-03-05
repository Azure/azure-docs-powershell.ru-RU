---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: c94f1e842697a64dd95f7d5ccb90e389484a61e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967251"
---
# <span data-ttu-id="8671c-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="8671c-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="8671c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8671c-102">SYNOPSIS</span></span>
<span data-ttu-id="8671c-103">Обновляет прослушивание группы доступности.</span><span class="sxs-lookup"><span data-stu-id="8671c-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="8671c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8671c-104">SYNTAX</span></span>

### <span data-ttu-id="8671c-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8671c-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8671c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8671c-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8671c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8671c-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8671c-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="8671c-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8671c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8671c-109">DESCRIPTION</span></span>
<span data-ttu-id="8671c-110">Этот Update-AzAvailabilityGroupListener обновляет прослушивание группы доступности.</span><span class="sxs-lookup"><span data-stu-id="8671c-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="8671c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8671c-111">EXAMPLES</span></span>

### <span data-ttu-id="8671c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8671c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="8671c-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="8671c-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="8671c-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="8671c-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="8671c-115">Обновляет список SQL виртуальных машин для прослушивания группы доступности.</span><span class="sxs-lookup"><span data-stu-id="8671c-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="8671c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8671c-116">PARAMETERS</span></span>

### <span data-ttu-id="8671c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8671c-117">-AsJob</span></span>
<span data-ttu-id="8671c-118">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="8671c-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8671c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8671c-119">-DefaultProfile</span></span>
<span data-ttu-id="8671c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8671c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8671c-121">-InputObject</span></span>
<span data-ttu-id="8671c-122">Объект "Прослушивание группы доступности".</span><span class="sxs-lookup"><span data-stu-id="8671c-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8671c-123">-Name</span></span>
<span data-ttu-id="8671c-124">Имя прослушавщика группы доступности.</span><span class="sxs-lookup"><span data-stu-id="8671c-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8671c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8671c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8671c-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8671c-127">-ResourceId</span></span>
<span data-ttu-id="8671c-128">ИД ресурса группы «Доступность»</span><span class="sxs-lookup"><span data-stu-id="8671c-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="8671c-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="8671c-130">Список ИД ресурсов Sql VM</span><span class="sxs-lookup"><span data-stu-id="8671c-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="8671c-131">-SqlVMGroupName</span></span>
<span data-ttu-id="8671c-132">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8671c-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="8671c-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="8671c-134">SQL группа виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8671c-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8671c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8671c-135">-Confirm</span></span>
<span data-ttu-id="8671c-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8671c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8671c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8671c-137">-WhatIf</span></span>
<span data-ttu-id="8671c-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8671c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8671c-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8671c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8671c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8671c-140">CommonParameters</span></span>
<span data-ttu-id="8671c-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8671c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8671c-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8671c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8671c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8671c-143">INPUTS</span></span>

### <span data-ttu-id="8671c-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="8671c-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="8671c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8671c-145">System.String</span></span>

### <span data-ttu-id="8671c-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMaviree.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="8671c-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="8671c-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8671c-147">OUTPUTS</span></span>

### <span data-ttu-id="8671c-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="8671c-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="8671c-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8671c-149">NOTES</span></span>

## <span data-ttu-id="8671c-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8671c-150">RELATED LINKS</span></span>
