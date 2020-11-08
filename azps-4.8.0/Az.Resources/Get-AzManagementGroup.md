---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: f21a6d641e06916ce70c71338b539ef0909db6de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242687"
---
# <span data-ttu-id="56eb4-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="56eb4-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="56eb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="56eb4-103">Получает группы управления (-ов)</span><span class="sxs-lookup"><span data-stu-id="56eb4-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="56eb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56eb4-104">SYNTAX</span></span>

### <span data-ttu-id="56eb4-105">ListOperation (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56eb4-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56eb4-106">Операция с операцией</span><span class="sxs-lookup"><span data-stu-id="56eb4-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56eb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56eb4-107">DESCRIPTION</span></span>
<span data-ttu-id="56eb4-108">Командлет Get-AzManagementGroup возвращает все или определенную группу управления.</span><span class="sxs-lookup"><span data-stu-id="56eb4-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="56eb4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56eb4-109">EXAMPLES</span></span>

### <span data-ttu-id="56eb4-110">Пример 1: получение всех групп управления</span><span class="sxs-lookup"><span data-stu-id="56eb4-110">Example 1: Get all Management Groups</span></span>
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

### <span data-ttu-id="56eb4-111">Пример 2: получение определенной группы управления</span><span class="sxs-lookup"><span data-stu-id="56eb4-111">Example 2: Get specific Management Group</span></span>
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

### <span data-ttu-id="56eb4-112">Пример 3: получение определенной группы управления и первого уровня иерархии</span><span class="sxs-lookup"><span data-stu-id="56eb4-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
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

<span data-ttu-id="56eb4-113">С помощью `Expand` флага один из них может перемещаться по `Children` массиву и получать сведения о каждом дочернем элементе.</span><span class="sxs-lookup"><span data-stu-id="56eb4-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="56eb4-114">Например, `Children[0]` вы получите сведения о группе с отображаемым именем `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="56eb4-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="56eb4-115">Пример 4: получение определенной группы управления и всех уровней иерархии</span><span class="sxs-lookup"><span data-stu-id="56eb4-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
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

## <span data-ttu-id="56eb4-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56eb4-116">PARAMETERS</span></span>

### <span data-ttu-id="56eb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56eb4-117">-DefaultProfile</span></span>
<span data-ttu-id="56eb4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56eb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56eb4-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="56eb4-119">-Expand</span></span>
<span data-ttu-id="56eb4-120">Разверните вывод со списком дочерних элементов группы "Менеджмент".</span><span class="sxs-lookup"><span data-stu-id="56eb4-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="56eb4-121">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="56eb4-121">-GroupName</span></span>
<span data-ttu-id="56eb4-122">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="56eb4-122">Management Group Id</span></span>

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

### <span data-ttu-id="56eb4-123">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="56eb4-123">-Recurse</span></span>
<span data-ttu-id="56eb4-124">Рекурсивный список дочерних элементов группы "Менеджмент"</span><span class="sxs-lookup"><span data-stu-id="56eb4-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="56eb4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56eb4-125">-Confirm</span></span>
<span data-ttu-id="56eb4-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56eb4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56eb4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56eb4-127">-WhatIf</span></span>
<span data-ttu-id="56eb4-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56eb4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56eb4-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56eb4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56eb4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56eb4-130">CommonParameters</span></span>
<span data-ttu-id="56eb4-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56eb4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56eb4-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56eb4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56eb4-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56eb4-133">INPUTS</span></span>

### <span data-ttu-id="56eb4-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="56eb4-134">None</span></span>

## <span data-ttu-id="56eb4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56eb4-135">OUTPUTS</span></span>

### <span data-ttu-id="56eb4-136">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="56eb4-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="56eb4-137">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="56eb4-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="56eb4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="56eb4-138">NOTES</span></span>

## <span data-ttu-id="56eb4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56eb4-139">RELATED LINKS</span></span>