---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 790a74ef5a296dbc90e9c1db16678b8c1bacf071
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234980"
---
# <span data-ttu-id="c76f0-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="c76f0-101">New-AzBlueprint</span></span>

## <span data-ttu-id="c76f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c76f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c76f0-103">Создайте новое определение схемы и сохраните его в указанной группе подписок или управления.</span><span class="sxs-lookup"><span data-stu-id="c76f0-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="c76f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c76f0-104">SYNTAX</span></span>

### <span data-ttu-id="c76f0-105">CreateBlueprintBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c76f0-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c76f0-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c76f0-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c76f0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c76f0-107">DESCRIPTION</span></span>
<span data-ttu-id="c76f0-108">Создайте новое определение схемы.</span><span class="sxs-lookup"><span data-stu-id="c76f0-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="c76f0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c76f0-109">EXAMPLES</span></span>

### <span data-ttu-id="c76f0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c76f0-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="c76f0-111">Создайте новое определение схемы в пределах указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="c76f0-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="c76f0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c76f0-112">PARAMETERS</span></span>

### <span data-ttu-id="c76f0-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="c76f0-113">-BlueprintFile</span></span>
<span data-ttu-id="c76f0-114">Путь к файлу Blueprint JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="c76f0-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76f0-115">-DefaultProfile</span></span>
<span data-ttu-id="c76f0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c76f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c76f0-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c76f0-117">-ManagementGroupId</span></span>
<span data-ttu-id="c76f0-118">ИД группы управления, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="c76f0-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c76f0-119">-Name</span></span>
<span data-ttu-id="c76f0-120">Название определения схемы.</span><span class="sxs-lookup"><span data-stu-id="c76f0-120">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f0-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c76f0-121">-SubscriptionId</span></span>
<span data-ttu-id="c76f0-122">ИД подписки, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="c76f0-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76f0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c76f0-123">-Confirm</span></span>
<span data-ttu-id="c76f0-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76f0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c76f0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c76f0-125">-WhatIf</span></span>
<span data-ttu-id="c76f0-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76f0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c76f0-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c76f0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c76f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76f0-128">CommonParameters</span></span>
<span data-ttu-id="c76f0-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c76f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76f0-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c76f0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76f0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c76f0-131">INPUTS</span></span>

### <span data-ttu-id="c76f0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c76f0-132">System.String</span></span>

## <span data-ttu-id="c76f0-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c76f0-133">OUTPUTS</span></span>

### <span data-ttu-id="c76f0-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="c76f0-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="c76f0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c76f0-135">NOTES</span></span>

## <span data-ttu-id="c76f0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c76f0-136">RELATED LINKS</span></span>
