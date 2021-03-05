---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 2ff37cec23499afb0a0bb14069dc4e694f4440f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971432"
---
# <span data-ttu-id="7f450-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-101">Start-AzVmss</span></span>

## <span data-ttu-id="7f450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f450-102">SYNOPSIS</span></span>
<span data-ttu-id="7f450-103">Запускает VMSS или набор виртуальных машин в них.</span><span class="sxs-lookup"><span data-stu-id="7f450-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="7f450-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f450-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f450-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f450-105">DESCRIPTION</span></span>
<span data-ttu-id="7f450-106">Для **запуска всех виртуальных** машин в наборе масштаба виртуальных машин (VMSS) или набора виртуальных машин запускается этот набор.</span><span class="sxs-lookup"><span data-stu-id="7f450-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="7f450-107">С помощью параметра *InstanceId* можно выбрать набор виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7f450-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="7f450-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f450-108">EXAMPLES</span></span>

### <span data-ttu-id="7f450-109">Пример 1. Запуск определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="7f450-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="7f450-110">Эта команда запускает набор виртуальных машин, заданный массивом строки "ИД экземпляра", относимых к VMSS ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="7f450-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="7f450-111">Пример 2. Запуск всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="7f450-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="7f450-112">Эта команда запускает все виртуальные машины, которые относятся к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="7f450-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="7f450-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f450-113">PARAMETERS</span></span>

### <span data-ttu-id="7f450-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f450-114">-AsJob</span></span>
<span data-ttu-id="7f450-115">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7f450-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f450-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f450-116">-DefaultProfile</span></span>
<span data-ttu-id="7f450-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f450-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f450-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="7f450-118">-InstanceId</span></span>
<span data-ttu-id="7f450-119">Указывает в качестве строкового массива коды экземпляров, которые запускается в этом наборе.</span><span class="sxs-lookup"><span data-stu-id="7f450-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="7f450-120">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="7f450-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="7f450-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f450-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f450-122">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="7f450-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="7f450-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7f450-123">-VMScaleSetName</span></span>
<span data-ttu-id="7f450-124">Указывает имя VMSS, с которого этот cmdlet запускает виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="7f450-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="7f450-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f450-125">-Confirm</span></span>
<span data-ttu-id="7f450-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f450-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f450-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f450-127">-WhatIf</span></span>
<span data-ttu-id="7f450-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f450-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f450-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f450-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f450-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f450-130">CommonParameters</span></span>
<span data-ttu-id="7f450-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f450-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f450-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f450-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f450-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f450-133">INPUTS</span></span>

### <span data-ttu-id="7f450-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7f450-134">System.String</span></span>

### <span data-ttu-id="7f450-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7f450-135">System.String[]</span></span>

## <span data-ttu-id="7f450-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f450-136">OUTPUTS</span></span>

### <span data-ttu-id="7f450-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7f450-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7f450-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f450-138">NOTES</span></span>

## <span data-ttu-id="7f450-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f450-139">RELATED LINKS</span></span>

[<span data-ttu-id="7f450-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="7f450-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="7f450-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="7f450-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="7f450-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="7f450-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="7f450-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7f450-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


