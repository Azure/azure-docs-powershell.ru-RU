---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: bb1fbb999d9e75569fa7321a6e2d9e5391c95943
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910953"
---
# <span data-ttu-id="6138a-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6138a-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="6138a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6138a-102">SYNOPSIS</span></span>
<span data-ttu-id="6138a-103">Получает группы управления (-ов)</span><span class="sxs-lookup"><span data-stu-id="6138a-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="6138a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6138a-104">SYNTAX</span></span>

### <span data-ttu-id="6138a-105">ListOperation (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6138a-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6138a-106">Операция с операцией</span><span class="sxs-lookup"><span data-stu-id="6138a-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand]
 [-Recurse] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6138a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6138a-107">DESCRIPTION</span></span>
<span data-ttu-id="6138a-108">Командлет Get-AzManagementGroup возвращает все или определенную группу управления.</span><span class="sxs-lookup"><span data-stu-id="6138a-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="6138a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6138a-109">EXAMPLES</span></span>

### <span data-ttu-id="6138a-110">Пример 1: получение всех групп управления</span><span class="sxs-lookup"><span data-stu-id="6138a-110">Example 1: Get all Management Groups</span></span>
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

### <span data-ttu-id="6138a-111">Пример 2: получение определенной группы управления</span><span class="sxs-lookup"><span data-stu-id="6138a-111">Example 2: Get specific Management Group</span></span>
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

### <span data-ttu-id="6138a-112">Пример 3: получение определенной группы управления и первого уровня иерархии</span><span class="sxs-lookup"><span data-stu-id="6138a-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
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

<span data-ttu-id="6138a-113">С помощью `Expand` флага один из них может перемещаться по `Children` массиву и получать сведения о каждом дочернем элементе.</span><span class="sxs-lookup"><span data-stu-id="6138a-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="6138a-114">Например, `Children[0]` вы получите сведения о группе с отображаемым именем `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="6138a-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="6138a-115">Пример 4: получение определенной группы управления и всех уровней hiearchy</span><span class="sxs-lookup"><span data-stu-id="6138a-115">Example 4: Get specific Management Group and all levels of hiearchy</span></span>
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

## <span data-ttu-id="6138a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6138a-116">PARAMETERS</span></span>

### <span data-ttu-id="6138a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6138a-117">-DefaultProfile</span></span>
<span data-ttu-id="6138a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6138a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6138a-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="6138a-119">-Expand</span></span>
<span data-ttu-id="6138a-120">Разверните вывод со списком дочерних элементов группы "Менеджмент".</span><span class="sxs-lookup"><span data-stu-id="6138a-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="6138a-121">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="6138a-121">-GroupName</span></span>
<span data-ttu-id="6138a-122">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="6138a-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6138a-123">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="6138a-123">-Recurse</span></span>
<span data-ttu-id="6138a-124">Рекурсивный список дочерних элементов группы "Менеджмент"</span><span class="sxs-lookup"><span data-stu-id="6138a-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="6138a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6138a-125">-Confirm</span></span>
<span data-ttu-id="6138a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6138a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6138a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6138a-127">-WhatIf</span></span>
<span data-ttu-id="6138a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6138a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6138a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6138a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6138a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6138a-130">CommonParameters</span></span>
<span data-ttu-id="6138a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6138a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6138a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6138a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6138a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6138a-133">INPUTS</span></span>

### <span data-ttu-id="6138a-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="6138a-134">None</span></span>

## <span data-ttu-id="6138a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6138a-135">OUTPUTS</span></span>

### <span data-ttu-id="6138a-136">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="6138a-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="6138a-137">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6138a-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6138a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6138a-138">NOTES</span></span>

## <span data-ttu-id="6138a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6138a-139">RELATED LINKS</span></span>
