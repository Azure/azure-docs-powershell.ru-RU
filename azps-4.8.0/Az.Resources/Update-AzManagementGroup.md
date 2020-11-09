---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdef58db8dcda735a7a8c08350b806c9fd00cf21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244001"
---
# <span data-ttu-id="6b3b2-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b3b2-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="6b3b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3b2-103">Обновляет группу управления</span><span class="sxs-lookup"><span data-stu-id="6b3b2-103">Updates a Management Group</span></span>

## <span data-ttu-id="6b3b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b3b2-104">SYNTAX</span></span>

### <span data-ttu-id="6b3b2-105">GroupOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b3b2-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3b2-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="6b3b2-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b3b2-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="6b3b2-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3b2-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="6b3b2-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b3b2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b3b2-109">DESCRIPTION</span></span>
<span data-ttu-id="6b3b2-110">Командлет **Update-AzManagementGroup** обновляет **ParentID** или **DisplayName** для группы управления.</span><span class="sxs-lookup"><span data-stu-id="6b3b2-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="6b3b2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b3b2-111">EXAMPLES</span></span>

### <span data-ttu-id="6b3b2-112">Пример 1: обновление отображаемого имени группы управления</span><span class="sxs-lookup"><span data-stu-id="6b3b2-112">Example 1: Update a Management Group's Display Name</span></span>
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

### <span data-ttu-id="6b3b2-113">Пример 2: обновление родительского элемента группы управления</span><span class="sxs-lookup"><span data-stu-id="6b3b2-113">Example 2: Update a Management Group's Parent</span></span>
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

### <span data-ttu-id="6b3b2-114">Пример 3: Обновление группы управления с помощью объекта трубопроводов PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b3b2-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
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

### <span data-ttu-id="6b3b2-115">Пример 4: обновление родительского элемента группы управления с помощью ParentObject</span><span class="sxs-lookup"><span data-stu-id="6b3b2-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
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

## <span data-ttu-id="6b3b2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b3b2-116">PARAMETERS</span></span>

### <span data-ttu-id="6b3b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3b2-117">-DefaultProfile</span></span>
<span data-ttu-id="6b3b2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b3b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b3b2-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6b3b2-119">-DisplayName</span></span>
<span data-ttu-id="6b3b2-120">Отображаемое имя группы управления</span><span class="sxs-lookup"><span data-stu-id="6b3b2-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="6b3b2-121">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="6b3b2-121">-GroupName</span></span>
<span data-ttu-id="6b3b2-122">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="6b3b2-122">Management Group Id</span></span>

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

### <span data-ttu-id="6b3b2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b3b2-123">-InputObject</span></span>
<span data-ttu-id="6b3b2-124">Объект input из вызова Get</span><span class="sxs-lookup"><span data-stu-id="6b3b2-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="6b3b2-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="6b3b2-125">-ParentId</span></span>
<span data-ttu-id="6b3b2-126">Родительский идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="6b3b2-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="6b3b2-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6b3b2-127">-ParentObject</span></span>
<span data-ttu-id="6b3b2-128">Объект input из вызова Get</span><span class="sxs-lookup"><span data-stu-id="6b3b2-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="6b3b2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b3b2-129">-Confirm</span></span>
<span data-ttu-id="6b3b2-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b3b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3b2-131">-WhatIf</span></span>
<span data-ttu-id="6b3b2-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b3b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b3b2-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b3b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b3b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3b2-134">CommonParameters</span></span>
<span data-ttu-id="6b3b2-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b3b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3b2-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b3b2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3b2-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b3b2-137">INPUTS</span></span>

### <span data-ttu-id="6b3b2-138">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b3b2-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6b3b2-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b3b2-139">OUTPUTS</span></span>

### <span data-ttu-id="6b3b2-140">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b3b2-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6b3b2-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b3b2-141">NOTES</span></span>

## <span data-ttu-id="6b3b2-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b3b2-142">RELATED LINKS</span></span>