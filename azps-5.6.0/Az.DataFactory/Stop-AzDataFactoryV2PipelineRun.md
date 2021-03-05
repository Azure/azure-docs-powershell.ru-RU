---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 096ee403a0ee12c80462a1fb87db4378e3d86f01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998469"
---
# <span data-ttu-id="a9d5f-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a9d5f-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="a9d5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d5f-103">Остановка конвейера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="a9d5f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9d5f-104">SYNTAX</span></span>

### <span data-ttu-id="a9d5f-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9d5f-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d5f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9d5f-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9d5f-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a9d5f-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d5f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9d5f-108">DESCRIPTION</span></span>
<span data-ttu-id="a9d5f-109">**Cmdlet Stop-AzDataFactoryV2PipelineRun** останавливает запуск конвейера в фабрике данных, заданной с кодом запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="a9d5f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9d5f-110">EXAMPLES</span></span>

### <span data-ttu-id="a9d5f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a9d5f-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="a9d5f-112">Эта команда останавливает работу конвейера с помощью id b9730a13-aa12-4926-a8b3-8e3a974ab0bd на заводском wikiADF.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="a9d5f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9d5f-113">PARAMETERS</span></span>

### <span data-ttu-id="a9d5f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a9d5f-114">-DataFactory</span></span>
<span data-ttu-id="a9d5f-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-115">The data factory object.</span></span>

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

### <span data-ttu-id="a9d5f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a9d5f-116">-DataFactoryName</span></span>
<span data-ttu-id="a9d5f-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-117">The data factory name.</span></span>

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

### <span data-ttu-id="a9d5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d5f-118">-DefaultProfile</span></span>
<span data-ttu-id="a9d5f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d5f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9d5f-120">-InputObject</span></span>
<span data-ttu-id="a9d5f-121">Run ID of the pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="a9d5f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9d5f-122">-PassThru</span></span>
<span data-ttu-id="a9d5f-123">Если для указанного cmdlet задано написание истина в случае успешного написания.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="a9d5f-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a9d5f-124">-PipelineRunId</span></span>
<span data-ttu-id="a9d5f-125">Запустите ИД конвейера.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="a9d5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9d5f-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-127">The resource group name.</span></span>

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

### <span data-ttu-id="a9d5f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9d5f-128">-Confirm</span></span>
<span data-ttu-id="a9d5f-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d5f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d5f-130">-WhatIf</span></span>
<span data-ttu-id="a9d5f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d5f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d5f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d5f-133">CommonParameters</span></span>
<span data-ttu-id="a9d5f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d5f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d5f-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d5f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d5f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9d5f-136">INPUTS</span></span>

### <span data-ttu-id="a9d5f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="a9d5f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="a9d5f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a9d5f-138">System.String</span></span>

### <span data-ttu-id="a9d5f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9d5f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a9d5f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9d5f-140">OUTPUTS</span></span>

### <span data-ttu-id="a9d5f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9d5f-141">System.Boolean</span></span>

## <span data-ttu-id="a9d5f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9d5f-142">NOTES</span></span>

## <span data-ttu-id="a9d5f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9d5f-143">RELATED LINKS</span></span>
