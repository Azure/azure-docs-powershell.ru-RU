---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 6669952330d82fc7c5dac8f564b34de7c896511c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910454"
---
# <span data-ttu-id="3c133-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-101">Stop-AzVmss</span></span>

## <span data-ttu-id="3c133-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c133-102">SYNOPSIS</span></span>
<span data-ttu-id="3c133-103">Останавливает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c133-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="3c133-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c133-104">SYNTAX</span></span>

### <span data-ttu-id="3c133-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c133-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c133-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3c133-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c133-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c133-107">DESCRIPTION</span></span>
<span data-ttu-id="3c133-108">Командлет **Stop-AzVmss** останавливает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="3c133-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="3c133-109">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="3c133-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="3c133-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c133-110">EXAMPLES</span></span>

### <span data-ttu-id="3c133-111">Пример 1: остановка всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="3c133-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="3c133-112">Эта команда останавливает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="3c133-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="3c133-113">Пример 2: остановка определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="3c133-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="3c133-114">Эта команда останавливает конкретный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="3c133-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="3c133-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c133-115">PARAMETERS</span></span>

### <span data-ttu-id="3c133-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c133-116">-AsJob</span></span>
<span data-ttu-id="3c133-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3c133-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c133-118">-DefaultProfile</span></span>
<span data-ttu-id="3c133-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c133-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3c133-120">-Force</span></span>
<span data-ttu-id="3c133-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c133-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3c133-122">-InstanceId</span></span>
<span data-ttu-id="3c133-123">Задает в качестве строкового массива ИДЕНТИФИКАТОРы или идентификаторы экземпляров виртуальных машин, которые завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3c133-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="3c133-124">Например: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="3c133-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c133-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c133-126">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="3c133-126">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="3c133-127">-StayProvisioned</span></span>
<span data-ttu-id="3c133-128">Если задано значение "остановлено", виртуальная машина будет введена в состояние Stopped.</span><span class="sxs-lookup"><span data-stu-id="3c133-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="3c133-129">Если этот элемент не указан, виртуальная машина будет переведена в состояние "остановлено".</span><span class="sxs-lookup"><span data-stu-id="3c133-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="3c133-130">Пользователь по-прежнему оплачивается для виртуальных машин в остановленном состоянии, но не для виртуальных машин в состоянии Stopped-освобождено.</span><span class="sxs-lookup"><span data-stu-id="3c133-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3c133-131">-VMScaleSetName</span></span>
<span data-ttu-id="3c133-132">Указывает имя VMSS, для которого этот командлет останавливает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="3c133-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c133-133">-Confirm</span></span>
<span data-ttu-id="3c133-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c133-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c133-135">-WhatIf</span></span>
<span data-ttu-id="3c133-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c133-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c133-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c133-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c133-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c133-138">CommonParameters</span></span>
<span data-ttu-id="3c133-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c133-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c133-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c133-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c133-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c133-141">INPUTS</span></span>

### <span data-ttu-id="3c133-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c133-142">None</span></span>
<span data-ttu-id="3c133-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3c133-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c133-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c133-144">OUTPUTS</span></span>

### <span data-ttu-id="3c133-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3c133-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3c133-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c133-146">NOTES</span></span>

## <span data-ttu-id="3c133-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c133-147">RELATED LINKS</span></span>

[<span data-ttu-id="3c133-148">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-148">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="3c133-149">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-149">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="3c133-150">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-150">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="3c133-151">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-151">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="3c133-152">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-152">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="3c133-153">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-153">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="3c133-154">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3c133-154">Update-AzVmss</span></span>](./Update-AzVmss.md)


