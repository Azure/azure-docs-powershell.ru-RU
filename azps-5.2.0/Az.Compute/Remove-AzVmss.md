---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408055"
---
# <span data-ttu-id="75da9-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-101">Remove-AzVmss</span></span>

## <span data-ttu-id="75da9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75da9-102">SYNOPSIS</span></span>
<span data-ttu-id="75da9-103">Удаляет VMSS или виртуальную машину, которая находится в VMSS.</span><span class="sxs-lookup"><span data-stu-id="75da9-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="75da9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75da9-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75da9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75da9-105">DESCRIPTION</span></span>
<span data-ttu-id="75da9-106">При этом из Azure **удаляется** набор масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="75da9-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="75da9-107">Этот cmdlet также можно использовать для удаления определенной виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="75da9-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="75da9-108">С помощью параметра *InstanceId* можно удалить определенную виртуальную машину внутри VMSS.</span><span class="sxs-lookup"><span data-stu-id="75da9-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="75da9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75da9-109">EXAMPLES</span></span>

### <span data-ttu-id="75da9-110">Пример 1. Удаление VMSS</span><span class="sxs-lookup"><span data-stu-id="75da9-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="75da9-111">Эта команда удаляет VMSS С именем VMScaleSet001, который принадлежит к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="75da9-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="75da9-112">Пример 2. Удаление виртуальной машины из VMSS</span><span class="sxs-lookup"><span data-stu-id="75da9-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="75da9-113">Эта команда удаляет виртуальную машину с ИД экземпляра 3 из VMSS С именем VMScaleSet002, который принадлежит группе ресурсов "Группа002".</span><span class="sxs-lookup"><span data-stu-id="75da9-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="75da9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75da9-114">PARAMETERS</span></span>

### <span data-ttu-id="75da9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75da9-115">-AsJob</span></span>
<span data-ttu-id="75da9-116">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="75da9-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="75da9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75da9-117">-DefaultProfile</span></span>
<span data-ttu-id="75da9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75da9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75da9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="75da9-119">-Force</span></span>
<span data-ttu-id="75da9-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="75da9-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75da9-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="75da9-121">-InstanceId</span></span>
<span data-ttu-id="75da9-122">Указывает в качестве строки массива ИД в экземпляров, которые нужно начать.</span><span class="sxs-lookup"><span data-stu-id="75da9-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="75da9-123">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="75da9-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="75da9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75da9-124">-ResourceGroupName</span></span>
<span data-ttu-id="75da9-125">Имя группы ресурсов, к которой относится VMSS.</span><span class="sxs-lookup"><span data-stu-id="75da9-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="75da9-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="75da9-126">-VMScaleSetName</span></span>
<span data-ttu-id="75da9-127">Вид имени VMSS, удаляемого этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75da9-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="75da9-128">При указании *параметра InstanceId* указанный виртуальный компьютер удаляется из VMSS, именуемого этим параметром.</span><span class="sxs-lookup"><span data-stu-id="75da9-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="75da9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75da9-129">-Confirm</span></span>
<span data-ttu-id="75da9-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75da9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75da9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75da9-131">-WhatIf</span></span>
<span data-ttu-id="75da9-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75da9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75da9-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="75da9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75da9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75da9-134">CommonParameters</span></span>
<span data-ttu-id="75da9-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75da9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75da9-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75da9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75da9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75da9-137">INPUTS</span></span>

### <span data-ttu-id="75da9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="75da9-138">System.String</span></span>

### <span data-ttu-id="75da9-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="75da9-139">System.String[]</span></span>

## <span data-ttu-id="75da9-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75da9-140">OUTPUTS</span></span>

### <span data-ttu-id="75da9-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="75da9-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="75da9-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75da9-142">NOTES</span></span>

## <span data-ttu-id="75da9-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75da9-143">RELATED LINKS</span></span>

[<span data-ttu-id="75da9-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="75da9-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="75da9-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="75da9-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="75da9-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="75da9-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="75da9-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="75da9-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


