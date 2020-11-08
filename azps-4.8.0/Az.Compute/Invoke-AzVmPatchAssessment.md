---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235649"
---
# <span data-ttu-id="254a0-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="254a0-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="254a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="254a0-102">SYNOPSIS</span></span>
<span data-ttu-id="254a0-103">Оценка состояния исправления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="254a0-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="254a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="254a0-104">SYNTAX</span></span>

### <span data-ttu-id="254a0-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="254a0-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="254a0-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="254a0-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="254a0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="254a0-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="254a0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="254a0-108">DESCRIPTION</span></span>
<span data-ttu-id="254a0-109">Оценивает состояние исправления ВМ и сообщает обо всех обнаруженных исправлениях, которые можно установить.</span><span class="sxs-lookup"><span data-stu-id="254a0-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="254a0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="254a0-110">EXAMPLES</span></span>

### <span data-ttu-id="254a0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="254a0-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="254a0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="254a0-112">PARAMETERS</span></span>

### <span data-ttu-id="254a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="254a0-113">-AsJob</span></span>
<span data-ttu-id="254a0-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="254a0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="254a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254a0-115">-DefaultProfile</span></span>
<span data-ttu-id="254a0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="254a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="254a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="254a0-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="254a0-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="254a0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="254a0-119">-ResourceId</span></span>
<span data-ttu-id="254a0-120">Идентификатор ресурса для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="254a0-120">Resource ID for your virtual machine.</span></span>

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

### <span data-ttu-id="254a0-121">-VM</span><span class="sxs-lookup"><span data-stu-id="254a0-121">-VM</span></span>
<span data-ttu-id="254a0-122">Объект виртуальной машины PowerShell</span><span class="sxs-lookup"><span data-stu-id="254a0-122">PowerShell Virtual Machine Object</span></span>

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

### <span data-ttu-id="254a0-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="254a0-123">-VMName</span></span>
<span data-ttu-id="254a0-124">Имя виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="254a0-124">Virtual Machine name</span></span>

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

### <span data-ttu-id="254a0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="254a0-125">-Confirm</span></span>
<span data-ttu-id="254a0-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="254a0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="254a0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="254a0-127">-WhatIf</span></span>
<span data-ttu-id="254a0-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="254a0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="254a0-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="254a0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="254a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254a0-130">CommonParameters</span></span>
<span data-ttu-id="254a0-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="254a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254a0-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="254a0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254a0-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="254a0-133">INPUTS</span></span>

### <span data-ttu-id="254a0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="254a0-134">System.String</span></span>

## <span data-ttu-id="254a0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="254a0-135">OUTPUTS</span></span>

### <span data-ttu-id="254a0-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="254a0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="254a0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="254a0-137">NOTES</span></span>

## <span data-ttu-id="254a0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="254a0-138">RELATED LINKS</span></span>