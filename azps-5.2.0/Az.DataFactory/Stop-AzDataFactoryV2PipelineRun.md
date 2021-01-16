---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406300"
---
# <span data-ttu-id="70474-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="70474-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="70474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70474-102">SYNOPSIS</span></span>
<span data-ttu-id="70474-103">Остановка конвейера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="70474-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="70474-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70474-104">SYNTAX</span></span>

### <span data-ttu-id="70474-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70474-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70474-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="70474-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70474-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="70474-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70474-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70474-108">DESCRIPTION</span></span>
<span data-ttu-id="70474-109">**Cmdlet Stop-AzDataFactoryV2PipelineRun** останавливает запуск конвейера в фабрике данных, заданной с кодом запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="70474-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="70474-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70474-110">EXAMPLES</span></span>

### <span data-ttu-id="70474-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="70474-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="70474-112">Эта команда останавливает работу конвейера с помощью id b9730a13-aa12-4926-a8b3-8e3a974ab0bd на заводском wikiADF.</span><span class="sxs-lookup"><span data-stu-id="70474-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="70474-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70474-113">PARAMETERS</span></span>

### <span data-ttu-id="70474-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="70474-114">-DataFactory</span></span>
<span data-ttu-id="70474-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="70474-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70474-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="70474-116">-DataFactoryName</span></span>
<span data-ttu-id="70474-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="70474-117">The data factory name.</span></span>

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

### <span data-ttu-id="70474-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70474-118">-DefaultProfile</span></span>
<span data-ttu-id="70474-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70474-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70474-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70474-120">-InputObject</span></span>
<span data-ttu-id="70474-121">Run ID of the pipeline.</span><span class="sxs-lookup"><span data-stu-id="70474-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70474-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70474-122">-PassThru</span></span>
<span data-ttu-id="70474-123">Если для указанного cmdlet задано написание истина в случае успешного написания.</span><span class="sxs-lookup"><span data-stu-id="70474-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="70474-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="70474-124">-PipelineRunId</span></span>
<span data-ttu-id="70474-125">Run ID of the pipeline.</span><span class="sxs-lookup"><span data-stu-id="70474-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70474-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70474-126">-ResourceGroupName</span></span>
<span data-ttu-id="70474-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70474-127">The resource group name.</span></span>

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

### <span data-ttu-id="70474-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70474-128">-Confirm</span></span>
<span data-ttu-id="70474-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="70474-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70474-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70474-130">-WhatIf</span></span>
<span data-ttu-id="70474-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70474-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70474-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="70474-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70474-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70474-133">CommonParameters</span></span>
<span data-ttu-id="70474-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70474-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70474-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70474-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70474-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70474-136">INPUTS</span></span>

### <span data-ttu-id="70474-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="70474-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="70474-138">System.String</span><span class="sxs-lookup"><span data-stu-id="70474-138">System.String</span></span>

### <span data-ttu-id="70474-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="70474-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="70474-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70474-140">OUTPUTS</span></span>

### <span data-ttu-id="70474-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70474-141">System.Boolean</span></span>

## <span data-ttu-id="70474-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70474-142">NOTES</span></span>

## <span data-ttu-id="70474-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70474-143">RELATED LINKS</span></span>