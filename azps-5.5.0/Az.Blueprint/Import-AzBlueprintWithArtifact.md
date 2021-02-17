---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216020"
---
# <span data-ttu-id="0c4e7-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="0c4e7-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="0c4e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4e7-103">Импорт файла чертежа в формате JSON в объект чертежа и сохранение его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="0c4e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c4e7-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c4e7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c4e7-105">DESCRIPTION</span></span>
<span data-ttu-id="0c4e7-106">Импорт определения чертежа с его артефактами.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="0c4e7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c4e7-107">EXAMPLES</span></span>

### <span data-ttu-id="0c4e7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c4e7-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="0c4e7-109">Импорт определения чертежа с его артефактами и сохранение в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="0c4e7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c4e7-110">PARAMETERS</span></span>

### <span data-ttu-id="0c4e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4e7-111">-DefaultProfile</span></span>
<span data-ttu-id="0c4e7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c4e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0c4e7-113">-Force</span></span>
<span data-ttu-id="0c4e7-114">Если задается true, выполнение не будет запросить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-114">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4e7-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="0c4e7-115">-IncludeSubFolders</span></span>
<span data-ttu-id="0c4e7-116">Если задается true, артефакт во встроит в нее.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-116">When set to true, artifact in the subfolders will be included.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4e7-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="0c4e7-117">-InputPath</span></span>
<span data-ttu-id="0c4e7-118">Путь к файлу Blueprint JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="0c4e7-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0c4e7-119">-ManagementGroupId</span></span>
<span data-ttu-id="0c4e7-120">ИД группы управления, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4e7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0c4e7-121">-Name</span></span>
<span data-ttu-id="0c4e7-122">Название определения схемы.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="0c4e7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c4e7-123">-PassThru</span></span>
<span data-ttu-id="0c4e7-124">При этом будет возвращен объект, представляющий определение импортируемого чертежа.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="0c4e7-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c4e7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c4e7-126">-SubscriptionId</span></span>
<span data-ttu-id="0c4e7-127">ИД подписки, где находится или будет сохранено определение схемы.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c4e7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c4e7-128">-Confirm</span></span>
<span data-ttu-id="0c4e7-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c4e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c4e7-130">-WhatIf</span></span>
<span data-ttu-id="0c4e7-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c4e7-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c4e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4e7-133">CommonParameters</span></span>
<span data-ttu-id="0c4e7-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c4e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4e7-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c4e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4e7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c4e7-136">INPUTS</span></span>

### <span data-ttu-id="0c4e7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0c4e7-137">System.String</span></span>

## <span data-ttu-id="0c4e7-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c4e7-138">OUTPUTS</span></span>

### <span data-ttu-id="0c4e7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0c4e7-139">System.String</span></span>

## <span data-ttu-id="0c4e7-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c4e7-140">NOTES</span></span>

## <span data-ttu-id="0c4e7-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c4e7-141">RELATED LINKS</span></span>
