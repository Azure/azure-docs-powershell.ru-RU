---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: 23d60b0251c50f5bf4d5174e1ea1b5ef6f60b0ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972579"
---
# <span data-ttu-id="fe5e7-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fe5e7-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="fe5e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5e7-103">Обновление группы управления</span><span class="sxs-lookup"><span data-stu-id="fe5e7-103">Updates a Management Group</span></span>

## <span data-ttu-id="fe5e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe5e7-104">SYNTAX</span></span>

### <span data-ttu-id="fe5e7-105">GroupOperations (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe5e7-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe5e7-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="fe5e7-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe5e7-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="fe5e7-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe5e7-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="fe5e7-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe5e7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe5e7-109">DESCRIPTION</span></span>
<span data-ttu-id="fe5e7-110">В **результате выполнения команды Update-AzManagementGroup** **обновляется ParentId** или **DisplayName** для группы управления.</span><span class="sxs-lookup"><span data-stu-id="fe5e7-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="fe5e7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe5e7-111">EXAMPLES</span></span>

### <span data-ttu-id="fe5e7-112">Пример 1. Обновление отображаемом имени группы управления</span><span class="sxs-lookup"><span data-stu-id="fe5e7-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="fe5e7-113">Пример 2. Обновление родительского группы</span><span class="sxs-lookup"><span data-stu-id="fe5e7-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="fe5e7-114">Пример 3. Обновление группы управления путем перенаправления объектов PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fe5e7-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="fe5e7-115">Пример 4. Обновление родительского проекта группы управления с помощью parentObject</span><span class="sxs-lookup"><span data-stu-id="fe5e7-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="fe5e7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe5e7-116">PARAMETERS</span></span>

### <span data-ttu-id="fe5e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5e7-117">-DefaultProfile</span></span>
<span data-ttu-id="fe5e7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe5e7-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe5e7-119">-DisplayName</span></span>
<span data-ttu-id="fe5e7-120">Отображаемая группа управления</span><span class="sxs-lookup"><span data-stu-id="fe5e7-120">Display Name of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e7-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="fe5e7-121">-GroupName</span></span>
<span data-ttu-id="fe5e7-122">ИД группы управления</span><span class="sxs-lookup"><span data-stu-id="fe5e7-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe5e7-123">-InputObject</span></span>
<span data-ttu-id="fe5e7-124">Объект ввода из звонка "Получить"</span><span class="sxs-lookup"><span data-stu-id="fe5e7-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e7-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="fe5e7-125">-ParentId</span></span>
<span data-ttu-id="fe5e7-126">Родительский ИД группы управления</span><span class="sxs-lookup"><span data-stu-id="fe5e7-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e7-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fe5e7-127">-ParentObject</span></span>
<span data-ttu-id="fe5e7-128">Объект ввода из звонка "Получить"</span><span class="sxs-lookup"><span data-stu-id="fe5e7-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe5e7-129">-Confirm</span></span>
<span data-ttu-id="fe5e7-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5e7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe5e7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe5e7-131">-WhatIf</span></span>
<span data-ttu-id="fe5e7-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5e7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe5e7-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe5e7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe5e7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5e7-134">CommonParameters</span></span>
<span data-ttu-id="fe5e7-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5e7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5e7-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe5e7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5e7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe5e7-137">INPUTS</span></span>

### <span data-ttu-id="fe5e7-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fe5e7-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="fe5e7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe5e7-139">OUTPUTS</span></span>

### <span data-ttu-id="fe5e7-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fe5e7-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="fe5e7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe5e7-141">NOTES</span></span>

## <span data-ttu-id="fe5e7-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe5e7-142">RELATED LINKS</span></span>
