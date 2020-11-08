---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072618"
---
# <span data-ttu-id="13e59-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="13e59-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="13e59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13e59-102">SYNOPSIS</span></span>
<span data-ttu-id="13e59-103">Обновляет прослушиватель группы доступности.</span><span class="sxs-lookup"><span data-stu-id="13e59-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="13e59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13e59-104">SYNTAX</span></span>

### <span data-ttu-id="13e59-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13e59-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13e59-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="13e59-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13e59-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13e59-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13e59-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="13e59-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13e59-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13e59-109">DESCRIPTION</span></span>
<span data-ttu-id="13e59-110">Командлет Update-AzAvailabilityGroupListener обновляет прослушиватель группы доступности.</span><span class="sxs-lookup"><span data-stu-id="13e59-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="13e59-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13e59-111">EXAMPLES</span></span>

### <span data-ttu-id="13e59-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13e59-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="13e59-113">Name ResourceGroupName имя_группы AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="13e59-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="13e59-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="13e59-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="13e59-115">Обновляет виртуальные машины SQL списка для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="13e59-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="13e59-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13e59-116">PARAMETERS</span></span>

### <span data-ttu-id="13e59-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13e59-117">-AsJob</span></span>
<span data-ttu-id="13e59-118">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="13e59-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="13e59-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e59-119">-DefaultProfile</span></span>
<span data-ttu-id="13e59-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13e59-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e59-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13e59-121">-InputObject</span></span>
<span data-ttu-id="13e59-122">Объект прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="13e59-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="13e59-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13e59-123">-Name</span></span>
<span data-ttu-id="13e59-124">Имя прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="13e59-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="13e59-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13e59-125">-ResourceGroupName</span></span>
<span data-ttu-id="13e59-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13e59-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="13e59-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13e59-127">-ResourceId</span></span>
<span data-ttu-id="13e59-128">Идентификатор ресурса прослушивателя группы доступности</span><span class="sxs-lookup"><span data-stu-id="13e59-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="13e59-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="13e59-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="13e59-130">Список идентификаторов ресурсов виртуальной машины SQL</span><span class="sxs-lookup"><span data-stu-id="13e59-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="13e59-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="13e59-131">-SqlVMGroupName</span></span>
<span data-ttu-id="13e59-132">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="13e59-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="13e59-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="13e59-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="13e59-134">Объект группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="13e59-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="13e59-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13e59-135">-Confirm</span></span>
<span data-ttu-id="13e59-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13e59-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e59-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e59-137">-WhatIf</span></span>
<span data-ttu-id="13e59-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13e59-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13e59-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13e59-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e59-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e59-140">CommonParameters</span></span>
<span data-ttu-id="13e59-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13e59-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e59-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13e59-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e59-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13e59-143">INPUTS</span></span>

### <span data-ttu-id="13e59-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="13e59-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="13e59-145">System. String</span><span class="sxs-lookup"><span data-stu-id="13e59-145">System.String</span></span>

### <span data-ttu-id="13e59-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="13e59-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="13e59-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13e59-147">OUTPUTS</span></span>

### <span data-ttu-id="13e59-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="13e59-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="13e59-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="13e59-149">NOTES</span></span>

## <span data-ttu-id="13e59-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13e59-150">RELATED LINKS</span></span>
