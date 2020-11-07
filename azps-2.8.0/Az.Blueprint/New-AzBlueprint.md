---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 3213d5dbb981d9cc7d7871ce97f9fd78f375a59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727635"
---
# <span data-ttu-id="7e3f7-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="7e3f7-101">New-AzBlueprint</span></span>

## <span data-ttu-id="7e3f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3f7-103">Создание нового определения чертежа и сохранение его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="7e3f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e3f7-104">SYNTAX</span></span>

### <span data-ttu-id="7e3f7-105">CreateBlueprintBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e3f7-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e3f7-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="7e3f7-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e3f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e3f7-107">DESCRIPTION</span></span>
<span data-ttu-id="7e3f7-108">Создание нового определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="7e3f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e3f7-109">EXAMPLES</span></span>

### <span data-ttu-id="7e3f7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e3f7-110">Example 1</span></span>
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

<span data-ttu-id="7e3f7-111">Создание нового определения чертежа в рамках указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="7e3f7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e3f7-112">PARAMETERS</span></span>

### <span data-ttu-id="7e3f7-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="7e3f7-113">-BlueprintFile</span></span>
<span data-ttu-id="7e3f7-114">Путь к JSON-файлу, который планируется на диске.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3f7-115">-DefaultProfile</span></span>
<span data-ttu-id="7e3f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e3f7-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7e3f7-117">-ManagementGroupId</span></span>
<span data-ttu-id="7e3f7-118">Идентификатор группы управления, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3f7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e3f7-119">-Name</span></span>
<span data-ttu-id="7e3f7-120">Имя определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3f7-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e3f7-121">-SubscriptionId</span></span>
<span data-ttu-id="7e3f7-122">Идентификатор подписки, в которой должно быть сохранено определение.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3f7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e3f7-123">-Confirm</span></span>
<span data-ttu-id="7e3f7-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3f7-125">-WhatIf</span></span>
<span data-ttu-id="7e3f7-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e3f7-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3f7-128">CommonParameters</span></span>
<span data-ttu-id="7e3f7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7e3f7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e3f7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3f7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e3f7-131">INPUTS</span></span>

### <span data-ttu-id="7e3f7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7e3f7-132">System.String</span></span>

## <span data-ttu-id="7e3f7-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e3f7-133">OUTPUTS</span></span>

### <span data-ttu-id="7e3f7-134">Microsoft. Azure. Commands. чертеж. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="7e3f7-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="7e3f7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e3f7-135">NOTES</span></span>

## <span data-ttu-id="7e3f7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e3f7-136">RELATED LINKS</span></span>
