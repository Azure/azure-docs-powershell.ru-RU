---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394151"
---
# <span data-ttu-id="92776-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="92776-101">Restart-AzVM</span></span>

## <span data-ttu-id="92776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92776-102">SYNOPSIS</span></span>
<span data-ttu-id="92776-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="92776-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="92776-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92776-104">SYNTAX</span></span>

### <span data-ttu-id="92776-105">RestartResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92776-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92776-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="92776-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92776-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="92776-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92776-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="92776-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92776-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92776-109">DESCRIPTION</span></span>
<span data-ttu-id="92776-110">С **его использованием можно перезапустить** виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="92776-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="92776-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92776-111">EXAMPLES</span></span>

### <span data-ttu-id="92776-112">Пример 1. Перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="92776-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="92776-113">Эта команда перезапустит виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="92776-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="92776-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92776-114">PARAMETERS</span></span>

### <span data-ttu-id="92776-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92776-115">-AsJob</span></span>
<span data-ttu-id="92776-116">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="92776-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="92776-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92776-117">-DefaultProfile</span></span>
<span data-ttu-id="92776-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92776-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92776-119">-Id</span><span class="sxs-lookup"><span data-stu-id="92776-119">-Id</span></span>
<span data-ttu-id="92776-120">ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92776-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="92776-121">-Name</span><span class="sxs-lookup"><span data-stu-id="92776-121">-Name</span></span>
<span data-ttu-id="92776-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92776-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="92776-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92776-123">-NoWait</span></span>
<span data-ttu-id="92776-124">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="92776-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="92776-125">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="92776-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="92776-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="92776-126">-PerformMaintenance</span></span>
<span data-ttu-id="92776-127">Для обслуживания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92776-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="92776-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92776-128">-ResourceGroupName</span></span>
<span data-ttu-id="92776-129">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92776-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="92776-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92776-130">-Confirm</span></span>
<span data-ttu-id="92776-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="92776-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92776-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92776-132">-WhatIf</span></span>
<span data-ttu-id="92776-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92776-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92776-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92776-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92776-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92776-135">CommonParameters</span></span>
<span data-ttu-id="92776-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92776-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92776-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92776-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92776-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92776-138">INPUTS</span></span>

### <span data-ttu-id="92776-139">System.String</span><span class="sxs-lookup"><span data-stu-id="92776-139">System.String</span></span>

### <span data-ttu-id="92776-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92776-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92776-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92776-141">OUTPUTS</span></span>

### <span data-ttu-id="92776-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="92776-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="92776-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="92776-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="92776-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92776-144">NOTES</span></span>

## <span data-ttu-id="92776-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92776-145">RELATED LINKS</span></span>

[<span data-ttu-id="92776-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="92776-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="92776-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="92776-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="92776-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="92776-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="92776-149">Start-AzvM</span><span class="sxs-lookup"><span data-stu-id="92776-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="92776-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="92776-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="92776-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="92776-151">Update-AzVM</span></span>](./Update-AzVM.md)


