---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: eca73d71d213b31c0bbc339708cc744b3bf64d2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963251"
---
# <span data-ttu-id="ab619-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab619-101">Restart-AzVM</span></span>

## <span data-ttu-id="ab619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab619-102">SYNOPSIS</span></span>
<span data-ttu-id="ab619-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="ab619-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ab619-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab619-104">SYNTAX</span></span>

### <span data-ttu-id="ab619-105">RestartResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab619-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab619-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab619-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab619-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab619-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab619-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab619-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab619-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab619-109">DESCRIPTION</span></span>
<span data-ttu-id="ab619-110">Для **перезапуска виртуальной** машины Azure будет перезапущена cmdlet Restart-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ab619-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ab619-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab619-111">EXAMPLES</span></span>

### <span data-ttu-id="ab619-112">Пример 1. Перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ab619-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ab619-113">Эта команда перезапустит виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ab619-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ab619-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab619-114">PARAMETERS</span></span>

### <span data-ttu-id="ab619-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab619-115">-AsJob</span></span>
<span data-ttu-id="ab619-116">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ab619-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ab619-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab619-117">-DefaultProfile</span></span>
<span data-ttu-id="ab619-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab619-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab619-119">-Id</span><span class="sxs-lookup"><span data-stu-id="ab619-119">-Id</span></span>
<span data-ttu-id="ab619-120">ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab619-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="ab619-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ab619-121">-Name</span></span>
<span data-ttu-id="ab619-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab619-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="ab619-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ab619-123">-NoWait</span></span>
<span data-ttu-id="ab619-124">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="ab619-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ab619-125">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="ab619-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ab619-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="ab619-126">-PerformMaintenance</span></span>
<span data-ttu-id="ab619-127">Для обслуживания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab619-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="ab619-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab619-128">-ResourceGroupName</span></span>
<span data-ttu-id="ab619-129">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab619-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ab619-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab619-130">-Confirm</span></span>
<span data-ttu-id="ab619-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab619-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab619-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab619-132">-WhatIf</span></span>
<span data-ttu-id="ab619-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab619-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab619-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ab619-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab619-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab619-135">CommonParameters</span></span>
<span data-ttu-id="ab619-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab619-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab619-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab619-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab619-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab619-138">INPUTS</span></span>

### <span data-ttu-id="ab619-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ab619-139">System.String</span></span>

### <span data-ttu-id="ab619-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab619-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab619-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab619-141">OUTPUTS</span></span>

### <span data-ttu-id="ab619-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ab619-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="ab619-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ab619-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ab619-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab619-144">NOTES</span></span>

## <span data-ttu-id="ab619-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab619-145">RELATED LINKS</span></span>

[<span data-ttu-id="ab619-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab619-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ab619-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab619-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="ab619-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab619-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="ab619-149">Start-AzvM</span><span class="sxs-lookup"><span data-stu-id="ab619-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="ab619-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab619-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="ab619-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab619-151">Update-AzVM</span></span>](./Update-AzVM.md)


