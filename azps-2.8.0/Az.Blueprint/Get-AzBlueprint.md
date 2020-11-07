---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: cd4cb9f7137d0e6cdd91222c278b6e59c04d7e3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727649"
---
# <span data-ttu-id="a77e5-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a77e5-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="a77e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a77e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a77e5-103">Получение одного или нескольких определений чертежей.</span><span class="sxs-lookup"><span data-stu-id="a77e5-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="a77e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a77e5-104">SYNTAX</span></span>

### <span data-ttu-id="a77e5-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a77e5-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a77e5-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="a77e5-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a77e5-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="a77e5-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a77e5-108">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="a77e5-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a77e5-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a77e5-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a77e5-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="a77e5-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a77e5-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="a77e5-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a77e5-112">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="a77e5-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a77e5-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a77e5-113">DESCRIPTION</span></span>
<span data-ttu-id="a77e5-114">Получение одного или нескольких определений чертежей.</span><span class="sxs-lookup"><span data-stu-id="a77e5-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="a77e5-115">Определения чертежей находятся в области группы управления или подписки.</span><span class="sxs-lookup"><span data-stu-id="a77e5-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="a77e5-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a77e5-116">EXAMPLES</span></span>

### <span data-ttu-id="a77e5-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a77e5-117">Example 1</span></span>
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

<span data-ttu-id="a77e5-118">Получение определений чертежей в текущей подписке и иерархии групп управления для подписки.</span><span class="sxs-lookup"><span data-stu-id="a77e5-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="a77e5-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a77e5-119">Example 2</span></span>
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

<span data-ttu-id="a77e5-120">Получение определений чертежей в заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a77e5-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="a77e5-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a77e5-121">Example 3</span></span>
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

<span data-ttu-id="a77e5-122">Получение определений чертежей в указанной подписке и иерархии групп управления для подписки.</span><span class="sxs-lookup"><span data-stu-id="a77e5-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="a77e5-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a77e5-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="a77e5-124">Получение определения плана с заданным именем в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="a77e5-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="a77e5-125">Пример 5</span><span class="sxs-lookup"><span data-stu-id="a77e5-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="a77e5-126">Получение определения чертежа с заданным именем и версией в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a77e5-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="a77e5-127">Пример 6</span><span class="sxs-lookup"><span data-stu-id="a77e5-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="a77e5-128">Получение последнего опубликованного определения чертежа с заданным именем в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a77e5-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="a77e5-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a77e5-129">PARAMETERS</span></span>

### <span data-ttu-id="a77e5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77e5-130">-DefaultProfile</span></span>
<span data-ttu-id="a77e5-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a77e5-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a77e5-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="a77e5-132">-LatestPublished</span></span>
<span data-ttu-id="a77e5-133">Последний опубликованный флаг определения чертежей.</span><span class="sxs-lookup"><span data-stu-id="a77e5-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="a77e5-134">Если этот параметр установлен, выполнение возвращает последнюю опубликованную версию определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="a77e5-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="a77e5-135">По умолчанию используется значение false.</span><span class="sxs-lookup"><span data-stu-id="a77e5-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySubscriptionNameAndLatestPublished, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77e5-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a77e5-136">-ManagementGroupId</span></span>
<span data-ttu-id="a77e5-137">Идентификатор группы управления, в которой хранится определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="a77e5-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a77e5-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a77e5-138">-Name</span></span>
<span data-ttu-id="a77e5-139">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="a77e5-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a77e5-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a77e5-140">-SubscriptionId</span></span>
<span data-ttu-id="a77e5-141">Идентификатор подписки, в которой сохраняется определение.</span><span class="sxs-lookup"><span data-stu-id="a77e5-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a77e5-142">-Version</span><span class="sxs-lookup"><span data-stu-id="a77e5-142">-Version</span></span>
<span data-ttu-id="a77e5-143">Версия определений опубликованных чертежей.</span><span class="sxs-lookup"><span data-stu-id="a77e5-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionNameAndVersion, ByManagementGroupNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a77e5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77e5-144">CommonParameters</span></span>
<span data-ttu-id="a77e5-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a77e5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77e5-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a77e5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77e5-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a77e5-147">INPUTS</span></span>

### <span data-ttu-id="a77e5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a77e5-148">System.String</span></span>

## <span data-ttu-id="a77e5-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a77e5-149">OUTPUTS</span></span>

### <span data-ttu-id="a77e5-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="a77e5-150">System.Object</span></span>
## <span data-ttu-id="a77e5-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="a77e5-151">NOTES</span></span>

## <span data-ttu-id="a77e5-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a77e5-152">RELATED LINKS</span></span>
