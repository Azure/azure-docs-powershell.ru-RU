---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 30aad11674cbdef747e444d18bce55ed223e3698
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010579"
---
# <span data-ttu-id="55a30-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="55a30-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="55a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a30-102">SYNOPSIS</span></span>
<span data-ttu-id="55a30-103">Задает политику виртуальных машин для лабораторных лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="55a30-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="55a30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55a30-104">SYNTAX</span></span>

### <span data-ttu-id="55a30-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55a30-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a30-106">"Отключить"</span><span class="sxs-lookup"><span data-stu-id="55a30-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a30-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55a30-107">DESCRIPTION</span></span>
<span data-ttu-id="55a30-108">Для этого используется поле **"Set-AzDtlVMsPerLabPolicy",** которое задает политику для виртуальных машин в лабораторных условиях, которая задает общее количество виртуальных машин, разрешенных в лабораторной.</span><span class="sxs-lookup"><span data-stu-id="55a30-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="55a30-109">Для этого используется заданная группа ресурсов и название лабораторных работы.</span><span class="sxs-lookup"><span data-stu-id="55a30-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="55a30-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55a30-110">EXAMPLES</span></span>

## <span data-ttu-id="55a30-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55a30-111">PARAMETERS</span></span>

### <span data-ttu-id="55a30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a30-112">-DefaultProfile</span></span>
<span data-ttu-id="55a30-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55a30-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55a30-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="55a30-114">-Disable</span></span>
<span data-ttu-id="55a30-115">Указывает на то, что этот cmdlet отключает политику лабораторных анализов.</span><span class="sxs-lookup"><span data-stu-id="55a30-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="55a30-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="55a30-116">-Enable</span></span>
<span data-ttu-id="55a30-117">Указывает на то, что этот cmdlet включает политику лабораторных анализов.</span><span class="sxs-lookup"><span data-stu-id="55a30-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="55a30-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="55a30-118">-LabName</span></span>
<span data-ttu-id="55a30-119">Задает имя лаборатории, для которой этот cmdlet задает политику виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="55a30-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="55a30-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="55a30-120">-MaxVMs</span></span>
<span data-ttu-id="55a30-121">Указывает максимальное количество виртуальных машин, которые можно создать в лабораторных условиях.</span><span class="sxs-lookup"><span data-stu-id="55a30-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="55a30-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a30-122">-ResourceGroupName</span></span>
<span data-ttu-id="55a30-123">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="55a30-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="55a30-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55a30-124">-Confirm</span></span>
<span data-ttu-id="55a30-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="55a30-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a30-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a30-126">-WhatIf</span></span>
<span data-ttu-id="55a30-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55a30-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a30-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="55a30-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a30-129">CommonParameters</span></span>
<span data-ttu-id="55a30-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a30-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55a30-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a30-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55a30-132">INPUTS</span></span>

### <span data-ttu-id="55a30-133">System.String</span><span class="sxs-lookup"><span data-stu-id="55a30-133">System.String</span></span>

## <span data-ttu-id="55a30-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55a30-134">OUTPUTS</span></span>

### <span data-ttu-id="55a30-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="55a30-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="55a30-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55a30-136">NOTES</span></span>

## <span data-ttu-id="55a30-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55a30-137">RELATED LINKS</span></span>

[<span data-ttu-id="55a30-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="55a30-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


