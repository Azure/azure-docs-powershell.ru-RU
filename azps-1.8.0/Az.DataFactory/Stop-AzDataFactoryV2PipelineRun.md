---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 3d58b378a64eca438340174d6e2085e26ca3868f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731109"
---
# <span data-ttu-id="653ae-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="653ae-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="653ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="653ae-102">SYNOPSIS</span></span>
<span data-ttu-id="653ae-103">Прекращение работы pieline в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="653ae-103">Stops a pieline run in a data factory.</span></span>

## <span data-ttu-id="653ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="653ae-104">SYNTAX</span></span>

### <span data-ttu-id="653ae-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="653ae-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="653ae-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="653ae-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="653ae-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="653ae-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="653ae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="653ae-108">DESCRIPTION</span></span>
<span data-ttu-id="653ae-109">Командлет **Stop-AzDataFactoryV2PipelineRun** останавливает выполнение конвейера в фабрике данных, указанной с помощью идентификатора запуска pieline.</span><span class="sxs-lookup"><span data-stu-id="653ae-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="653ae-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="653ae-110">EXAMPLES</span></span>

### <span data-ttu-id="653ae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="653ae-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="653ae-112">Эта команда останавливает процесс конвейера с ИД b9730a13-AA12-4926-a8b3-8e3a974ab0bd в фабрике WikiADF.</span><span class="sxs-lookup"><span data-stu-id="653ae-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="653ae-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="653ae-113">PARAMETERS</span></span>

### <span data-ttu-id="653ae-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="653ae-114">-DataFactory</span></span>
<span data-ttu-id="653ae-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="653ae-115">The data factory object.</span></span>

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

### <span data-ttu-id="653ae-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="653ae-116">-DataFactoryName</span></span>
<span data-ttu-id="653ae-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="653ae-117">The data factory name.</span></span>

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

### <span data-ttu-id="653ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="653ae-118">-DefaultProfile</span></span>
<span data-ttu-id="653ae-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="653ae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="653ae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="653ae-120">-InputObject</span></span>
<span data-ttu-id="653ae-121">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="653ae-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="653ae-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="653ae-122">-PassThru</span></span>
<span data-ttu-id="653ae-123">При успешном указании командлета записать истинную операцию в case.</span><span class="sxs-lookup"><span data-stu-id="653ae-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="653ae-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="653ae-124">-PipelineRunId</span></span>
<span data-ttu-id="653ae-125">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="653ae-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="653ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="653ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="653ae-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="653ae-127">The resource group name.</span></span>

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

### <span data-ttu-id="653ae-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="653ae-128">-Confirm</span></span>
<span data-ttu-id="653ae-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="653ae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="653ae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="653ae-130">-WhatIf</span></span>
<span data-ttu-id="653ae-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="653ae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="653ae-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="653ae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="653ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653ae-133">CommonParameters</span></span>
<span data-ttu-id="653ae-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="653ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653ae-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="653ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653ae-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="653ae-136">INPUTS</span></span>

### <span data-ttu-id="653ae-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="653ae-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="653ae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="653ae-138">System.String</span></span>

### <span data-ttu-id="653ae-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="653ae-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="653ae-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="653ae-140">OUTPUTS</span></span>

### <span data-ttu-id="653ae-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="653ae-141">System.Boolean</span></span>

## <span data-ttu-id="653ae-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="653ae-142">NOTES</span></span>

## <span data-ttu-id="653ae-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="653ae-143">RELATED LINKS</span></span>
