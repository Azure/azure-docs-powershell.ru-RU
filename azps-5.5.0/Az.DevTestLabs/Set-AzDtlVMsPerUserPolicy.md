---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230497"
---
# <span data-ttu-id="ed8d9-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="ed8d9-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="ed8d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8d9-103">Задает виртуальную машину на пользователя в лабораторной лаборатории DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ed8d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed8d9-104">SYNTAX</span></span>

### <span data-ttu-id="ed8d9-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed8d9-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8d9-106">"Отключить"</span><span class="sxs-lookup"><span data-stu-id="ed8d9-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8d9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed8d9-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8d9-108">Cmdlet **Set-AzDtlVMsPerUserPolicy** задает виртуальную машину на пользователя в лабораторной, которая задает максимальное количество виртуальных машин, разрешенных для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="ed8d9-109">Для этого используется указанная группа ресурсов и название лабораторных работы.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="ed8d9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed8d9-110">EXAMPLES</span></span>

## <span data-ttu-id="ed8d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed8d9-111">PARAMETERS</span></span>

### <span data-ttu-id="ed8d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8d9-112">-DefaultProfile</span></span>
<span data-ttu-id="ed8d9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed8d9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed8d9-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="ed8d9-114">-Disable</span></span>
<span data-ttu-id="ed8d9-115">Указывает на то, что этот cmdlet отключает политику для лабораторной работы.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="ed8d9-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="ed8d9-116">-Enable</span></span>
<span data-ttu-id="ed8d9-117">Указывает на то, что этот cmdlet включает политику для лабораторных анализов.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="ed8d9-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="ed8d9-118">-LabName</span></span>
<span data-ttu-id="ed8d9-119">Задает имя лаборатории, для которой этот cmdlet задает виртуальные машины в политике пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="ed8d9-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="ed8d9-120">-MaxVMs</span></span>
<span data-ttu-id="ed8d9-121">Указывает максимальное количество виртуальных машин, которые можно создать в лабораторных условиях.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="ed8d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed8d9-123">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ed8d9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed8d9-124">-Confirm</span></span>
<span data-ttu-id="ed8d9-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8d9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8d9-126">-WhatIf</span></span>
<span data-ttu-id="ed8d9-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed8d9-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8d9-129">CommonParameters</span></span>
<span data-ttu-id="ed8d9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8d9-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8d9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8d9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed8d9-132">INPUTS</span></span>

### <span data-ttu-id="ed8d9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ed8d9-133">System.String</span></span>

## <span data-ttu-id="ed8d9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed8d9-134">OUTPUTS</span></span>

### <span data-ttu-id="ed8d9-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ed8d9-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="ed8d9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed8d9-136">NOTES</span></span>

## <span data-ttu-id="ed8d9-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed8d9-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed8d9-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="ed8d9-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


