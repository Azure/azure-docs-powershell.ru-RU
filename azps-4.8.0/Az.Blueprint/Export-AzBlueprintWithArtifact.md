---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078483"
---
# <span data-ttu-id="770bd-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="770bd-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="770bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="770bd-102">SYNOPSIS</span></span>
<span data-ttu-id="770bd-103">Экспортировать определение указанного чертежа в указанное расположение выходных файлов в виде JSON-файла.</span><span class="sxs-lookup"><span data-stu-id="770bd-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="770bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="770bd-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="770bd-105">DESCRIPTION</span></span>
<span data-ttu-id="770bd-106">Экспортируйте определение чертежа вместе с артефактами и сохраните его на диск.</span><span class="sxs-lookup"><span data-stu-id="770bd-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="770bd-107">Этот командлет экспортирует последнюю версию проекта (черновика или опубликована).</span><span class="sxs-lookup"><span data-stu-id="770bd-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="770bd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="770bd-108">EXAMPLES</span></span>

### <span data-ttu-id="770bd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="770bd-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="770bd-110">Экспортируйте определение чертежа вместе с артефактами и сохраните его на диск.</span><span class="sxs-lookup"><span data-stu-id="770bd-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="770bd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="770bd-111">PARAMETERS</span></span>

### <span data-ttu-id="770bd-112">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="770bd-112">-Blueprint</span></span>
<span data-ttu-id="770bd-113">Объект определения чертежей, который нужно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="770bd-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="770bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770bd-114">-DefaultProfile</span></span>
<span data-ttu-id="770bd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="770bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770bd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="770bd-116">-Force</span></span>
<span data-ttu-id="770bd-117">Если задано значение "true", при выполнении не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="770bd-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="770bd-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="770bd-118">-OutputPath</span></span>
<span data-ttu-id="770bd-119">Путь к файлу на диске, на который нужно экспортировать определение чертежа в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="770bd-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="770bd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="770bd-120">-PassThru</span></span>
<span data-ttu-id="770bd-121">При установке командлет возвращает объект, который представляет экспортированное определение для этого чертежа.</span><span class="sxs-lookup"><span data-stu-id="770bd-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="770bd-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="770bd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="770bd-123">-Version</span><span class="sxs-lookup"><span data-stu-id="770bd-123">-Version</span></span>
<span data-ttu-id="770bd-124">Версия определений опубликованных чертежей.</span><span class="sxs-lookup"><span data-stu-id="770bd-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="770bd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="770bd-125">-Confirm</span></span>
<span data-ttu-id="770bd-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="770bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770bd-127">-WhatIf</span></span>
<span data-ttu-id="770bd-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="770bd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="770bd-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="770bd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770bd-130">CommonParameters</span></span>
<span data-ttu-id="770bd-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="770bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770bd-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="770bd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770bd-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="770bd-133">INPUTS</span></span>

### <span data-ttu-id="770bd-134">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="770bd-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="770bd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="770bd-135">System.String</span></span>

## <span data-ttu-id="770bd-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="770bd-136">OUTPUTS</span></span>

### <span data-ttu-id="770bd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="770bd-137">System.String</span></span>

## <span data-ttu-id="770bd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="770bd-138">NOTES</span></span>

## <span data-ttu-id="770bd-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="770bd-139">RELATED LINKS</span></span>
