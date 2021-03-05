---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 152be66a2e1582d9f8377e09e250d3cf044c64db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010787"
---
# <span data-ttu-id="89811-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-101">Stop-AzVmss</span></span>

## <span data-ttu-id="89811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89811-102">SYNOPSIS</span></span>
<span data-ttu-id="89811-103">Остановка виртуальных машин или виртуальных машин в них.</span><span class="sxs-lookup"><span data-stu-id="89811-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="89811-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89811-104">SYNTAX</span></span>

### <span data-ttu-id="89811-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89811-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89811-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="89811-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89811-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89811-107">DESCRIPTION</span></span>
<span data-ttu-id="89811-108">Для остановки всех виртуальных машин в наборе виртуальных машин (VMSS) или набора виртуальных машин используется **cmdlet Stop-AzVmss.**</span><span class="sxs-lookup"><span data-stu-id="89811-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="89811-109">С помощью параметра *InstanceId* можно выбрать набор виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="89811-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="89811-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89811-110">EXAMPLES</span></span>

### <span data-ttu-id="89811-111">Пример 1. Остановка всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="89811-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="89811-112">Эта команда останавливает все виртуальные машины, которые относятся к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="89811-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="89811-113">Пример 2. Остановка определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="89811-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="89811-114">Эта команда останавливает определенный набор виртуальных машин, заданный массивом строки "ИД экземпляра", относимых к VMSS ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="89811-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="89811-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89811-115">PARAMETERS</span></span>

### <span data-ttu-id="89811-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89811-116">-AsJob</span></span>
<span data-ttu-id="89811-117">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89811-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="89811-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89811-118">-DefaultProfile</span></span>
<span data-ttu-id="89811-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89811-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89811-120">-Force</span><span class="sxs-lookup"><span data-stu-id="89811-120">-Force</span></span>
<span data-ttu-id="89811-121">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="89811-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89811-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="89811-122">-InstanceId</span></span>
<span data-ttu-id="89811-123">Указывает, что это строкового массива, а также коды экземпляров виртуальной машины, которые останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89811-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="89811-124">Например: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="89811-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="89811-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89811-125">-ResourceGroupName</span></span>
<span data-ttu-id="89811-126">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="89811-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="89811-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="89811-127">-SkipShutdown</span></span>
<span data-ttu-id="89811-128">Запрос на неявное завершение работы VM</span><span class="sxs-lookup"><span data-stu-id="89811-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89811-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="89811-129">-StayProvisioned</span></span>
<span data-ttu-id="89811-130">При этом виртуальная машинка будет вводиться в состояние "Остановлено".</span><span class="sxs-lookup"><span data-stu-id="89811-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="89811-131">Если не указано, виртуальная машинка будет вводить состояние остановленной сделки.</span><span class="sxs-lookup"><span data-stu-id="89811-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="89811-132">С пользователя по-прежнему взимается плата за ВТБ в остановленом состоянии, но не за ВИМ в состоянии остановленной сделки.</span><span class="sxs-lookup"><span data-stu-id="89811-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="89811-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="89811-133">-VMScaleSetName</span></span>
<span data-ttu-id="89811-134">Указывает имя виртуальных машин, для которых этот cmdlet останавливает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="89811-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="89811-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89811-135">-Confirm</span></span>
<span data-ttu-id="89811-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="89811-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89811-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89811-137">-WhatIf</span></span>
<span data-ttu-id="89811-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89811-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89811-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89811-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89811-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89811-140">CommonParameters</span></span>
<span data-ttu-id="89811-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89811-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89811-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89811-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89811-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89811-143">INPUTS</span></span>

### <span data-ttu-id="89811-144">System.String</span><span class="sxs-lookup"><span data-stu-id="89811-144">System.String</span></span>

### <span data-ttu-id="89811-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="89811-145">System.String[]</span></span>

## <span data-ttu-id="89811-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89811-146">OUTPUTS</span></span>

### <span data-ttu-id="89811-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="89811-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="89811-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89811-148">NOTES</span></span>

## <span data-ttu-id="89811-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89811-149">RELATED LINKS</span></span>

[<span data-ttu-id="89811-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="89811-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="89811-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="89811-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="89811-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="89811-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="89811-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="89811-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


