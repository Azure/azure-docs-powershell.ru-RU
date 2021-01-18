---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518925"
---
# <span data-ttu-id="0049c-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0049c-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="0049c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0049c-102">SYNOPSIS</span></span>
<span data-ttu-id="0049c-103">Удаляет конвейер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0049c-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="0049c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0049c-104">SYNTAX</span></span>

### <span data-ttu-id="0049c-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0049c-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0049c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0049c-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0049c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0049c-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0049c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0049c-108">DESCRIPTION</span></span>
<span data-ttu-id="0049c-109">Новый Remove-AzDataFactoryV2Pipeline удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="0049c-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="0049c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0049c-110">EXAMPLES</span></span>

### <span data-ttu-id="0049c-111">Пример 1. Удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="0049c-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="0049c-112">Этот cmdlet удаляет канал DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0049c-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="0049c-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="0049c-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="0049c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0049c-114">PARAMETERS</span></span>

### <span data-ttu-id="0049c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0049c-115">-DataFactoryName</span></span>
<span data-ttu-id="0049c-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0049c-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0049c-117">Этот cmdlet удаляет канал из фабрики данных, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0049c-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0049c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0049c-118">-DefaultProfile</span></span>
<span data-ttu-id="0049c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0049c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0049c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0049c-120">-Force</span></span>
<span data-ttu-id="0049c-121">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0049c-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0049c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0049c-122">-InputObject</span></span>
<span data-ttu-id="0049c-123">Определяет объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="0049c-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="0049c-124">Этот cmdlet удаляет канал, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0049c-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="0049c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0049c-125">-Name</span></span>
<span data-ttu-id="0049c-126">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0049c-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="0049c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0049c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0049c-128">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0049c-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0049c-129">Этот cmdlet удаляет канал из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0049c-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0049c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0049c-130">-ResourceId</span></span>
<span data-ttu-id="0049c-131">ИД ресурса Azure для конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0049c-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="0049c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0049c-132">-Confirm</span></span>
<span data-ttu-id="0049c-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0049c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0049c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0049c-134">-WhatIf</span></span>
<span data-ttu-id="0049c-135">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0049c-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0049c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0049c-136">CommonParameters</span></span>
<span data-ttu-id="0049c-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0049c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0049c-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0049c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0049c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0049c-139">INPUTS</span></span>

### <span data-ttu-id="0049c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="0049c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="0049c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0049c-141">System.String</span></span>

## <span data-ttu-id="0049c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0049c-142">OUTPUTS</span></span>

### <span data-ttu-id="0049c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0049c-143">System.Boolean</span></span>

## <span data-ttu-id="0049c-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0049c-144">NOTES</span></span>
<span data-ttu-id="0049c-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="0049c-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0049c-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0049c-146">RELATED LINKS</span></span>

[<span data-ttu-id="0049c-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0049c-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0049c-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0049c-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0049c-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0049c-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

