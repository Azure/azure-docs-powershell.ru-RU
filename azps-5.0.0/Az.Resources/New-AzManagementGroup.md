---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 07272df9b1892373d23b89447f1c21a5a4fb53c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315716"
---
# <span data-ttu-id="f559b-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f559b-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="f559b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f559b-102">SYNOPSIS</span></span>
<span data-ttu-id="f559b-103">Создание группы управления</span><span class="sxs-lookup"><span data-stu-id="f559b-103">Creates a Management Group</span></span>

## <span data-ttu-id="f559b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f559b-104">SYNTAX</span></span>

### <span data-ttu-id="f559b-105">GroupOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f559b-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f559b-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="f559b-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f559b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f559b-107">DESCRIPTION</span></span>
<span data-ttu-id="f559b-108">Командлет **New-AzManagementGroup** создает группу управления.</span><span class="sxs-lookup"><span data-stu-id="f559b-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="f559b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f559b-109">EXAMPLES</span></span>

### <span data-ttu-id="f559b-110">Пример 1: создание группы управления</span><span class="sxs-lookup"><span data-stu-id="f559b-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="f559b-111">Создание новой группы с `DisplayName` `ParentId` заданным значением `null` .</span><span class="sxs-lookup"><span data-stu-id="f559b-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="f559b-112">Оно `DisplayName` будет совпадать с `GroupName` родительским объектом группы, который является клиентом.</span><span class="sxs-lookup"><span data-stu-id="f559b-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="f559b-113">Пример 2: создание группы управления с отображаемым именем</span><span class="sxs-lookup"><span data-stu-id="f559b-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="f559b-114">В этом случае родительский объект группы будет клиентом, и `DisplayName` для него будет задано указанное значение.</span><span class="sxs-lookup"><span data-stu-id="f559b-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="f559b-115">Пример 3: создание группы управления с родительским элементом и отображаемым именем</span><span class="sxs-lookup"><span data-stu-id="f559b-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="f559b-116">Пример 4: создание группы управления с родительским объектом (с использованием родительского объекта)</span><span class="sxs-lookup"><span data-stu-id="f559b-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="f559b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f559b-117">PARAMETERS</span></span>

### <span data-ttu-id="f559b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f559b-118">-DefaultProfile</span></span>
<span data-ttu-id="f559b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f559b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f559b-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f559b-120">-DisplayName</span></span>
<span data-ttu-id="f559b-121">Отображаемое имя группы управления</span><span class="sxs-lookup"><span data-stu-id="f559b-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="f559b-122">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="f559b-122">-GroupName</span></span>
<span data-ttu-id="f559b-123">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="f559b-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f559b-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="f559b-124">-ParentId</span></span>
<span data-ttu-id="f559b-125">Родительский идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="f559b-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f559b-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f559b-126">-ParentObject</span></span>
<span data-ttu-id="f559b-127">Родительский объект</span><span class="sxs-lookup"><span data-stu-id="f559b-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f559b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f559b-128">-Confirm</span></span>
<span data-ttu-id="f559b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f559b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f559b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f559b-130">-WhatIf</span></span>
<span data-ttu-id="f559b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f559b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f559b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f559b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f559b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f559b-133">CommonParameters</span></span>
<span data-ttu-id="f559b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f559b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f559b-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f559b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f559b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f559b-136">INPUTS</span></span>

### <span data-ttu-id="f559b-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="f559b-137">None</span></span>

## <span data-ttu-id="f559b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f559b-138">OUTPUTS</span></span>

### <span data-ttu-id="f559b-139">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f559b-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="f559b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="f559b-140">NOTES</span></span>

## <span data-ttu-id="f559b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f559b-141">RELATED LINKS</span></span>

[<span data-ttu-id="f559b-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f559b-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="f559b-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f559b-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="f559b-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f559b-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)