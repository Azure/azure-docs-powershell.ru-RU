---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222585"
---
# <span data-ttu-id="5502b-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="5502b-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="5502b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5502b-102">SYNOPSIS</span></span>
<span data-ttu-id="5502b-103">Задает политику допустимого размера виртуальной машины в лабораторной лаборатории DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="5502b-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="5502b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5502b-104">SYNTAX</span></span>

### <span data-ttu-id="5502b-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5502b-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5502b-106">"Отключить"</span><span class="sxs-lookup"><span data-stu-id="5502b-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5502b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5502b-107">DESCRIPTION</span></span>
<span data-ttu-id="5502b-108">Для **этого** задана политика разрешенных размеров виртуальных машин, задав список размеров виртуальных машин, допустимых в лабораторных условиях.</span><span class="sxs-lookup"><span data-stu-id="5502b-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="5502b-109">Для этого используется указанная группа ресурсов и название лабораторных работы.</span><span class="sxs-lookup"><span data-stu-id="5502b-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="5502b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5502b-110">EXAMPLES</span></span>

## <span data-ttu-id="5502b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5502b-111">PARAMETERS</span></span>

### <span data-ttu-id="5502b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5502b-112">-DefaultProfile</span></span>
<span data-ttu-id="5502b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5502b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5502b-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="5502b-114">-Disable</span></span>
<span data-ttu-id="5502b-115">Указывает на то, что этот cmdlet отключает политику.</span><span class="sxs-lookup"><span data-stu-id="5502b-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="5502b-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="5502b-116">-Enable</span></span>
<span data-ttu-id="5502b-117">Указывает на то, что этот cmdlet включает политику.</span><span class="sxs-lookup"><span data-stu-id="5502b-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="5502b-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="5502b-118">-LabName</span></span>
<span data-ttu-id="5502b-119">Задает имя лаборатории, для которой этот cmdlet задает политику размера виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5502b-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="5502b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5502b-120">-ResourceGroupName</span></span>
<span data-ttu-id="5502b-121">Имя группы ресурсов, в которую входит лабораторный анализ.</span><span class="sxs-lookup"><span data-stu-id="5502b-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5502b-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="5502b-122">-VmSizes</span></span>
<span data-ttu-id="5502b-123">Указывает, что в качестве строки массива можно использовать список допустимого размера виртуальной машины в лабораторной.</span><span class="sxs-lookup"><span data-stu-id="5502b-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5502b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5502b-124">-Confirm</span></span>
<span data-ttu-id="5502b-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5502b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5502b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5502b-126">-WhatIf</span></span>
<span data-ttu-id="5502b-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5502b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5502b-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5502b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5502b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5502b-129">CommonParameters</span></span>
<span data-ttu-id="5502b-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5502b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5502b-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5502b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5502b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5502b-132">INPUTS</span></span>

### <span data-ttu-id="5502b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5502b-133">System.String</span></span>

## <span data-ttu-id="5502b-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5502b-134">OUTPUTS</span></span>

### <span data-ttu-id="5502b-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5502b-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="5502b-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5502b-136">NOTES</span></span>

## <span data-ttu-id="5502b-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5502b-137">RELATED LINKS</span></span>

[<span data-ttu-id="5502b-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="5502b-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


