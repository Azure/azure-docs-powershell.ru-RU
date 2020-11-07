---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: d00a51a722fa03742c56387ee27faa4f6228ded7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731209"
---
# <span data-ttu-id="c2748-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-101">Stop-AzVmss</span></span>

## <span data-ttu-id="c2748-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2748-102">SYNOPSIS</span></span>
<span data-ttu-id="c2748-103">Останавливает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c2748-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="c2748-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2748-104">SYNTAX</span></span>

### <span data-ttu-id="c2748-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2748-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2748-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c2748-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2748-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2748-107">DESCRIPTION</span></span>
<span data-ttu-id="c2748-108">Командлет **Stop-AzVmss** останавливает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c2748-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c2748-109">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c2748-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c2748-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2748-110">EXAMPLES</span></span>

### <span data-ttu-id="c2748-111">Пример 1: остановка всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="c2748-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c2748-112">Эта команда останавливает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="c2748-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c2748-113">Пример 2: остановка определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="c2748-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="c2748-114">Эта команда останавливает конкретный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="c2748-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c2748-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2748-115">PARAMETERS</span></span>

### <span data-ttu-id="c2748-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2748-116">-AsJob</span></span>
<span data-ttu-id="c2748-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c2748-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c2748-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2748-118">-DefaultProfile</span></span>
<span data-ttu-id="c2748-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2748-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2748-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c2748-120">-Force</span></span>
<span data-ttu-id="c2748-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2748-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2748-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c2748-122">-InstanceId</span></span>
<span data-ttu-id="c2748-123">Задает в качестве строкового массива ИДЕНТИФИКАТОРы или идентификаторы экземпляров виртуальных машин, которые завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c2748-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="c2748-124">Например: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="c2748-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="c2748-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2748-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2748-126">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="c2748-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c2748-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="c2748-127">-StayProvisioned</span></span>
<span data-ttu-id="c2748-128">Если задано значение "остановлено", виртуальная машина будет введена в состояние Stopped.</span><span class="sxs-lookup"><span data-stu-id="c2748-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="c2748-129">Если этот элемент не указан, виртуальная машина будет переведена в состояние "остановлено".</span><span class="sxs-lookup"><span data-stu-id="c2748-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="c2748-130">Пользователь по-прежнему оплачивается для виртуальных машин в остановленном состоянии, но не для виртуальных машин в состоянии Stopped-освобождено.</span><span class="sxs-lookup"><span data-stu-id="c2748-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="c2748-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c2748-131">-VMScaleSetName</span></span>
<span data-ttu-id="c2748-132">Указывает имя VMSS, для которого этот командлет останавливает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="c2748-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="c2748-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2748-133">-Confirm</span></span>
<span data-ttu-id="c2748-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2748-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2748-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2748-135">-WhatIf</span></span>
<span data-ttu-id="c2748-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2748-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2748-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2748-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2748-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2748-138">CommonParameters</span></span>
<span data-ttu-id="c2748-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2748-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2748-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2748-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2748-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2748-141">INPUTS</span></span>

### <span data-ttu-id="c2748-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c2748-142">System.String</span></span>

### <span data-ttu-id="c2748-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="c2748-143">System.String[]</span></span>

## <span data-ttu-id="c2748-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2748-144">OUTPUTS</span></span>

### <span data-ttu-id="c2748-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c2748-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c2748-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2748-146">NOTES</span></span>

## <span data-ttu-id="c2748-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2748-147">RELATED LINKS</span></span>

[<span data-ttu-id="c2748-148">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-148">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="c2748-149">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-149">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="c2748-150">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-150">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="c2748-151">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-151">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="c2748-152">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-152">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="c2748-153">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-153">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="c2748-154">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c2748-154">Update-AzVmss</span></span>](./Update-AzVmss.md)


