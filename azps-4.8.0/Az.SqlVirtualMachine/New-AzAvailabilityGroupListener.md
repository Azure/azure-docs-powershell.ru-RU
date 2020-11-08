---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077537"
---
# <span data-ttu-id="06474-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="06474-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="06474-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06474-102">SYNOPSIS</span></span>
<span data-ttu-id="06474-103">Создает новый прослушиватель группы доступности.</span><span class="sxs-lookup"><span data-stu-id="06474-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="06474-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06474-104">SYNTAX</span></span>

### <span data-ttu-id="06474-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06474-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06474-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="06474-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06474-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06474-107">DESCRIPTION</span></span>
<span data-ttu-id="06474-108">Командлет New-AzAvailabilityGroupListener создает новый прослушиватель группы доступности.</span><span class="sxs-lookup"><span data-stu-id="06474-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="06474-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06474-109">EXAMPLES</span></span>

### <span data-ttu-id="06474-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06474-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="06474-111">Name ResourceGroupName имя_группы AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="06474-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="06474-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="06474-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="06474-113">Создание нового прослушивателя группы доступности AgListener01 для группы доступности AvailabilityGroup01 в группе "виртуальная машина SQL" SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="06474-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="06474-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06474-114">PARAMETERS</span></span>

### <span data-ttu-id="06474-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06474-115">-AsJob</span></span>
<span data-ttu-id="06474-116">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="06474-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="06474-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="06474-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="06474-118">Имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="06474-118">Availability Group name.</span></span>

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

### <span data-ttu-id="06474-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06474-119">-DefaultProfile</span></span>
<span data-ttu-id="06474-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06474-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06474-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="06474-121">-IpAddress</span></span>
<span data-ttu-id="06474-122">Частный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="06474-122">Private Ip Address</span></span>

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

### <span data-ttu-id="06474-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="06474-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="06474-124">Идентификатор подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="06474-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="06474-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06474-125">-Name</span></span>
<span data-ttu-id="06474-126">Имя прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="06474-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="06474-127">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="06474-127">-Port</span></span>
<span data-ttu-id="06474-128">Номер порта для прослушивателя AG.</span><span class="sxs-lookup"><span data-stu-id="06474-128">Port number of AG Listener.</span></span> <span data-ttu-id="06474-129">Значение по умолчанию — 1433.</span><span class="sxs-lookup"><span data-stu-id="06474-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="06474-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="06474-130">-ProbePort</span></span>
<span data-ttu-id="06474-131">Пробный порт</span><span class="sxs-lookup"><span data-stu-id="06474-131">Probe Port</span></span>

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

### <span data-ttu-id="06474-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="06474-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="06474-133">Идентификатор ресурса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="06474-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="06474-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06474-134">-ResourceGroupName</span></span>
<span data-ttu-id="06474-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06474-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="06474-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="06474-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="06474-137">Список идентификаторов ресурсов виртуальной машины SQL</span><span class="sxs-lookup"><span data-stu-id="06474-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="06474-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="06474-138">-SqlVMGroupName</span></span>
<span data-ttu-id="06474-139">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="06474-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="06474-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="06474-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="06474-141">Объект группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="06474-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="06474-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="06474-142">-SubnetId</span></span>
<span data-ttu-id="06474-143">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="06474-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="06474-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06474-144">-Confirm</span></span>
<span data-ttu-id="06474-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06474-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06474-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06474-146">-WhatIf</span></span>
<span data-ttu-id="06474-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06474-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06474-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06474-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06474-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06474-149">CommonParameters</span></span>
<span data-ttu-id="06474-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06474-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06474-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06474-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06474-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06474-152">INPUTS</span></span>

### <span data-ttu-id="06474-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="06474-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="06474-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06474-154">OUTPUTS</span></span>

### <span data-ttu-id="06474-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="06474-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="06474-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="06474-156">NOTES</span></span>

## <span data-ttu-id="06474-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06474-157">RELATED LINKS</span></span>
