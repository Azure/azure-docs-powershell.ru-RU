---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392068"
---
# <span data-ttu-id="9fb64-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="9fb64-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="9fb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb64-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb64-103">Получите одно или несколько определений схем.</span><span class="sxs-lookup"><span data-stu-id="9fb64-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="9fb64-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9fb64-104">SYNTAX</span></span>

### <span data-ttu-id="9fb64-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fb64-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb64-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="9fb64-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb64-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="9fb64-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb64-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="9fb64-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb64-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="9fb64-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb64-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="9fb64-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb64-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="9fb64-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fb64-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="9fb64-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fb64-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fb64-113">DESCRIPTION</span></span>
<span data-ttu-id="9fb64-114">Получите одно или несколько определений схем.</span><span class="sxs-lookup"><span data-stu-id="9fb64-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="9fb64-115">Определение схемы существует в составе группы управления или подписки.</span><span class="sxs-lookup"><span data-stu-id="9fb64-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="9fb64-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9fb64-116">EXAMPLES</span></span>

### <span data-ttu-id="9fb64-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9fb64-117">Example 1</span></span>
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

<span data-ttu-id="9fb64-118">Получите определение схемы в текущей подписке и иерархию группы управления подписки.</span><span class="sxs-lookup"><span data-stu-id="9fb64-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="9fb64-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9fb64-119">Example 2</span></span>
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

<span data-ttu-id="9fb64-120">Получите определение схемы в пределах указанной группы управления.</span><span class="sxs-lookup"><span data-stu-id="9fb64-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="9fb64-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9fb64-121">Example 3</span></span>
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

<span data-ttu-id="9fb64-122">Получите определение схемы в рамках указанной подписки и иерархию группы управления в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="9fb64-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="9fb64-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="9fb64-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="9fb64-124">Получите определение схемы с указанным именем в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="9fb64-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="9fb64-125">Пример 5</span><span class="sxs-lookup"><span data-stu-id="9fb64-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="9fb64-126">Определение документа с указанным именем и версией в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="9fb64-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="9fb64-127">Пример 6</span><span class="sxs-lookup"><span data-stu-id="9fb64-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="9fb64-128">Получите последнее определение опубликованного чертежа с указанным именем в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="9fb64-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="9fb64-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fb64-129">PARAMETERS</span></span>

### <span data-ttu-id="9fb64-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb64-130">-DefaultProfile</span></span>
<span data-ttu-id="9fb64-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fb64-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fb64-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="9fb64-132">-LatestPublished</span></span>
<span data-ttu-id="9fb64-133">Последний опубликованный флаг определения схемы.</span><span class="sxs-lookup"><span data-stu-id="9fb64-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="9fb64-134">Если все настроено, то выполнение возвращает последнюю опубликованную версию определения документа.</span><span class="sxs-lookup"><span data-stu-id="9fb64-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="9fb64-135">Значение по умолчанию false.</span><span class="sxs-lookup"><span data-stu-id="9fb64-135">Defaults to false.</span></span>

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

### <span data-ttu-id="9fb64-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9fb64-136">-ManagementGroupId</span></span>
<span data-ttu-id="9fb64-137">ИД группы управления, в которой сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="9fb64-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="9fb64-138">-Name</span><span class="sxs-lookup"><span data-stu-id="9fb64-138">-Name</span></span>
<span data-ttu-id="9fb64-139">Название определения схемы.</span><span class="sxs-lookup"><span data-stu-id="9fb64-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="9fb64-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9fb64-140">-SubscriptionId</span></span>
<span data-ttu-id="9fb64-141">ИД подписки, в котором сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="9fb64-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="9fb64-142">-Версия</span><span class="sxs-lookup"><span data-stu-id="9fb64-142">-Version</span></span>
<span data-ttu-id="9fb64-143">Опубликованная версия определения схемы.</span><span class="sxs-lookup"><span data-stu-id="9fb64-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="9fb64-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb64-144">CommonParameters</span></span>
<span data-ttu-id="9fb64-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb64-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb64-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fb64-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb64-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fb64-147">INPUTS</span></span>

### <span data-ttu-id="9fb64-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9fb64-148">System.String</span></span>

## <span data-ttu-id="9fb64-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9fb64-149">OUTPUTS</span></span>

### <span data-ttu-id="9fb64-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="9fb64-150">System.Object</span></span>
## <span data-ttu-id="9fb64-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9fb64-151">NOTES</span></span>

## <span data-ttu-id="9fb64-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fb64-152">RELATED LINKS</span></span>
