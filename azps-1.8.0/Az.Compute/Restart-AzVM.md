---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 5f2c7d4c3a047a4893158e7f1a12b375106d640b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731264"
---
# <span data-ttu-id="d573d-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d573d-101">Restart-AzVM</span></span>

## <span data-ttu-id="d573d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d573d-102">SYNOPSIS</span></span>
<span data-ttu-id="d573d-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="d573d-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="d573d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d573d-104">SYNTAX</span></span>

### <span data-ttu-id="d573d-105">RestartResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d573d-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d573d-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d573d-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d573d-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d573d-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d573d-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d573d-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d573d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d573d-109">DESCRIPTION</span></span>
<span data-ttu-id="d573d-110">Командлет **restart-AzVM** перезапустит виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="d573d-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="d573d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d573d-111">EXAMPLES</span></span>

### <span data-ttu-id="d573d-112">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d573d-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d573d-113">Эта команда перезапускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d573d-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="d573d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d573d-114">PARAMETERS</span></span>

### <span data-ttu-id="d573d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d573d-115">-AsJob</span></span>
<span data-ttu-id="d573d-116">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="d573d-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d573d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d573d-117">-DefaultProfile</span></span>
<span data-ttu-id="d573d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d573d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d573d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d573d-119">-Id</span></span>
<span data-ttu-id="d573d-120">ИДЕНТИФИКАТОР виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d573d-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d573d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d573d-121">-Name</span></span>
<span data-ttu-id="d573d-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d573d-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d573d-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="d573d-123">-PerformMaintenance</span></span>
<span data-ttu-id="d573d-124">Для выполнения обслуживания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d573d-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d573d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d573d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d573d-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d573d-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d573d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d573d-127">-Confirm</span></span>
<span data-ttu-id="d573d-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d573d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d573d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d573d-129">-WhatIf</span></span>
<span data-ttu-id="d573d-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d573d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d573d-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d573d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d573d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d573d-132">CommonParameters</span></span>
<span data-ttu-id="d573d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d573d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d573d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d573d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d573d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d573d-135">INPUTS</span></span>

### <span data-ttu-id="d573d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d573d-136">System.String</span></span>

### <span data-ttu-id="d573d-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d573d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d573d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d573d-138">OUTPUTS</span></span>

### <span data-ttu-id="d573d-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d573d-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="d573d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d573d-140">NOTES</span></span>

## <span data-ttu-id="d573d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d573d-141">RELATED LINKS</span></span>

[<span data-ttu-id="d573d-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d573d-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d573d-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d573d-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d573d-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d573d-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d573d-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="d573d-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d573d-146">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="d573d-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d573d-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d573d-147">Update-AzVM</span></span>](./Update-AzVM.md)


