---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243102"
---
# <span data-ttu-id="4bdb7-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-101">Remove-AzVmss</span></span>

## <span data-ttu-id="4bdb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bdb7-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdb7-103">Удаление VMSS или виртуальной машины, которая находится в VMSS.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="4bdb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bdb7-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bdb7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bdb7-105">DESCRIPTION</span></span>
<span data-ttu-id="4bdb7-106">Командлет **Remove-AzVmss** удаляет из Azure (VMSS) установленный параметр "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="4bdb7-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="4bdb7-107">Этот командлет также можно использовать для удаления определенной виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="4bdb7-108">Вы можете использовать параметр *InstanceId* для удаления определенной виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="4bdb7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bdb7-109">EXAMPLES</span></span>

### <span data-ttu-id="4bdb7-110">Пример 1: удаление VMSS</span><span class="sxs-lookup"><span data-stu-id="4bdb7-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="4bdb7-111">Эта команда удаляет VMSS с именем VMScaleSet001, который относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="4bdb7-112">Пример 2: Удаление виртуальной машины из VMSS</span><span class="sxs-lookup"><span data-stu-id="4bdb7-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="4bdb7-113">Эта команда удаляет виртуальную машину с ИДЕНТИФИКАТОРом 3 из VMSS с именем VMScaleSet002, которая относится к группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="4bdb7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bdb7-114">PARAMETERS</span></span>

### <span data-ttu-id="4bdb7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bdb7-115">-AsJob</span></span>
<span data-ttu-id="4bdb7-116">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4bdb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdb7-117">-DefaultProfile</span></span>
<span data-ttu-id="4bdb7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bdb7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4bdb7-119">-Force</span></span>
<span data-ttu-id="4bdb7-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bdb7-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4bdb7-121">-InstanceId</span></span>
<span data-ttu-id="4bdb7-122">Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо запустить.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="4bdb7-123">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="4bdb7-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="4bdb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="4bdb7-125">Указывает имя группы ресурсов, к которой относится VMSS.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="4bdb7-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4bdb7-126">-VMScaleSetName</span></span>
<span data-ttu-id="4bdb7-127">Форель имя VMSS, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="4bdb7-128">Если вы укажете параметр *InstanceId* , командлет удалит указанную виртуальную машину из VMSS с именем, указанным в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="4bdb7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bdb7-129">-Confirm</span></span>
<span data-ttu-id="4bdb7-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdb7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdb7-131">-WhatIf</span></span>
<span data-ttu-id="4bdb7-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bdb7-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdb7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdb7-134">CommonParameters</span></span>
<span data-ttu-id="4bdb7-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bdb7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdb7-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bdb7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdb7-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bdb7-137">INPUTS</span></span>

### <span data-ttu-id="4bdb7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4bdb7-138">System.String</span></span>

### <span data-ttu-id="4bdb7-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="4bdb7-139">System.String[]</span></span>

## <span data-ttu-id="4bdb7-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bdb7-140">OUTPUTS</span></span>

### <span data-ttu-id="4bdb7-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4bdb7-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4bdb7-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bdb7-142">NOTES</span></span>

## <span data-ttu-id="4bdb7-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bdb7-143">RELATED LINKS</span></span>

[<span data-ttu-id="4bdb7-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4bdb7-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4bdb7-146">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4bdb7-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4bdb7-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4bdb7-149">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="4bdb7-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bdb7-150">Update-AzVmss</span></span>](./Update-AzVmss.md)

