---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246774"
---
# <span data-ttu-id="6bf61-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-101">Start-AzVmss</span></span>

## <span data-ttu-id="6bf61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6bf61-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf61-103">Запускает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf61-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="6bf61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6bf61-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bf61-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bf61-105">DESCRIPTION</span></span>
<span data-ttu-id="6bf61-106">Командлет **Start-AzVmss** запускает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6bf61-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="6bf61-107">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6bf61-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="6bf61-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6bf61-108">EXAMPLES</span></span>

### <span data-ttu-id="6bf61-109">Пример 1: запуск определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="6bf61-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="6bf61-110">Эта команда запускает определенный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf61-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="6bf61-111">Пример 2: запуск всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="6bf61-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="6bf61-112">Эта команда запускает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf61-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6bf61-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6bf61-113">PARAMETERS</span></span>

### <span data-ttu-id="6bf61-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bf61-114">-AsJob</span></span>
<span data-ttu-id="6bf61-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6bf61-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6bf61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf61-116">-DefaultProfile</span></span>
<span data-ttu-id="6bf61-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bf61-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bf61-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6bf61-118">-InstanceId</span></span>
<span data-ttu-id="6bf61-119">Задает в качестве массива строк идентификатор или идентификаторы экземпляров, с которых начинается командлет.</span><span class="sxs-lookup"><span data-stu-id="6bf61-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="6bf61-120">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="6bf61-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="6bf61-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bf61-121">-ResourceGroupName</span></span>
<span data-ttu-id="6bf61-122">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="6bf61-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6bf61-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6bf61-123">-VMScaleSetName</span></span>
<span data-ttu-id="6bf61-124">Указывает имя VMSS, который запускается этим командлетом для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6bf61-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="6bf61-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bf61-125">-Confirm</span></span>
<span data-ttu-id="6bf61-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6bf61-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bf61-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf61-127">-WhatIf</span></span>
<span data-ttu-id="6bf61-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6bf61-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bf61-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6bf61-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bf61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf61-130">CommonParameters</span></span>
<span data-ttu-id="6bf61-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6bf61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf61-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bf61-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf61-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6bf61-133">INPUTS</span></span>

### <span data-ttu-id="6bf61-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6bf61-134">System.String</span></span>

### <span data-ttu-id="6bf61-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="6bf61-135">System.String[]</span></span>

## <span data-ttu-id="6bf61-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bf61-136">OUTPUTS</span></span>

### <span data-ttu-id="6bf61-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6bf61-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6bf61-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6bf61-138">NOTES</span></span>

## <span data-ttu-id="6bf61-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bf61-139">RELATED LINKS</span></span>

[<span data-ttu-id="6bf61-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="6bf61-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="6bf61-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6bf61-143">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="6bf61-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6bf61-145">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="6bf61-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6bf61-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


