---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: 6b646e22ff32d9fe361cdedd6dbb6fa5c9fba270
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010840"
---
# <span data-ttu-id="3d58a-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="3d58a-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="3d58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d58a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d58a-103">Получите одно или несколько определений схем.</span><span class="sxs-lookup"><span data-stu-id="3d58a-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="3d58a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d58a-104">SYNTAX</span></span>

### <span data-ttu-id="3d58a-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d58a-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d58a-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="3d58a-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d58a-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="3d58a-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d58a-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="3d58a-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d58a-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="3d58a-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d58a-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="3d58a-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d58a-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="3d58a-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d58a-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="3d58a-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d58a-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d58a-113">DESCRIPTION</span></span>
<span data-ttu-id="3d58a-114">Получите одно или несколько определений схем.</span><span class="sxs-lookup"><span data-stu-id="3d58a-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="3d58a-115">Определение схемы существует в составе группы управления или подписки.</span><span class="sxs-lookup"><span data-stu-id="3d58a-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="3d58a-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d58a-116">EXAMPLES</span></span>

### <span data-ttu-id="3d58a-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d58a-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="3d58a-118">Получите определение схемы в текущей подписке и иерархию группы управления подписки.</span><span class="sxs-lookup"><span data-stu-id="3d58a-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="3d58a-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3d58a-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="3d58a-120">Получите определение схемы в пределах указанной группы управления.</span><span class="sxs-lookup"><span data-stu-id="3d58a-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="3d58a-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3d58a-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="3d58a-122">Получите определение схемы в рамках указанной подписки и иерархию группы управления в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="3d58a-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="3d58a-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="3d58a-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="3d58a-124">Получите определение схемы с указанным именем в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="3d58a-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="3d58a-125">Пример 5</span><span class="sxs-lookup"><span data-stu-id="3d58a-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="3d58a-126">Определение документа с указанным именем и версией в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="3d58a-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="3d58a-127">Пример 6</span><span class="sxs-lookup"><span data-stu-id="3d58a-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="3d58a-128">Получите последнее определение опубликованного чертежа с указанным именем в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="3d58a-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="3d58a-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d58a-129">PARAMETERS</span></span>

### <span data-ttu-id="3d58a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d58a-130">-DefaultProfile</span></span>
<span data-ttu-id="3d58a-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d58a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d58a-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="3d58a-132">-LatestPublished</span></span>
<span data-ttu-id="3d58a-133">Последний опубликованный флаг определения схемы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="3d58a-134">Если все настроено, то выполнение возвращает последнюю опубликованную версию определения документа.</span><span class="sxs-lookup"><span data-stu-id="3d58a-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="3d58a-135">Значение по умолчанию false.</span><span class="sxs-lookup"><span data-stu-id="3d58a-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d58a-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="3d58a-136">-ManagementGroupId</span></span>
<span data-ttu-id="3d58a-137">ИД группы управления, в которой сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d58a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="3d58a-138">-Name</span></span>
<span data-ttu-id="3d58a-139">Название определения схемы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d58a-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d58a-140">-SubscriptionId</span></span>
<span data-ttu-id="3d58a-141">ИД подписки, в котором сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d58a-142">-Version</span><span class="sxs-lookup"><span data-stu-id="3d58a-142">-Version</span></span>
<span data-ttu-id="3d58a-143">Опубликованная версия определения схемы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d58a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d58a-144">CommonParameters</span></span>
<span data-ttu-id="3d58a-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d58a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d58a-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d58a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d58a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d58a-147">INPUTS</span></span>

### <span data-ttu-id="3d58a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3d58a-148">System.String</span></span>

## <span data-ttu-id="3d58a-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d58a-149">OUTPUTS</span></span>

### <span data-ttu-id="3d58a-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="3d58a-150">System.Object</span></span>
## <span data-ttu-id="3d58a-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d58a-151">NOTES</span></span>

## <span data-ttu-id="3d58a-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d58a-152">RELATED LINKS</span></span>
