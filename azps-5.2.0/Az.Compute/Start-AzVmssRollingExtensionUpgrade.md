---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402615"
---
# <span data-ttu-id="6a35f-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="6a35f-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="6a35f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a35f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a35f-103">Этот cmdlet запускает развертывание обновления для всех расширений с заданным набором масштаба виртуальной машины до последней доступной версии.</span><span class="sxs-lookup"><span data-stu-id="6a35f-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="6a35f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a35f-104">SYNTAX</span></span>

### <span data-ttu-id="6a35f-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="6a35f-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a35f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6a35f-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a35f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a35f-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a35f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a35f-108">DESCRIPTION</span></span>
<span data-ttu-id="6a35f-109">Запускает развертывание обновления для перемещения всех расширений в масштабе виртуальной машины до последней доступной версии.</span><span class="sxs-lookup"><span data-stu-id="6a35f-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="6a35f-110">Расширения, которые уже работают с последней доступной версией, не затронуты.</span><span class="sxs-lookup"><span data-stu-id="6a35f-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="6a35f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a35f-111">EXAMPLES</span></span>

### <span data-ttu-id="6a35f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a35f-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="6a35f-113">В этом примере набор масштаба VM получает "MyVmssName" и добавляет к этому данной шкале расширение.</span><span class="sxs-lookup"><span data-stu-id="6a35f-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="6a35f-114">Конечная команда выполняет процесс обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="6a35f-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="6a35f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a35f-115">PARAMETERS</span></span>

### <span data-ttu-id="6a35f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a35f-116">-AsJob</span></span>
<span data-ttu-id="6a35f-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6a35f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a35f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a35f-118">-DefaultProfile</span></span>
<span data-ttu-id="6a35f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a35f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a35f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a35f-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a35f-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a35f-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a35f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a35f-122">-ResourceId</span></span>
<span data-ttu-id="6a35f-123">ИД ресурса объекта набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6a35f-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a35f-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6a35f-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6a35f-125">Объект набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6a35f-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a35f-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6a35f-126">-VMScaleSetName</span></span>
<span data-ttu-id="6a35f-127">Имя набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="6a35f-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a35f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a35f-128">-Confirm</span></span>
<span data-ttu-id="6a35f-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a35f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a35f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a35f-130">-WhatIf</span></span>
<span data-ttu-id="6a35f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a35f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a35f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a35f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a35f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a35f-133">CommonParameters</span></span>
<span data-ttu-id="6a35f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a35f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a35f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a35f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a35f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a35f-136">INPUTS</span></span>

### <span data-ttu-id="6a35f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6a35f-137">System.String</span></span>

### <span data-ttu-id="6a35f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="6a35f-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6a35f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a35f-139">OUTPUTS</span></span>

### <span data-ttu-id="6a35f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6a35f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6a35f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a35f-141">NOTES</span></span>

## <span data-ttu-id="6a35f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a35f-142">RELATED LINKS</span></span>
