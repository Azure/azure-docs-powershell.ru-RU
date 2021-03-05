---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: 4686941a744532ad8d6f48e079e8120b6d6b3a53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985631"
---
# <span data-ttu-id="f2f21-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f2f21-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="f2f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f21-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f21-103">Gets Management Group(s)</span><span class="sxs-lookup"><span data-stu-id="f2f21-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="f2f21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2f21-104">SYNTAX</span></span>

### <span data-ttu-id="f2f21-105">ListOperation (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2f21-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2f21-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="f2f21-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2f21-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2f21-107">DESCRIPTION</span></span>
<span data-ttu-id="f2f21-108">Этот Get-AzManagementGroup возвращает всю или определенную группу управления.</span><span class="sxs-lookup"><span data-stu-id="f2f21-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="f2f21-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2f21-109">EXAMPLES</span></span>

### <span data-ttu-id="f2f21-110">Пример 1. Получить все группы управления</span><span class="sxs-lookup"><span data-stu-id="f2f21-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="f2f21-111">Пример 2. Получить конкретную группу управления</span><span class="sxs-lookup"><span data-stu-id="f2f21-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="f2f21-112">Пример 3. Получить группу управления и первый уровень иерархии</span><span class="sxs-lookup"><span data-stu-id="f2f21-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="f2f21-113">С помощью `Expand` флажка можно перемещаться по массиву и получать сведения `Children` о каждом ребенке.</span><span class="sxs-lookup"><span data-stu-id="f2f21-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="f2f21-114">Например, `Children[0]` можно предоставить сведения о группе с отображаемой именем. `TestGroup1DisplayName`</span><span class="sxs-lookup"><span data-stu-id="f2f21-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="f2f21-115">Пример 4. Получите определенную группу управления и все уровни иерархии</span><span class="sxs-lookup"><span data-stu-id="f2f21-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="f2f21-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2f21-116">PARAMETERS</span></span>

### <span data-ttu-id="f2f21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f21-117">-DefaultProfile</span></span>
<span data-ttu-id="f2f21-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f21-119">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="f2f21-119">-Expand</span></span>
<span data-ttu-id="f2f21-120">Разорите выходные данные для списка детей группы управления</span><span class="sxs-lookup"><span data-stu-id="f2f21-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f2f21-121">-GroupName</span></span>
<span data-ttu-id="f2f21-122">ИД группы управления</span><span class="sxs-lookup"><span data-stu-id="f2f21-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="f2f21-123">-Recurse</span></span>
<span data-ttu-id="f2f21-124">Recursively list the children of the management group</span><span class="sxs-lookup"><span data-stu-id="f2f21-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2f21-125">-Confirm</span></span>
<span data-ttu-id="f2f21-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f2f21-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f21-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f21-127">-WhatIf</span></span>
<span data-ttu-id="f2f21-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f21-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2f21-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f2f21-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f21-130">CommonParameters</span></span>
<span data-ttu-id="f2f21-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f21-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2f21-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f21-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2f21-133">INPUTS</span></span>

### <span data-ttu-id="f2f21-134">Нет</span><span class="sxs-lookup"><span data-stu-id="f2f21-134">None</span></span>

## <span data-ttu-id="f2f21-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2f21-135">OUTPUTS</span></span>

### <span data-ttu-id="f2f21-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="f2f21-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="f2f21-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f2f21-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="f2f21-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2f21-138">NOTES</span></span>

## <span data-ttu-id="f2f21-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2f21-139">RELATED LINKS</span></span>
