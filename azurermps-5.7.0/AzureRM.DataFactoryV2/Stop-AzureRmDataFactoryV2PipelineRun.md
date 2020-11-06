---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 7ddbc2809c58172eea2cd98ce048e0e49fbb14f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563631"
---
# <span data-ttu-id="a9172-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a9172-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="a9172-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9172-102">SYNOPSIS</span></span>
<span data-ttu-id="a9172-103">Прекращение работы pieline в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a9172-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9172-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9172-104">SYNTAX</span></span>

### <span data-ttu-id="a9172-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9172-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9172-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9172-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9172-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a9172-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9172-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9172-108">DESCRIPTION</span></span>
<span data-ttu-id="a9172-109">Командлет **Stop-AzureRmDataFactoryV2PipelineRun** останавливает выполнение конвейера в фабрике данных, указанной с помощью идентификатора запуска pieline.</span><span class="sxs-lookup"><span data-stu-id="a9172-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="a9172-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9172-110">EXAMPLES</span></span>

### <span data-ttu-id="a9172-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a9172-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="a9172-112">Эта команда останавливает процесс конвейера с ИД b9730a13-AA12-4926-a8b3-8e3a974ab0bd в фабрике WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a9172-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="a9172-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9172-113">PARAMETERS</span></span>

### <span data-ttu-id="a9172-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a9172-114">-DataFactory</span></span>
<span data-ttu-id="a9172-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a9172-115">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a9172-116">-DataFactoryName</span></span>
<span data-ttu-id="a9172-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a9172-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9172-118">-DefaultProfile</span></span>
<span data-ttu-id="a9172-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9172-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9172-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9172-120">-InputObject</span></span>
<span data-ttu-id="a9172-121">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="a9172-121">The Run ID of the pipeline.</span></span>

```yaml
Type: PSPipelineRun
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9172-122">-PassThru</span></span>
<span data-ttu-id="a9172-123">При успешном указании командлета записать истинную операцию в case.</span><span class="sxs-lookup"><span data-stu-id="a9172-123">If specified the cmdlet write true in case operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a9172-124">-PipelineRunId</span></span>
<span data-ttu-id="a9172-125">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="a9172-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9172-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9172-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a9172-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9172-128">-Confirm</span></span>
<span data-ttu-id="a9172-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a9172-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9172-130">-WhatIf</span></span>
<span data-ttu-id="a9172-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a9172-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9172-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9172-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9172-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9172-133">CommonParameters</span></span>
<span data-ttu-id="a9172-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9172-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9172-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9172-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9172-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9172-136">INPUTS</span></span>

### <span data-ttu-id="a9172-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="a9172-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="a9172-138">System. String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9172-138">System.String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a9172-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9172-139">OUTPUTS</span></span>

### <span data-ttu-id="a9172-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9172-140">System.Boolean</span></span>

## <span data-ttu-id="a9172-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9172-141">NOTES</span></span>

## <span data-ttu-id="a9172-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9172-142">RELATED LINKS</span></span>

