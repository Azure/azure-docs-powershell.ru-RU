---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 5511be0e20c99a6a120e2f7591287b9ee17b0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965096"
---
# <span data-ttu-id="1b48c-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="1b48c-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="1b48c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b48c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b48c-103">Обновив определение схемы.</span><span class="sxs-lookup"><span data-stu-id="1b48c-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="1b48c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b48c-104">SYNTAX</span></span>

### <span data-ttu-id="1b48c-105">UpdateBlueprintBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b48c-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b48c-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1b48c-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b48c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b48c-107">DESCRIPTION</span></span>
<span data-ttu-id="1b48c-108">Обновите определение схемы и сохраните его в пределах указанной подписки или группы управления.</span><span class="sxs-lookup"><span data-stu-id="1b48c-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="1b48c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b48c-109">EXAMPLES</span></span>

### <span data-ttu-id="1b48c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b48c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="1b48c-111">Обновив определение схемы, ввести новые параметры.</span><span class="sxs-lookup"><span data-stu-id="1b48c-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="1b48c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b48c-112">PARAMETERS</span></span>

### <span data-ttu-id="1b48c-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="1b48c-113">-BlueprintFile</span></span>
<span data-ttu-id="1b48c-114">Путь к файлу Blueprint JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="1b48c-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="1b48c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b48c-115">-DefaultProfile</span></span>
<span data-ttu-id="1b48c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b48c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b48c-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1b48c-117">-ManagementGroupId</span></span>
<span data-ttu-id="1b48c-118">ИД группы управления, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="1b48c-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b48c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1b48c-119">-Name</span></span>
<span data-ttu-id="1b48c-120">Название определения схемы.</span><span class="sxs-lookup"><span data-stu-id="1b48c-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="1b48c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b48c-121">-SubscriptionId</span></span>
<span data-ttu-id="1b48c-122">ИД подписки, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="1b48c-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b48c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b48c-123">-Confirm</span></span>
<span data-ttu-id="1b48c-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1b48c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b48c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b48c-125">-WhatIf</span></span>
<span data-ttu-id="1b48c-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b48c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b48c-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b48c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b48c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b48c-128">CommonParameters</span></span>
<span data-ttu-id="1b48c-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b48c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b48c-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b48c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b48c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b48c-131">INPUTS</span></span>

### <span data-ttu-id="1b48c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1b48c-132">System.String</span></span>

## <span data-ttu-id="1b48c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b48c-133">OUTPUTS</span></span>

### <span data-ttu-id="1b48c-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="1b48c-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="1b48c-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b48c-135">NOTES</span></span>

## <span data-ttu-id="1b48c-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b48c-136">RELATED LINKS</span></span>
