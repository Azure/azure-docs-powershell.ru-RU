---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 7366e263f6106d2d332daab95f029d07c824aa90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727632"
---
# <span data-ttu-id="c5308-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="c5308-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="c5308-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5308-102">SYNOPSIS</span></span>
<span data-ttu-id="c5308-103">Обновите определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="c5308-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="c5308-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5308-104">SYNTAX</span></span>

### <span data-ttu-id="c5308-105">UpdateBlueprintBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5308-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5308-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c5308-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5308-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5308-107">DESCRIPTION</span></span>
<span data-ttu-id="c5308-108">Обновите определение чертежа и сохраните его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="c5308-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="c5308-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5308-109">EXAMPLES</span></span>

### <span data-ttu-id="c5308-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5308-110">Example 1</span></span>
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

<span data-ttu-id="c5308-111">Обновление определения схемы с использованием новых параметров.</span><span class="sxs-lookup"><span data-stu-id="c5308-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="c5308-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5308-112">PARAMETERS</span></span>

### <span data-ttu-id="c5308-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="c5308-113">-BlueprintFile</span></span>
<span data-ttu-id="c5308-114">Путь к JSON-файлу, который планируется на диске.</span><span class="sxs-lookup"><span data-stu-id="c5308-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="c5308-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5308-115">-DefaultProfile</span></span>
<span data-ttu-id="c5308-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5308-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5308-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c5308-117">-ManagementGroupId</span></span>
<span data-ttu-id="c5308-118">Идентификатор группы управления, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="c5308-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="c5308-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5308-119">-Name</span></span>
<span data-ttu-id="c5308-120">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="c5308-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="c5308-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5308-121">-SubscriptionId</span></span>
<span data-ttu-id="c5308-122">Идентификатор подписки, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="c5308-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="c5308-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5308-123">-Confirm</span></span>
<span data-ttu-id="c5308-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5308-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5308-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5308-125">-WhatIf</span></span>
<span data-ttu-id="c5308-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5308-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5308-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5308-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5308-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5308-128">CommonParameters</span></span>
<span data-ttu-id="c5308-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5308-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c5308-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5308-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5308-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5308-131">INPUTS</span></span>

### <span data-ttu-id="c5308-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c5308-132">System.String</span></span>

## <span data-ttu-id="c5308-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5308-133">OUTPUTS</span></span>

### <span data-ttu-id="c5308-134">Microsoft. Azure. Commands. чертеж. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="c5308-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="c5308-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5308-135">NOTES</span></span>

## <span data-ttu-id="c5308-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5308-136">RELATED LINKS</span></span>
