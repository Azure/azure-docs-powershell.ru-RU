---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560996"
---
# <span data-ttu-id="fbd2e-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="fbd2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbd2e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd2e-103">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbd2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbd2e-104">SYNTAX</span></span>

### <span data-ttu-id="fbd2e-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbd2e-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbd2e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fbd2e-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbd2e-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="fbd2e-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbd2e-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="fbd2e-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbd2e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbd2e-109">DESCRIPTION</span></span>
<span data-ttu-id="fbd2e-110">Командлет **Set-AzureRmVmss** задает определенные действия в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fbd2e-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fbd2e-111">Единственным действием, поддерживаемым этим командлетом, является переобраз.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="fbd2e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbd2e-112">EXAMPLES</span></span>

### <span data-ttu-id="fbd2e-113">Пример 1: переизображение VMSS</span><span class="sxs-lookup"><span data-stu-id="fbd2e-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="fbd2e-114">Эта команда позволяет переобразировать VMSS с именем ContosoVMSS, которое принадлежит группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="fbd2e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbd2e-115">PARAMETERS</span></span>

### <span data-ttu-id="fbd2e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbd2e-116">-AsJob</span></span>
<span data-ttu-id="fbd2e-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fbd2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd2e-118">-DefaultProfile</span></span>
<span data-ttu-id="fbd2e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2e-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fbd2e-120">-InstanceId</span></span>
<span data-ttu-id="fbd2e-121">Идентификатор экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2e-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="fbd2e-122">-PerformMaintenance</span></span>
<span data-ttu-id="fbd2e-123">Указывает на то, что этот командлет выполняет обслуживание одной или нескольких виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="fbd2e-124">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="fbd2e-124">-Redeploy</span></span>
<span data-ttu-id="fbd2e-125">Указывает на то, что командлет повторно развертывает одну или несколько виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="fbd2e-126">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="fbd2e-126">-Reimage</span></span>
<span data-ttu-id="fbd2e-127">Указывает на то, что командлет переобразует VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="fbd2e-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="fbd2e-128">-ReimageAll</span></span>
<span data-ttu-id="fbd2e-129">Указывает на то, что командлет переобразовать все диски в VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="fbd2e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd2e-130">-ResourceGroupName</span></span>
<span data-ttu-id="fbd2e-131">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2e-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fbd2e-132">-VMScaleSetName</span></span>
<span data-ttu-id="fbd2e-133">Форель имя VMSS, для которого этот командлет задает действия.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbd2e-134">-Confirm</span></span>
<span data-ttu-id="fbd2e-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbd2e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbd2e-136">-WhatIf</span></span>
<span data-ttu-id="fbd2e-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbd2e-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbd2e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd2e-139">CommonParameters</span></span>
<span data-ttu-id="fbd2e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd2e-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbd2e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd2e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbd2e-142">INPUTS</span></span>

### <span data-ttu-id="fbd2e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fbd2e-143">System.String</span></span>

### <span data-ttu-id="fbd2e-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="fbd2e-144">System.String[]</span></span>

## <span data-ttu-id="fbd2e-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbd2e-145">OUTPUTS</span></span>

### <span data-ttu-id="fbd2e-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fbd2e-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fbd2e-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbd2e-147">NOTES</span></span>

## <span data-ttu-id="fbd2e-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbd2e-148">RELATED LINKS</span></span>

[<span data-ttu-id="fbd2e-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="fbd2e-150">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="fbd2e-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="fbd2e-152">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="fbd2e-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="fbd2e-154">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="fbd2e-155">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fbd2e-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


