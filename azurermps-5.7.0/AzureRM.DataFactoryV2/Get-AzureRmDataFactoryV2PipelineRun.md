---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568604"
---
# <span data-ttu-id="737c3-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="737c3-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="737c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="737c3-102">SYNOPSIS</span></span>
<span data-ttu-id="737c3-103">Получает сведения о выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="737c3-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="737c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="737c3-104">SYNTAX</span></span>

### <span data-ttu-id="737c3-105">ByFactoryNameByRunId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="737c3-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737c3-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="737c3-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737c3-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="737c3-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="737c3-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="737c3-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737c3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="737c3-109">DESCRIPTION</span></span>
<span data-ttu-id="737c3-110">Команда **Get-AzureRmDataFactoryV2PipelineRun** возвращает сведения о запусках для указанного конвейера.</span><span class="sxs-lookup"><span data-stu-id="737c3-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="737c3-111">Если указан PipelineRunId, он отображает сведения для запуска с этим ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="737c3-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="737c3-112">Если PipelineRunId не указан, выводятся сведения обо всех запусках для указанного конвейера между значениями LastUpdatedAfter и LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="737c3-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="737c3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="737c3-113">EXAMPLES</span></span>

### <span data-ttu-id="737c3-114">Пример 1: получение сведений о выполнении pipline</span><span class="sxs-lookup"><span data-stu-id="737c3-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :
```

<span data-ttu-id="737c3-115">Эта команда получает подробные сведения о выполнении конвейера с ИДЕНТИФИКАТОРом "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="737c3-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="737c3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="737c3-116">PARAMETERS</span></span>

### <span data-ttu-id="737c3-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="737c3-117">-DataFactory</span></span>
<span data-ttu-id="737c3-118">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="737c3-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="737c3-119">-DataFactoryName</span></span>
<span data-ttu-id="737c3-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="737c3-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737c3-121">-DefaultProfile</span></span>
<span data-ttu-id="737c3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="737c3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="737c3-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="737c3-124">Время, по истечении которого выполнение конвейера было Обновлено в ISO8601 формате.</span><span class="sxs-lookup"><span data-stu-id="737c3-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="737c3-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="737c3-126">Время, в течение которого выполнение конвейера было Обновлено в формате ISO8601 или до него.</span><span class="sxs-lookup"><span data-stu-id="737c3-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="737c3-127">-PipelineName</span></span>
<span data-ttu-id="737c3-128">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="737c3-128">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="737c3-129">-PipelineRunId</span></span>
<span data-ttu-id="737c3-130">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="737c3-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737c3-131">-ResourceGroupName</span></span>
<span data-ttu-id="737c3-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="737c3-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737c3-133">CommonParameters</span></span>
<span data-ttu-id="737c3-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="737c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737c3-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737c3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737c3-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="737c3-136">INPUTS</span></span>

### <span data-ttu-id="737c3-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="737c3-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="737c3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="737c3-138">System.String</span></span>

## <span data-ttu-id="737c3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="737c3-139">OUTPUTS</span></span>

### <span data-ttu-id="737c3-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="737c3-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="737c3-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="737c3-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="737c3-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="737c3-142">NOTES</span></span>

## <span data-ttu-id="737c3-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="737c3-143">RELATED LINKS</span></span>

[<span data-ttu-id="737c3-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="737c3-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="737c3-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="737c3-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

