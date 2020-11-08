---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 155bf1a7851f6cc8e3283c66297df811738edd2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065458"
---
# <span data-ttu-id="55f83-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="55f83-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="55f83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55f83-102">SYNOPSIS</span></span>
<span data-ttu-id="55f83-103">Обновите определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="55f83-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="55f83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55f83-104">SYNTAX</span></span>

### <span data-ttu-id="55f83-105">UpdateBlueprintBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55f83-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f83-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="55f83-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f83-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55f83-107">DESCRIPTION</span></span>
<span data-ttu-id="55f83-108">Обновите определение чертежа и сохраните его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="55f83-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="55f83-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55f83-109">EXAMPLES</span></span>

### <span data-ttu-id="55f83-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55f83-110">Example 1</span></span>
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

<span data-ttu-id="55f83-111">Обновление определения схемы с использованием новых параметров.</span><span class="sxs-lookup"><span data-stu-id="55f83-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="55f83-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55f83-112">PARAMETERS</span></span>

### <span data-ttu-id="55f83-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="55f83-113">-BlueprintFile</span></span>
<span data-ttu-id="55f83-114">Путь к JSON-файлу, который планируется на диске.</span><span class="sxs-lookup"><span data-stu-id="55f83-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f83-115">-DefaultProfile</span></span>
<span data-ttu-id="55f83-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55f83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f83-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="55f83-117">-ManagementGroupId</span></span>
<span data-ttu-id="55f83-118">Идентификатор группы управления, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="55f83-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup, ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f83-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55f83-119">-Name</span></span>
<span data-ttu-id="55f83-120">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="55f83-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup, ImportBlueprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f83-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55f83-121">-SubscriptionId</span></span>
<span data-ttu-id="55f83-122">Идентификатор подписки, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="55f83-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, ImportBlueprint, SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f83-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55f83-123">-Confirm</span></span>
<span data-ttu-id="55f83-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55f83-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f83-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f83-125">-WhatIf</span></span>
<span data-ttu-id="55f83-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55f83-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f83-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55f83-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f83-128">CommonParameters</span></span>
<span data-ttu-id="55f83-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55f83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="55f83-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f83-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f83-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55f83-131">INPUTS</span></span>

### <span data-ttu-id="55f83-132">System. String</span><span class="sxs-lookup"><span data-stu-id="55f83-132">System.String</span></span>

## <span data-ttu-id="55f83-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55f83-133">OUTPUTS</span></span>

### <span data-ttu-id="55f83-134">Microsoft. Azure. Commands. чертеж. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="55f83-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="55f83-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="55f83-135">NOTES</span></span>

## <span data-ttu-id="55f83-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55f83-136">RELATED LINKS</span></span>
