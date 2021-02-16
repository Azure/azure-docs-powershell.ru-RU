---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229100"
---
# <span data-ttu-id="82ba0-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="82ba0-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="82ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="82ba0-103">Оцените состояние исправления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="82ba0-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="82ba0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82ba0-104">SYNTAX</span></span>

### <span data-ttu-id="82ba0-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82ba0-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ba0-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ba0-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ba0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ba0-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ba0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82ba0-108">DESCRIPTION</span></span>
<span data-ttu-id="82ba0-109">Оценивает состояние исправлений для VM-системы и сообщает о всех обнаруженных исправлениях, доступных для установки.</span><span class="sxs-lookup"><span data-stu-id="82ba0-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="82ba0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82ba0-110">EXAMPLES</span></span>

### <span data-ttu-id="82ba0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82ba0-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="82ba0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="82ba0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82ba0-113">-AsJob</span></span>
<span data-ttu-id="82ba0-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="82ba0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82ba0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ba0-115">-DefaultProfile</span></span>
<span data-ttu-id="82ba0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82ba0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ba0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ba0-117">-ResourceGroupName</span></span>
<span data-ttu-id="82ba0-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82ba0-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ba0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82ba0-119">-ResourceId</span></span>
<span data-ttu-id="82ba0-120">ИД ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="82ba0-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ba0-121">-VM</span><span class="sxs-lookup"><span data-stu-id="82ba0-121">-VM</span></span>
<span data-ttu-id="82ba0-122">Объект виртуальной машины PowerShell</span><span class="sxs-lookup"><span data-stu-id="82ba0-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ba0-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="82ba0-123">-VMName</span></span>
<span data-ttu-id="82ba0-124">Имя виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="82ba0-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ba0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82ba0-125">-Confirm</span></span>
<span data-ttu-id="82ba0-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="82ba0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ba0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ba0-127">-WhatIf</span></span>
<span data-ttu-id="82ba0-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ba0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82ba0-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82ba0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ba0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ba0-130">CommonParameters</span></span>
<span data-ttu-id="82ba0-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ba0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ba0-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82ba0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ba0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82ba0-133">INPUTS</span></span>

### <span data-ttu-id="82ba0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="82ba0-134">System.String</span></span>

## <span data-ttu-id="82ba0-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82ba0-135">OUTPUTS</span></span>

### <span data-ttu-id="82ba0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelsePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="82ba0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="82ba0-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82ba0-137">NOTES</span></span>

## <span data-ttu-id="82ba0-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82ba0-138">RELATED LINKS</span></span>
