---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568617"
---
# <span data-ttu-id="d4558-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="d4558-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4558-102">SYNOPSIS</span></span>
<span data-ttu-id="d4558-103">Останавливает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4558-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4558-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4558-104">SYNTAX</span></span>

### <span data-ttu-id="d4558-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4558-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4558-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d4558-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4558-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4558-107">DESCRIPTION</span></span>
<span data-ttu-id="d4558-108">Командлет **Stop-AzureRmVmss** останавливает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d4558-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="d4558-109">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d4558-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="d4558-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4558-110">EXAMPLES</span></span>

### <span data-ttu-id="d4558-111">Пример 1: остановка всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="d4558-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d4558-112">Эта команда останавливает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="d4558-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="d4558-113">Пример 2: остановка определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="d4558-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="d4558-114">Эта команда останавливает конкретный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="d4558-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d4558-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4558-115">PARAMETERS</span></span>

### <span data-ttu-id="d4558-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d4558-116">-Force</span></span>
<span data-ttu-id="d4558-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4558-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4558-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d4558-118">-InstanceId</span></span>
<span data-ttu-id="d4558-119">Задает в качестве строкового массива ИДЕНТИФИКАТОРы или идентификаторы экземпляров виртуальных машин, которые завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d4558-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="d4558-120">Например: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="d4558-120">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="d4558-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4558-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4558-122">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4558-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d4558-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="d4558-123">-StayProvisioned</span></span>
<span data-ttu-id="d4558-124">Если задано значение "остановлено", виртуальная машина будет введена в состояние Stopped.</span><span class="sxs-lookup"><span data-stu-id="d4558-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="d4558-125">Если этот элемент не указан, виртуальная машина будет переведена в состояние "остановлено".</span><span class="sxs-lookup"><span data-stu-id="d4558-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="d4558-126">Пользователь по-прежнему оплачивается для виртуальных машин в остановленном состоянии, но не для виртуальных машин в состоянии Stopped-освобождено.</span><span class="sxs-lookup"><span data-stu-id="d4558-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4558-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4558-127">-VMScaleSetName</span></span>
<span data-ttu-id="d4558-128">Указывает имя VMSS, для которого этот командлет останавливает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="d4558-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="d4558-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4558-129">-Confirm</span></span>
<span data-ttu-id="d4558-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4558-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4558-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4558-131">-WhatIf</span></span>
<span data-ttu-id="d4558-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4558-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4558-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4558-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4558-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4558-134">CommonParameters</span></span>
<span data-ttu-id="d4558-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4558-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4558-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4558-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4558-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4558-137">INPUTS</span></span>

### <span data-ttu-id="d4558-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="d4558-138">None</span></span>
<span data-ttu-id="d4558-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d4558-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4558-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4558-140">OUTPUTS</span></span>

## <span data-ttu-id="d4558-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4558-141">NOTES</span></span>

## <span data-ttu-id="d4558-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4558-142">RELATED LINKS</span></span>

[<span data-ttu-id="d4558-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="d4558-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d4558-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d4558-146">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="d4558-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="d4558-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="d4558-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4558-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


