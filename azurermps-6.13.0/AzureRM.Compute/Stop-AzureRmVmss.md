---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 206ce916e1a170bbcdf11f791a4610dd5d2172af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734671"
---
# <span data-ttu-id="0a302-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="0a302-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a302-102">SYNOPSIS</span></span>
<span data-ttu-id="0a302-103">Останавливает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a302-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a302-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a302-104">SYNTAX</span></span>

### <span data-ttu-id="0a302-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a302-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a302-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0a302-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a302-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a302-107">DESCRIPTION</span></span>
<span data-ttu-id="0a302-108">Командлет **Stop-AzureRmVmss** останавливает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0a302-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="0a302-109">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0a302-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="0a302-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a302-110">EXAMPLES</span></span>

### <span data-ttu-id="0a302-111">Пример 1: остановка всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="0a302-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="0a302-112">Эта команда останавливает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="0a302-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="0a302-113">Пример 2: остановка определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="0a302-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="0a302-114">Эта команда останавливает конкретный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="0a302-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="0a302-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a302-115">PARAMETERS</span></span>

### <span data-ttu-id="0a302-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a302-116">-AsJob</span></span>
<span data-ttu-id="0a302-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0a302-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0a302-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a302-118">-DefaultProfile</span></span>
<span data-ttu-id="0a302-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a302-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a302-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0a302-120">-Force</span></span>
<span data-ttu-id="0a302-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a302-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a302-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0a302-122">-InstanceId</span></span>
<span data-ttu-id="0a302-123">Задает в качестве строкового массива ИДЕНТИФИКАТОРы или идентификаторы экземпляров виртуальных машин, которые завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0a302-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="0a302-124">Например: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="0a302-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="0a302-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a302-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a302-126">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="0a302-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="0a302-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="0a302-127">-StayProvisioned</span></span>
<span data-ttu-id="0a302-128">Если задано значение "остановлено", виртуальная машина будет введена в состояние Stopped.</span><span class="sxs-lookup"><span data-stu-id="0a302-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="0a302-129">Если этот элемент не указан, виртуальная машина будет переведена в состояние "остановлено".</span><span class="sxs-lookup"><span data-stu-id="0a302-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="0a302-130">Пользователь по-прежнему оплачивается для виртуальных машин в остановленном состоянии, но не для виртуальных машин в состоянии Stopped-освобождено.</span><span class="sxs-lookup"><span data-stu-id="0a302-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="0a302-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0a302-131">-VMScaleSetName</span></span>
<span data-ttu-id="0a302-132">Указывает имя VMSS, для которого этот командлет останавливает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="0a302-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="0a302-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a302-133">-Confirm</span></span>
<span data-ttu-id="0a302-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a302-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a302-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a302-135">-WhatIf</span></span>
<span data-ttu-id="0a302-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a302-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a302-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a302-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a302-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a302-138">CommonParameters</span></span>
<span data-ttu-id="0a302-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a302-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a302-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a302-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a302-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a302-141">INPUTS</span></span>

### <span data-ttu-id="0a302-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0a302-142">System.String</span></span>

### <span data-ttu-id="0a302-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="0a302-143">System.String[]</span></span>

## <span data-ttu-id="0a302-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a302-144">OUTPUTS</span></span>

### <span data-ttu-id="0a302-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0a302-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0a302-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a302-146">NOTES</span></span>

## <span data-ttu-id="0a302-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a302-147">RELATED LINKS</span></span>

[<span data-ttu-id="0a302-148">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-148">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="0a302-149">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-149">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="0a302-150">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-150">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="0a302-151">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-151">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="0a302-152">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-152">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="0a302-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="0a302-154">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0a302-154">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


