---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: eb832037080550a1a22c3cacce2386eba7c4e6f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971139"
---
# <span data-ttu-id="379de-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="379de-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="379de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379de-102">SYNOPSIS</span></span>
<span data-ttu-id="379de-103">Удаляет конвейер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="379de-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="379de-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="379de-104">SYNTAX</span></span>

### <span data-ttu-id="379de-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="379de-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379de-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="379de-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379de-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="379de-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="379de-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="379de-108">DESCRIPTION</span></span>
<span data-ttu-id="379de-109">Новый Remove-AzDataFactoryV2Pipeline удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="379de-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="379de-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="379de-110">EXAMPLES</span></span>

### <span data-ttu-id="379de-111">Пример 1. Удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="379de-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="379de-112">Этот cmdlet удаляет конвейер под названием DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="379de-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="379de-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="379de-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="379de-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="379de-114">PARAMETERS</span></span>

### <span data-ttu-id="379de-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="379de-115">-DataFactoryName</span></span>
<span data-ttu-id="379de-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="379de-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="379de-117">Этот cmdlet удаляет канал из фабрики данных, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="379de-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379de-118">-DefaultProfile</span></span>
<span data-ttu-id="379de-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="379de-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="379de-120">-Force</span><span class="sxs-lookup"><span data-stu-id="379de-120">-Force</span></span>
<span data-ttu-id="379de-121">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="379de-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="379de-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="379de-122">-InputObject</span></span>
<span data-ttu-id="379de-123">Определяет объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="379de-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="379de-124">Этот cmdlet удаляет канал, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="379de-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="379de-125">-Name</span><span class="sxs-lookup"><span data-stu-id="379de-125">-Name</span></span>
<span data-ttu-id="379de-126">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="379de-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379de-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379de-127">-ResourceGroupName</span></span>
<span data-ttu-id="379de-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="379de-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="379de-129">Этот cmdlet удаляет канал из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="379de-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379de-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="379de-130">-ResourceId</span></span>
<span data-ttu-id="379de-131">ИД ресурса Azure для конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="379de-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379de-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="379de-132">-Confirm</span></span>
<span data-ttu-id="379de-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="379de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="379de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="379de-134">-WhatIf</span></span>
<span data-ttu-id="379de-135">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="379de-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="379de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379de-136">CommonParameters</span></span>
<span data-ttu-id="379de-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379de-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="379de-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379de-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="379de-139">INPUTS</span></span>

### <span data-ttu-id="379de-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="379de-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="379de-141">System.String</span><span class="sxs-lookup"><span data-stu-id="379de-141">System.String</span></span>

## <span data-ttu-id="379de-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="379de-142">OUTPUTS</span></span>

### <span data-ttu-id="379de-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="379de-143">System.Boolean</span></span>

## <span data-ttu-id="379de-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="379de-144">NOTES</span></span>
<span data-ttu-id="379de-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="379de-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="379de-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="379de-146">RELATED LINKS</span></span>

[<span data-ttu-id="379de-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="379de-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="379de-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="379de-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="379de-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="379de-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

