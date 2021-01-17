---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3e06b4f1236863e208a167024e9d0562dc82ca89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426260"
---
# <span data-ttu-id="310d8-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="310d8-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="310d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="310d8-102">SYNOPSIS</span></span>
<span data-ttu-id="310d8-103">Задает политику виртуальных машин для лабораторных лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="310d8-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="310d8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="310d8-104">SYNTAX</span></span>

### <span data-ttu-id="310d8-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="310d8-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="310d8-106">Отключить</span><span class="sxs-lookup"><span data-stu-id="310d8-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="310d8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="310d8-107">DESCRIPTION</span></span>
<span data-ttu-id="310d8-108">Cmdlet **Set-AzDtlVMsPerLabPolicy** задает виртуальную машину в лабораторной политике, которая задает общее количество виртуальных машин, разрешенных в лабораторной.</span><span class="sxs-lookup"><span data-stu-id="310d8-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="310d8-109">Для этого используется заданная группа ресурсов и название лабораторных работы.</span><span class="sxs-lookup"><span data-stu-id="310d8-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="310d8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="310d8-110">EXAMPLES</span></span>

## <span data-ttu-id="310d8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="310d8-111">PARAMETERS</span></span>

### <span data-ttu-id="310d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310d8-112">-DefaultProfile</span></span>
<span data-ttu-id="310d8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="310d8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="310d8-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="310d8-114">-Disable</span></span>
<span data-ttu-id="310d8-115">Указывает на то, что этот cmdlet отключает политику лабораторных анализов.</span><span class="sxs-lookup"><span data-stu-id="310d8-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310d8-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="310d8-116">-Enable</span></span>
<span data-ttu-id="310d8-117">Указывает на то, что этот cmdlet включает политику лабораторных анализов.</span><span class="sxs-lookup"><span data-stu-id="310d8-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310d8-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="310d8-118">-LabName</span></span>
<span data-ttu-id="310d8-119">Задает имя лаборатории, для которой этот cmdlet задает политику виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="310d8-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="310d8-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="310d8-120">-MaxVMs</span></span>
<span data-ttu-id="310d8-121">Указывает максимальное количество виртуальных машин, которые можно создать в лабораторных условиях.</span><span class="sxs-lookup"><span data-stu-id="310d8-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="310d8-123">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="310d8-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="310d8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="310d8-124">-Confirm</span></span>
<span data-ttu-id="310d8-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="310d8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310d8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310d8-126">-WhatIf</span></span>
<span data-ttu-id="310d8-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="310d8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310d8-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="310d8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310d8-129">CommonParameters</span></span>
<span data-ttu-id="310d8-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="310d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310d8-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310d8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310d8-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="310d8-132">INPUTS</span></span>

### <span data-ttu-id="310d8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="310d8-133">System.String</span></span>

## <span data-ttu-id="310d8-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="310d8-134">OUTPUTS</span></span>

### <span data-ttu-id="310d8-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="310d8-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="310d8-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="310d8-136">NOTES</span></span>

## <span data-ttu-id="310d8-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="310d8-137">RELATED LINKS</span></span>

[<span data-ttu-id="310d8-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="310d8-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


