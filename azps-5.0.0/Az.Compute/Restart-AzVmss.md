---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: c686eec33a2f4a9f972acbdb7261f86fc45a6fa1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245607"
---
# <span data-ttu-id="65782-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-101">Restart-AzVmss</span></span>

## <span data-ttu-id="65782-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65782-102">SYNOPSIS</span></span>
<span data-ttu-id="65782-103">Перезапуск VMSS или виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="65782-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="65782-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65782-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65782-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65782-105">DESCRIPTION</span></span>
<span data-ttu-id="65782-106">Командлет **restarting-AzVmss** перезапустит установленный для виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="65782-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="65782-107">Этот командлет также можно использовать для перезапуска определенной виртуальной машины внутри VMSS с помощью параметра *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="65782-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="65782-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65782-108">EXAMPLES</span></span>

### <span data-ttu-id="65782-109">Пример 1: перезапуск VMSS</span><span class="sxs-lookup"><span data-stu-id="65782-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="65782-110">Эта команда перезапускает VMSS с именем VMSS001, который относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="65782-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="65782-111">Пример 2: перезагрузка определенной виртуальной машины в VMSS</span><span class="sxs-lookup"><span data-stu-id="65782-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="65782-112">Эта команда перезапускает виртуальную машину с ИДЕНТИФИКАТОРом 1 в VMSS с именем VMSS001, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="65782-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="65782-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65782-113">PARAMETERS</span></span>

### <span data-ttu-id="65782-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65782-114">-AsJob</span></span>
<span data-ttu-id="65782-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="65782-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="65782-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65782-116">-DefaultProfile</span></span>
<span data-ttu-id="65782-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65782-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65782-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="65782-118">-InstanceId</span></span>
<span data-ttu-id="65782-119">Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="65782-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="65782-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65782-120">-ResourceGroupName</span></span>
<span data-ttu-id="65782-121">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="65782-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="65782-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="65782-122">-VMScaleSetName</span></span>
<span data-ttu-id="65782-123">Форель имя VMSS, перезапускаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="65782-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="65782-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65782-124">-Confirm</span></span>
<span data-ttu-id="65782-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65782-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65782-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65782-126">-WhatIf</span></span>
<span data-ttu-id="65782-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65782-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65782-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65782-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65782-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65782-129">CommonParameters</span></span>
<span data-ttu-id="65782-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65782-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65782-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65782-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65782-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65782-132">INPUTS</span></span>

### <span data-ttu-id="65782-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65782-133">System.String</span></span>

### <span data-ttu-id="65782-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="65782-134">System.String[]</span></span>

## <span data-ttu-id="65782-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65782-135">OUTPUTS</span></span>

### <span data-ttu-id="65782-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="65782-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="65782-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="65782-137">NOTES</span></span>

## <span data-ttu-id="65782-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65782-138">RELATED LINKS</span></span>

[<span data-ttu-id="65782-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="65782-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="65782-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="65782-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="65782-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="65782-144">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="65782-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65782-145">Update-AzVmss</span></span>](./Update-AzVmss.md)

