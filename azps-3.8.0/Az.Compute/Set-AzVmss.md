---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 623ebc278b2903fb0563c7ea196bd6123f495388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074621"
---
# <span data-ttu-id="8e7c0-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-101">Set-AzVmss</span></span>

## <span data-ttu-id="8e7c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7c0-103">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="8e7c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e7c0-104">SYNTAX</span></span>

### <span data-ttu-id="8e7c0-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e7c0-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7c0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8e7c0-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7c0-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="8e7c0-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e7c0-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="8e7c0-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e7c0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e7c0-109">DESCRIPTION</span></span>
<span data-ttu-id="8e7c0-110">Командлет **Set-AzVmss** задает определенные действия в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8e7c0-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8e7c0-111">Единственным действием, поддерживаемым этим командлетом, является переобраз.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="8e7c0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e7c0-112">EXAMPLES</span></span>

### <span data-ttu-id="8e7c0-113">Пример 1: переизображение VMSS</span><span class="sxs-lookup"><span data-stu-id="8e7c0-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="8e7c0-114">Эта команда позволяет переобразировать VMSS с именем ContosoVMSS, которое принадлежит группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="8e7c0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e7c0-115">PARAMETERS</span></span>

### <span data-ttu-id="8e7c0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e7c0-116">-AsJob</span></span>
<span data-ttu-id="8e7c0-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8e7c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7c0-118">-DefaultProfile</span></span>
<span data-ttu-id="8e7c0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e7c0-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8e7c0-120">-InstanceId</span></span>
<span data-ttu-id="8e7c0-121">Идентификатор экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="8e7c0-122">-PerformMaintenance</span></span>
<span data-ttu-id="8e7c0-123">Указывает на то, что этот командлет выполняет обслуживание одной или нескольких виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-124">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="8e7c0-124">-Redeploy</span></span>
<span data-ttu-id="8e7c0-125">Указывает на то, что командлет повторно развертывает одну или несколько виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-126">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="8e7c0-126">-Reimage</span></span>
<span data-ttu-id="8e7c0-127">Указывает на то, что командлет переобразует VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="8e7c0-128">-ReimageAll</span></span>
<span data-ttu-id="8e7c0-129">Указывает на то, что командлет переобразовать все диски в VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7c0-130">-ResourceGroupName</span></span>
<span data-ttu-id="8e7c0-131">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="8e7c0-132">-TempDisk</span></span>
<span data-ttu-id="8e7c0-133">Указывает, следует ли переобразировать временный диск.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8e7c0-134">-VMScaleSetName</span></span>
<span data-ttu-id="8e7c0-135">Форель имя VMSS, для которого этот командлет задает действия.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7c0-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e7c0-136">-Confirm</span></span>
<span data-ttu-id="8e7c0-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7c0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7c0-138">-WhatIf</span></span>
<span data-ttu-id="8e7c0-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e7c0-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e7c0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7c0-141">CommonParameters</span></span>
<span data-ttu-id="8e7c0-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e7c0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7c0-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e7c0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7c0-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e7c0-144">INPUTS</span></span>

### <span data-ttu-id="8e7c0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8e7c0-145">System.String</span></span>

### <span data-ttu-id="8e7c0-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="8e7c0-146">System.String[]</span></span>

## <span data-ttu-id="8e7c0-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e7c0-147">OUTPUTS</span></span>

### <span data-ttu-id="8e7c0-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8e7c0-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8e7c0-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e7c0-149">NOTES</span></span>

## <span data-ttu-id="8e7c0-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e7c0-150">RELATED LINKS</span></span>

[<span data-ttu-id="8e7c0-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="8e7c0-152">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="8e7c0-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="8e7c0-154">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="8e7c0-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="8e7c0-156">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="8e7c0-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8e7c0-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


