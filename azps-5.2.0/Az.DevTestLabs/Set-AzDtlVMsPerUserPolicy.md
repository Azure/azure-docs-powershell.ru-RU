---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396684"
---
# <span data-ttu-id="a44e0-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="a44e0-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="a44e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a44e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a44e0-103">Задает виртуальную машину на пользователя в лабораторной лаборатории DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="a44e0-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a44e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a44e0-104">SYNTAX</span></span>

### <span data-ttu-id="a44e0-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a44e0-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a44e0-106">Отключить</span><span class="sxs-lookup"><span data-stu-id="a44e0-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a44e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a44e0-107">DESCRIPTION</span></span>
<span data-ttu-id="a44e0-108">Cmdlet **Set-AzDtlVMsPerUserPolicy** задает виртуальную машину на пользователя в лабораторной, которая задает максимальное количество виртуальных машин, разрешенных для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a44e0-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="a44e0-109">Для этого используется заданная группа ресурсов и название лабораторных работы.</span><span class="sxs-lookup"><span data-stu-id="a44e0-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="a44e0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a44e0-110">EXAMPLES</span></span>

## <span data-ttu-id="a44e0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a44e0-111">PARAMETERS</span></span>

### <span data-ttu-id="a44e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44e0-112">-DefaultProfile</span></span>
<span data-ttu-id="a44e0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a44e0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a44e0-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="a44e0-114">-Disable</span></span>
<span data-ttu-id="a44e0-115">Указывает на то, что этот cmdlet отключает политику для лабораторных анализов.</span><span class="sxs-lookup"><span data-stu-id="a44e0-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="a44e0-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="a44e0-116">-Enable</span></span>
<span data-ttu-id="a44e0-117">Указывает на то, что этот cmdlet включает политику для лабораторных анализов.</span><span class="sxs-lookup"><span data-stu-id="a44e0-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="a44e0-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="a44e0-118">-LabName</span></span>
<span data-ttu-id="a44e0-119">Задает имя лаборатории, для которой этот cmdlet задает виртуальные машины в политике пользователя.</span><span class="sxs-lookup"><span data-stu-id="a44e0-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="a44e0-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="a44e0-120">-MaxVMs</span></span>
<span data-ttu-id="a44e0-121">Указывает максимальное количество виртуальных машин, которые можно создать в лабораторных условиях.</span><span class="sxs-lookup"><span data-stu-id="a44e0-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="a44e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a44e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="a44e0-123">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="a44e0-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a44e0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a44e0-124">-Confirm</span></span>
<span data-ttu-id="a44e0-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a44e0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a44e0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a44e0-126">-WhatIf</span></span>
<span data-ttu-id="a44e0-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a44e0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a44e0-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a44e0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a44e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44e0-129">CommonParameters</span></span>
<span data-ttu-id="a44e0-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a44e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44e0-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a44e0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44e0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a44e0-132">INPUTS</span></span>

### <span data-ttu-id="a44e0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a44e0-133">System.String</span></span>

## <span data-ttu-id="a44e0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a44e0-134">OUTPUTS</span></span>

### <span data-ttu-id="a44e0-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a44e0-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a44e0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a44e0-136">NOTES</span></span>

## <span data-ttu-id="a44e0-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a44e0-137">RELATED LINKS</span></span>

[<span data-ttu-id="a44e0-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="a44e0-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)

