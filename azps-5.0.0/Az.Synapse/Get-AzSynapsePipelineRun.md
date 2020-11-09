---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316883"
---
# <span data-ttu-id="299f9-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="299f9-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="299f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="299f9-102">SYNOPSIS</span></span>
<span data-ttu-id="299f9-103">Получает сведения о выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="299f9-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="299f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="299f9-104">SYNTAX</span></span>

### <span data-ttu-id="299f9-105">GetByNameAndId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="299f9-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299f9-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="299f9-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="299f9-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="299f9-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299f9-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="299f9-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="299f9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="299f9-109">DESCRIPTION</span></span>
<span data-ttu-id="299f9-110">Команда **Get-AzSynapsePipelineRun** возвращает сведения о запусках для указанного конвейера.</span><span class="sxs-lookup"><span data-stu-id="299f9-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="299f9-111">Если указан PipelineRunId, он отображает сведения для запуска с этим ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="299f9-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="299f9-112">Если PipelineRunId не указан, выводятся сведения обо всех запусках конвейеров, которые произошли между значениями RunStartedAfter и RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="299f9-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="299f9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="299f9-113">EXAMPLES</span></span>

### <span data-ttu-id="299f9-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="299f9-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="299f9-115">Эта команда получает подробные сведения о выполнении конвейера с ИДЕНТИФИКАТОРом "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="299f9-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="299f9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="299f9-116">PARAMETERS</span></span>

### <span data-ttu-id="299f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299f9-117">-DefaultProfile</span></span>
<span data-ttu-id="299f9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="299f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="299f9-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="299f9-119">-PipelineName</span></span>
<span data-ttu-id="299f9-120">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="299f9-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299f9-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="299f9-121">-PipelineRunId</span></span>
<span data-ttu-id="299f9-122">Идентификатор выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="299f9-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299f9-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="299f9-123">-RunStartedAfter</span></span>
<span data-ttu-id="299f9-124">Время, в течение или после которого событие "выполнение" было Обновлено в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="299f9-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299f9-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="299f9-125">-RunStartedBefore</span></span>
<span data-ttu-id="299f9-126">Время, в течение которого событие запуска было Обновлено в формате ISO 8601, или до него.</span><span class="sxs-lookup"><span data-stu-id="299f9-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299f9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="299f9-127">-WorkspaceName</span></span>
<span data-ttu-id="299f9-128">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="299f9-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299f9-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="299f9-129">-WorkspaceObject</span></span>
<span data-ttu-id="299f9-130">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="299f9-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="299f9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299f9-131">CommonParameters</span></span>
<span data-ttu-id="299f9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="299f9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299f9-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="299f9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299f9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="299f9-134">INPUTS</span></span>

### <span data-ttu-id="299f9-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="299f9-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="299f9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="299f9-136">OUTPUTS</span></span>

### <span data-ttu-id="299f9-137">Microsoft. Azure. Commands. Synapse. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="299f9-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="299f9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="299f9-138">NOTES</span></span>

## <span data-ttu-id="299f9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="299f9-139">RELATED LINKS</span></span>
