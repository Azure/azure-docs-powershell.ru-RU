---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243673"
---
# <span data-ttu-id="80a51-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="80a51-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="80a51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80a51-102">SYNOPSIS</span></span>
<span data-ttu-id="80a51-103">Останавливает выполнение конвейера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="80a51-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="80a51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80a51-104">SYNTAX</span></span>

### <span data-ttu-id="80a51-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80a51-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80a51-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="80a51-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a51-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="80a51-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a51-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80a51-108">DESCRIPTION</span></span>
<span data-ttu-id="80a51-109">Командлет **Stop-AzDataFactoryV2PipelineRun** останавливает выполнение конвейера в фабрике данных, указанной с помощью идентификатора запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="80a51-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="80a51-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80a51-110">EXAMPLES</span></span>

### <span data-ttu-id="80a51-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="80a51-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="80a51-112">Эта команда останавливает процесс конвейера с ИД b9730a13-AA12-4926-a8b3-8e3a974ab0bd в фабрике WikiADF.</span><span class="sxs-lookup"><span data-stu-id="80a51-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="80a51-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80a51-113">PARAMETERS</span></span>

### <span data-ttu-id="80a51-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="80a51-114">-DataFactory</span></span>
<span data-ttu-id="80a51-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="80a51-115">The data factory object.</span></span>

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

### <span data-ttu-id="80a51-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="80a51-116">-DataFactoryName</span></span>
<span data-ttu-id="80a51-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="80a51-117">The data factory name.</span></span>

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

### <span data-ttu-id="80a51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a51-118">-DefaultProfile</span></span>
<span data-ttu-id="80a51-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80a51-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a51-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80a51-120">-InputObject</span></span>
<span data-ttu-id="80a51-121">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="80a51-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="80a51-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80a51-122">-PassThru</span></span>
<span data-ttu-id="80a51-123">При успешном указании командлета записать истинную операцию в case.</span><span class="sxs-lookup"><span data-stu-id="80a51-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="80a51-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="80a51-124">-PipelineRunId</span></span>
<span data-ttu-id="80a51-125">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="80a51-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="80a51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a51-126">-ResourceGroupName</span></span>
<span data-ttu-id="80a51-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80a51-127">The resource group name.</span></span>

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

### <span data-ttu-id="80a51-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80a51-128">-Confirm</span></span>
<span data-ttu-id="80a51-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80a51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a51-130">-WhatIf</span></span>
<span data-ttu-id="80a51-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80a51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80a51-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80a51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a51-133">CommonParameters</span></span>
<span data-ttu-id="80a51-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80a51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a51-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a51-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a51-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80a51-136">INPUTS</span></span>

### <span data-ttu-id="80a51-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="80a51-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="80a51-138">System. String</span><span class="sxs-lookup"><span data-stu-id="80a51-138">System.String</span></span>

### <span data-ttu-id="80a51-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="80a51-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="80a51-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80a51-140">OUTPUTS</span></span>

### <span data-ttu-id="80a51-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="80a51-141">System.Boolean</span></span>

## <span data-ttu-id="80a51-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="80a51-142">NOTES</span></span>

## <span data-ttu-id="80a51-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80a51-143">RELATED LINKS</span></span>
