---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231681"
---
# <span data-ttu-id="5259f-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="5259f-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="5259f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5259f-102">SYNOPSIS</span></span>
<span data-ttu-id="5259f-103">Создает новое прослушивание группы доступности.</span><span class="sxs-lookup"><span data-stu-id="5259f-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="5259f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5259f-104">SYNTAX</span></span>

### <span data-ttu-id="5259f-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5259f-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5259f-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="5259f-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5259f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5259f-107">DESCRIPTION</span></span>
<span data-ttu-id="5259f-108">С New-AzAvailabilityGroupListener создается новый слушатель группы доступности.</span><span class="sxs-lookup"><span data-stu-id="5259f-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="5259f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5259f-109">EXAMPLES</span></span>

### <span data-ttu-id="5259f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5259f-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="5259f-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="5259f-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="5259f-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="5259f-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="5259f-113">Создает новую группу доступности AgListener01 для группы доступности AvailabilityGroup01 в SQL Virtual Machine Group SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="5259f-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="5259f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5259f-114">PARAMETERS</span></span>

### <span data-ttu-id="5259f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5259f-115">-AsJob</span></span>
<span data-ttu-id="5259f-116">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="5259f-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="5259f-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="5259f-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="5259f-118">Имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="5259f-118">Availability Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5259f-119">-DefaultProfile</span></span>
<span data-ttu-id="5259f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5259f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5259f-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="5259f-121">-IpAddress</span></span>
<span data-ttu-id="5259f-122">Частный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="5259f-122">Private Ip Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="5259f-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="5259f-124">ИД балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="5259f-124">Load Balancer Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5259f-125">-Name</span></span>
<span data-ttu-id="5259f-126">Имя прослушавщика группы доступности.</span><span class="sxs-lookup"><span data-stu-id="5259f-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-127">-Port</span><span class="sxs-lookup"><span data-stu-id="5259f-127">-Port</span></span>
<span data-ttu-id="5259f-128">Номер порта прослушки AG.</span><span class="sxs-lookup"><span data-stu-id="5259f-128">Port number of AG Listener.</span></span> <span data-ttu-id="5259f-129">Значение по умолчанию — 1433.</span><span class="sxs-lookup"><span data-stu-id="5259f-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-130">-СкайпПорт</span><span class="sxs-lookup"><span data-stu-id="5259f-130">-ProbePort</span></span>
<span data-ttu-id="5259f-131">ПортЫ-порты</span><span class="sxs-lookup"><span data-stu-id="5259f-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="5259f-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="5259f-133">ИД ресурса общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="5259f-133">Public Ip Address Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5259f-134">-ResourceGroupName</span></span>
<span data-ttu-id="5259f-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5259f-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="5259f-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5259f-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="5259f-137">Список ИД ресурсов Sql VM</span><span class="sxs-lookup"><span data-stu-id="5259f-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="5259f-138">-SqlVMGroupName</span></span>
<span data-ttu-id="5259f-139">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5259f-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="5259f-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="5259f-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="5259f-141">SQL группа виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5259f-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="5259f-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5259f-142">-SubnetId</span></span>
<span data-ttu-id="5259f-143">ИД ресурсов подсети</span><span class="sxs-lookup"><span data-stu-id="5259f-143">Subnet Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5259f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5259f-144">-Confirm</span></span>
<span data-ttu-id="5259f-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5259f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5259f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5259f-146">-WhatIf</span></span>
<span data-ttu-id="5259f-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5259f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5259f-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5259f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5259f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5259f-149">CommonParameters</span></span>
<span data-ttu-id="5259f-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5259f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5259f-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5259f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5259f-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5259f-152">INPUTS</span></span>

### <span data-ttu-id="5259f-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMaviree.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="5259f-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="5259f-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5259f-154">OUTPUTS</span></span>

### <span data-ttu-id="5259f-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="5259f-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="5259f-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5259f-156">NOTES</span></span>

## <span data-ttu-id="5259f-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5259f-157">RELATED LINKS</span></span>
