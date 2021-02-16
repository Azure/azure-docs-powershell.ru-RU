---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211956"
---
# <span data-ttu-id="edacb-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="edacb-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="edacb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edacb-102">SYNOPSIS</span></span>
<span data-ttu-id="edacb-103">Экспорт указанного определения чертежа в указанное выходное расположение в качестве файла JSON.</span><span class="sxs-lookup"><span data-stu-id="edacb-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="edacb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="edacb-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edacb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edacb-105">DESCRIPTION</span></span>
<span data-ttu-id="edacb-106">Экспорт определения чертежа с его артефактами и сохранение на диск.</span><span class="sxs-lookup"><span data-stu-id="edacb-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="edacb-107">Этот cmdlet экспортирует последнюю версию (черновик или опубликованную) документа.</span><span class="sxs-lookup"><span data-stu-id="edacb-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="edacb-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="edacb-108">EXAMPLES</span></span>

### <span data-ttu-id="edacb-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="edacb-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="edacb-110">Экспорт определения чертежа с его артефактами и сохранение на диск.</span><span class="sxs-lookup"><span data-stu-id="edacb-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="edacb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edacb-111">PARAMETERS</span></span>

### <span data-ttu-id="edacb-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="edacb-112">-Blueprint</span></span>
<span data-ttu-id="edacb-113">Объект определения схемы, который нужно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="edacb-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edacb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edacb-114">-DefaultProfile</span></span>
<span data-ttu-id="edacb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edacb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edacb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="edacb-116">-Force</span></span>
<span data-ttu-id="edacb-117">Если задается true, выполнение не будет запросить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="edacb-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="edacb-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="edacb-118">-OutputPath</span></span>
<span data-ttu-id="edacb-119">Путь к файлу на диске, где экспортируется определение Blueprint в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="edacb-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="edacb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edacb-120">-PassThru</span></span>
<span data-ttu-id="edacb-121">При этом будет возвращен объект, представляющий экспортируемую схему.</span><span class="sxs-lookup"><span data-stu-id="edacb-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="edacb-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="edacb-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="edacb-123">-Version</span><span class="sxs-lookup"><span data-stu-id="edacb-123">-Version</span></span>
<span data-ttu-id="edacb-124">Опубликованная версия определения схемы.</span><span class="sxs-lookup"><span data-stu-id="edacb-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="edacb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edacb-125">-Confirm</span></span>
<span data-ttu-id="edacb-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edacb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edacb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edacb-127">-WhatIf</span></span>
<span data-ttu-id="edacb-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edacb-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edacb-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="edacb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edacb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edacb-130">CommonParameters</span></span>
<span data-ttu-id="edacb-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edacb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edacb-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edacb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edacb-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edacb-133">INPUTS</span></span>

### <span data-ttu-id="edacb-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="edacb-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="edacb-135">System.String</span><span class="sxs-lookup"><span data-stu-id="edacb-135">System.String</span></span>

## <span data-ttu-id="edacb-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edacb-136">OUTPUTS</span></span>

### <span data-ttu-id="edacb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="edacb-137">System.String</span></span>

## <span data-ttu-id="edacb-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="edacb-138">NOTES</span></span>

## <span data-ttu-id="edacb-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edacb-139">RELATED LINKS</span></span>
