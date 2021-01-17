---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 790a74ef5a296dbc90e9c1db16678b8c1bacf071
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392055"
---
# <span data-ttu-id="a10bb-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a10bb-101">New-AzBlueprint</span></span>

## <span data-ttu-id="a10bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a10bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a10bb-103">Создайте новое определение схемы и сохраните его в указанной группе подписок или управления.</span><span class="sxs-lookup"><span data-stu-id="a10bb-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="a10bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a10bb-104">SYNTAX</span></span>

### <span data-ttu-id="a10bb-105">CreateBlueprintBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a10bb-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a10bb-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a10bb-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a10bb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a10bb-107">DESCRIPTION</span></span>
<span data-ttu-id="a10bb-108">Создайте новое определение схемы.</span><span class="sxs-lookup"><span data-stu-id="a10bb-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="a10bb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a10bb-109">EXAMPLES</span></span>

### <span data-ttu-id="a10bb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a10bb-110">Example 1</span></span>
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

<span data-ttu-id="a10bb-111">Создайте новый чертеж в пределах указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="a10bb-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="a10bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a10bb-112">PARAMETERS</span></span>

### <span data-ttu-id="a10bb-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="a10bb-113">-BlueprintFile</span></span>
<span data-ttu-id="a10bb-114">Путь к файлу Blueprint JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="a10bb-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="a10bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10bb-115">-DefaultProfile</span></span>
<span data-ttu-id="a10bb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a10bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a10bb-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a10bb-117">-ManagementGroupId</span></span>
<span data-ttu-id="a10bb-118">ИД группы управления, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="a10bb-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="a10bb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a10bb-119">-Name</span></span>
<span data-ttu-id="a10bb-120">Название определения схемы.</span><span class="sxs-lookup"><span data-stu-id="a10bb-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="a10bb-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a10bb-121">-SubscriptionId</span></span>
<span data-ttu-id="a10bb-122">ИД подписки, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="a10bb-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="a10bb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a10bb-123">-Confirm</span></span>
<span data-ttu-id="a10bb-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a10bb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a10bb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a10bb-125">-WhatIf</span></span>
<span data-ttu-id="a10bb-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a10bb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a10bb-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a10bb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a10bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10bb-128">CommonParameters</span></span>
<span data-ttu-id="a10bb-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a10bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10bb-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a10bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10bb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a10bb-131">INPUTS</span></span>

### <span data-ttu-id="a10bb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a10bb-132">System.String</span></span>

## <span data-ttu-id="a10bb-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a10bb-133">OUTPUTS</span></span>

### <span data-ttu-id="a10bb-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="a10bb-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="a10bb-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a10bb-135">NOTES</span></span>

## <span data-ttu-id="a10bb-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a10bb-136">RELATED LINKS</span></span>
