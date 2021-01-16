---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414047"
---
# <span data-ttu-id="c1e14-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1e14-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="c1e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1e14-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e14-103">Удаляет конвейер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c1e14-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="c1e14-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c1e14-104">SYNTAX</span></span>

### <span data-ttu-id="c1e14-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1e14-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e14-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1e14-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1e14-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e14-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1e14-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1e14-108">DESCRIPTION</span></span>
<span data-ttu-id="c1e14-109">Новый Remove-AzDataFactoryV2Pipeline удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c1e14-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="c1e14-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c1e14-110">EXAMPLES</span></span>

### <span data-ttu-id="c1e14-111">Пример 1. Удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="c1e14-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="c1e14-112">Этот cmdlet удаляет канал DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c1e14-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="c1e14-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="c1e14-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="c1e14-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1e14-114">PARAMETERS</span></span>

### <span data-ttu-id="c1e14-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c1e14-115">-DataFactoryName</span></span>
<span data-ttu-id="c1e14-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c1e14-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c1e14-117">Этот cmdlet удаляет канал из фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c1e14-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1e14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e14-118">-DefaultProfile</span></span>
<span data-ttu-id="c1e14-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1e14-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1e14-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c1e14-120">-Force</span></span>
<span data-ttu-id="c1e14-121">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c1e14-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c1e14-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1e14-122">-InputObject</span></span>
<span data-ttu-id="c1e14-123">Определяет объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="c1e14-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="c1e14-124">Этот cmdlet удаляет канал, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c1e14-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1e14-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c1e14-125">-Name</span></span>
<span data-ttu-id="c1e14-126">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c1e14-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="c1e14-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e14-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1e14-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c1e14-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c1e14-129">Этот cmdlet удаляет канал из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="c1e14-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1e14-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e14-130">-ResourceId</span></span>
<span data-ttu-id="c1e14-131">ИД ресурса Azure для конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c1e14-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="c1e14-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1e14-132">-Confirm</span></span>
<span data-ttu-id="c1e14-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1e14-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1e14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1e14-134">-WhatIf</span></span>
<span data-ttu-id="c1e14-135">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1e14-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c1e14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e14-136">CommonParameters</span></span>
<span data-ttu-id="c1e14-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1e14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e14-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1e14-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e14-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1e14-139">INPUTS</span></span>

### <span data-ttu-id="c1e14-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c1e14-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="c1e14-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c1e14-141">System.String</span></span>

## <span data-ttu-id="c1e14-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1e14-142">OUTPUTS</span></span>

### <span data-ttu-id="c1e14-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1e14-143">System.Boolean</span></span>

## <span data-ttu-id="c1e14-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c1e14-144">NOTES</span></span>
<span data-ttu-id="c1e14-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="c1e14-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c1e14-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1e14-146">RELATED LINKS</span></span>

[<span data-ttu-id="c1e14-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1e14-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c1e14-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1e14-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c1e14-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c1e14-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

