---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078480"
---
# <span data-ttu-id="af00e-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="af00e-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="af00e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af00e-102">SYNOPSIS</span></span>
<span data-ttu-id="af00e-103">Получение одного или нескольких определений чертежей.</span><span class="sxs-lookup"><span data-stu-id="af00e-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="af00e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af00e-104">SYNTAX</span></span>

### <span data-ttu-id="af00e-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af00e-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af00e-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="af00e-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af00e-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="af00e-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af00e-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="af00e-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af00e-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="af00e-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af00e-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="af00e-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af00e-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="af00e-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af00e-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="af00e-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af00e-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af00e-113">DESCRIPTION</span></span>
<span data-ttu-id="af00e-114">Получение одного или нескольких определений чертежей.</span><span class="sxs-lookup"><span data-stu-id="af00e-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="af00e-115">Определения чертежей находятся в области группы управления или подписки.</span><span class="sxs-lookup"><span data-stu-id="af00e-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="af00e-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af00e-116">EXAMPLES</span></span>

### <span data-ttu-id="af00e-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af00e-117">Example 1</span></span>
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

<span data-ttu-id="af00e-118">Получение определений чертежей в текущей подписке и иерархии групп управления для подписки.</span><span class="sxs-lookup"><span data-stu-id="af00e-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="af00e-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="af00e-119">Example 2</span></span>
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

<span data-ttu-id="af00e-120">Получение определений чертежей в заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="af00e-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="af00e-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="af00e-121">Example 3</span></span>
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

<span data-ttu-id="af00e-122">Получение определений чертежей в указанной подписке и иерархии групп управления для подписки.</span><span class="sxs-lookup"><span data-stu-id="af00e-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="af00e-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="af00e-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="af00e-124">Получение определения плана с заданным именем в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="af00e-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="af00e-125">Пример 5</span><span class="sxs-lookup"><span data-stu-id="af00e-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="af00e-126">Получение определения чертежа с заданным именем и версией в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="af00e-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="af00e-127">Пример 6</span><span class="sxs-lookup"><span data-stu-id="af00e-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="af00e-128">Получение последнего опубликованного определения чертежа с заданным именем в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="af00e-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="af00e-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af00e-129">PARAMETERS</span></span>

### <span data-ttu-id="af00e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af00e-130">-DefaultProfile</span></span>
<span data-ttu-id="af00e-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af00e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af00e-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="af00e-132">-LatestPublished</span></span>
<span data-ttu-id="af00e-133">Последний опубликованный флаг определения чертежей.</span><span class="sxs-lookup"><span data-stu-id="af00e-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="af00e-134">Если этот параметр установлен, выполнение возвращает последнюю опубликованную версию определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="af00e-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="af00e-135">По умолчанию используется значение false.</span><span class="sxs-lookup"><span data-stu-id="af00e-135">Defaults to false.</span></span>

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

### <span data-ttu-id="af00e-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="af00e-136">-ManagementGroupId</span></span>
<span data-ttu-id="af00e-137">Идентификатор группы управления, в которой хранится определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="af00e-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="af00e-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af00e-138">-Name</span></span>
<span data-ttu-id="af00e-139">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="af00e-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="af00e-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af00e-140">-SubscriptionId</span></span>
<span data-ttu-id="af00e-141">Идентификатор подписки, в которой сохраняется определение.</span><span class="sxs-lookup"><span data-stu-id="af00e-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="af00e-142">-Version</span><span class="sxs-lookup"><span data-stu-id="af00e-142">-Version</span></span>
<span data-ttu-id="af00e-143">Версия определений опубликованных чертежей.</span><span class="sxs-lookup"><span data-stu-id="af00e-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="af00e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af00e-144">CommonParameters</span></span>
<span data-ttu-id="af00e-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af00e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af00e-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af00e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af00e-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af00e-147">INPUTS</span></span>

### <span data-ttu-id="af00e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="af00e-148">System.String</span></span>

## <span data-ttu-id="af00e-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af00e-149">OUTPUTS</span></span>

### <span data-ttu-id="af00e-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="af00e-150">System.Object</span></span>
## <span data-ttu-id="af00e-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="af00e-151">NOTES</span></span>

## <span data-ttu-id="af00e-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af00e-152">RELATED LINKS</span></span>
