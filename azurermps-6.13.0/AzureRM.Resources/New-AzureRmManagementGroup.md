---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
ms.openlocfilehash: 20cfc2ef6b4b59e8cdd605dd14302aa1a172acb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556515"
---
# <span data-ttu-id="4b4e9-101">New-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4b4e9-101">New-AzureRmManagementGroup</span></span>

## <span data-ttu-id="4b4e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4e9-103">Создание группы управления</span><span class="sxs-lookup"><span data-stu-id="4b4e9-103">Creates a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b4e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b4e9-104">SYNTAX</span></span>

### <span data-ttu-id="4b4e9-105">GroupOperations (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b4e9-105">GroupOperations (Default)</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b4e9-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="4b4e9-106">ParentGroupObject</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b4e9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b4e9-107">DESCRIPTION</span></span>
<span data-ttu-id="4b4e9-108">Командлет **New-AzureRMManagementGroup** создает группу управления.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-108">The **New-AzureRMManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="4b4e9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b4e9-109">EXAMPLES</span></span>

### <span data-ttu-id="4b4e9-110">Пример 1: создание группы управления</span><span class="sxs-lookup"><span data-stu-id="4b4e9-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup"

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

<span data-ttu-id="4b4e9-111">Создание новой группы с `DisplayName` `ParentId` заданным значением `null` .</span><span class="sxs-lookup"><span data-stu-id="4b4e9-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="4b4e9-112">Оно `DisplayName` будет совпадать с `GroupName` родительским объектом группы, который является клиентом.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="4b4e9-113">Пример 2: создание группы управления с отображаемым именем</span><span class="sxs-lookup"><span data-stu-id="4b4e9-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

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

<span data-ttu-id="4b4e9-114">В этом случае родительский объект группы будет клиентом, и `DisplayName` для него будет задано указанное значение.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="4b4e9-115">Пример 3: создание группы управления с родительским элементом и отображаемым именем</span><span class="sxs-lookup"><span data-stu-id="4b4e9-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="4b4e9-116">Пример 4: создание группы управления с родительским объектом (с использованием родительского объекта)</span><span class="sxs-lookup"><span data-stu-id="4b4e9-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzureRmManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="4b4e9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b4e9-117">PARAMETERS</span></span>

### <span data-ttu-id="4b4e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4e9-118">-DefaultProfile</span></span>
<span data-ttu-id="4b4e9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b4e9-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4b4e9-120">-DisplayName</span></span>
<span data-ttu-id="4b4e9-121">Отображаемое имя группы управления</span><span class="sxs-lookup"><span data-stu-id="4b4e9-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="4b4e9-122">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="4b4e9-122">-GroupName</span></span>
<span data-ttu-id="4b4e9-123">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="4b4e9-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b4e9-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="4b4e9-124">-ParentId</span></span>
<span data-ttu-id="4b4e9-125">Родительский идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="4b4e9-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="4b4e9-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4b4e9-126">-ParentObject</span></span>
<span data-ttu-id="4b4e9-127">Родительский объект</span><span class="sxs-lookup"><span data-stu-id="4b4e9-127">Parent Object</span></span>

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

### <span data-ttu-id="4b4e9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b4e9-128">-Confirm</span></span>
<span data-ttu-id="4b4e9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b4e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b4e9-130">-WhatIf</span></span>
<span data-ttu-id="4b4e9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b4e9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b4e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4e9-133">CommonParameters</span></span>
<span data-ttu-id="4b4e9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b4e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4e9-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4e9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4e9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b4e9-136">INPUTS</span></span>

### <span data-ttu-id="4b4e9-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="4b4e9-137">None</span></span>

## <span data-ttu-id="4b4e9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b4e9-138">OUTPUTS</span></span>

### <span data-ttu-id="4b4e9-139">Microsoft. Azure. Commands. Resources. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4b4e9-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="4b4e9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b4e9-140">NOTES</span></span>

## <span data-ttu-id="4b4e9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b4e9-141">RELATED LINKS</span></span>

[<span data-ttu-id="4b4e9-142">Remove-AzureRMManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4b4e9-142">Remove-AzureRMManagementGroup</span></span>](./Remove-AzureRMManagementGroup.md)

[<span data-ttu-id="4b4e9-143">Update-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4b4e9-143">Update-AzureRmManagementGroup</span></span>](./Update-AzureRmManagementGroup.md)

[<span data-ttu-id="4b4e9-144">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4b4e9-144">Get-AzureRmManagementGroup</span></span>](./Get-AzureRmManagementGroup.md)
