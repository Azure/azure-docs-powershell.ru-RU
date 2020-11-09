---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 23bbd1f8698de63477da28c84de1aa531366ee26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246787"
---
# <span data-ttu-id="fa553-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-101">Set-AzVmss</span></span>

## <span data-ttu-id="fa553-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa553-102">SYNOPSIS</span></span>
<span data-ttu-id="fa553-103">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa553-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="fa553-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa553-104">SYNTAX</span></span>

### <span data-ttu-id="fa553-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa553-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa553-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fa553-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa553-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="fa553-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa553-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="fa553-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa553-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa553-109">DESCRIPTION</span></span>
<span data-ttu-id="fa553-110">Командлет **Set-AzVmss** задает определенные действия в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fa553-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fa553-111">Единственным действием, поддерживаемым этим командлетом, является переобраз.</span><span class="sxs-lookup"><span data-stu-id="fa553-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="fa553-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa553-112">EXAMPLES</span></span>

### <span data-ttu-id="fa553-113">Пример 1: переизображение VMSS</span><span class="sxs-lookup"><span data-stu-id="fa553-113">Example 1: Reimage a VMSS</span></span>
```powershell
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="fa553-114">Эта команда позволяет переобразировать VMSS с именем ContosoVMSS, которое принадлежит группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="fa553-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

### <span data-ttu-id="fa553-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa553-115">Example 2</span></span>

<span data-ttu-id="fa553-116">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa553-116">Sets specific actions on a specified VMSS.</span></span> <span data-ttu-id="fa553-117">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="fa553-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVmss -ReimageAll -ResourceGroupName 'ContosoGroup' -VMScaleSetName 'ContosoVMSS'
```

## <span data-ttu-id="fa553-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa553-118">PARAMETERS</span></span>

### <span data-ttu-id="fa553-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa553-119">-AsJob</span></span>
<span data-ttu-id="fa553-120">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fa553-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fa553-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa553-121">-DefaultProfile</span></span>
<span data-ttu-id="fa553-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa553-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa553-123">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fa553-123">-InstanceId</span></span>
<span data-ttu-id="fa553-124">Идентификатор экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fa553-124">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="fa553-125">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="fa553-125">-PerformMaintenance</span></span>
<span data-ttu-id="fa553-126">Указывает на то, что этот командлет выполняет обслуживание одной или нескольких виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa553-126">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="fa553-127">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="fa553-127">-Redeploy</span></span>
<span data-ttu-id="fa553-128">Указывает на то, что командлет повторно развертывает одну или несколько виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa553-128">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="fa553-129">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="fa553-129">-Reimage</span></span>
<span data-ttu-id="fa553-130">Указывает на то, что командлет переобразует VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa553-130">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="fa553-131">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="fa553-131">-ReimageAll</span></span>
<span data-ttu-id="fa553-132">Указывает на то, что командлет переобразовать все диски в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa553-132">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="fa553-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa553-133">-ResourceGroupName</span></span>
<span data-ttu-id="fa553-134">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="fa553-134">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="fa553-135">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="fa553-135">-TempDisk</span></span>
<span data-ttu-id="fa553-136">Указывает, следует ли переобразировать временный диск.</span><span class="sxs-lookup"><span data-stu-id="fa553-136">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="fa553-137">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fa553-137">-VMScaleSetName</span></span>
<span data-ttu-id="fa553-138">Форель имя VMSS, для которого этот командлет задает действия.</span><span class="sxs-lookup"><span data-stu-id="fa553-138">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="fa553-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa553-139">-Confirm</span></span>
<span data-ttu-id="fa553-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa553-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa553-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa553-141">-WhatIf</span></span>
<span data-ttu-id="fa553-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa553-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa553-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa553-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa553-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa553-144">CommonParameters</span></span>
<span data-ttu-id="fa553-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa553-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa553-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa553-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa553-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa553-147">INPUTS</span></span>

### <span data-ttu-id="fa553-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fa553-148">System.String</span></span>

### <span data-ttu-id="fa553-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="fa553-149">System.String[]</span></span>

## <span data-ttu-id="fa553-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa553-150">OUTPUTS</span></span>

### <span data-ttu-id="fa553-151">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fa553-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fa553-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa553-152">NOTES</span></span>

## <span data-ttu-id="fa553-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa553-153">RELATED LINKS</span></span>

[<span data-ttu-id="fa553-154">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-154">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="fa553-155">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-155">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="fa553-156">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-156">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fa553-157">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-157">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fa553-158">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-158">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fa553-159">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-159">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fa553-160">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fa553-160">Update-AzVmss</span></span>](./Update-AzVmss.md)

