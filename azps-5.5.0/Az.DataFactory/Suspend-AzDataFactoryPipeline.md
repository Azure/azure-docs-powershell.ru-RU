---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242752"
---
# <span data-ttu-id="aecf3-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="aecf3-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="aecf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aecf3-102">SYNOPSIS</span></span>
<span data-ttu-id="aecf3-103">Приостановка конвейера в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="aecf3-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="aecf3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aecf3-104">SYNTAX</span></span>

### <span data-ttu-id="aecf3-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aecf3-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aecf3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="aecf3-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aecf3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aecf3-107">DESCRIPTION</span></span>
<span data-ttu-id="aecf3-108">**Cmdlet Suspend-AzDataFactoryPipeline** приостанавливать конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="aecf3-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="aecf3-109">Вы можете возобновить работу конвейера с помощью Resume-AzDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="aecf3-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="aecf3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aecf3-110">EXAMPLES</span></span>

### <span data-ttu-id="aecf3-111">Пример 1. Приостановка конвейера</span><span class="sxs-lookup"><span data-stu-id="aecf3-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="aecf3-112">Эта команда приостанавливать канал DPWikiSample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="aecf3-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="aecf3-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="aecf3-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="aecf3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aecf3-114">PARAMETERS</span></span>

### <span data-ttu-id="aecf3-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="aecf3-115">-DataFactory</span></span>
<span data-ttu-id="aecf3-116">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="aecf3-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="aecf3-117">Этот cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="aecf3-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aecf3-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aecf3-118">-DataFactoryName</span></span>
<span data-ttu-id="aecf3-119">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="aecf3-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="aecf3-120">Этот cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="aecf3-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aecf3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecf3-121">-DefaultProfile</span></span>
<span data-ttu-id="aecf3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aecf3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aecf3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="aecf3-123">-Name</span></span>
<span data-ttu-id="aecf3-124">Указывает имя конвейера, который нужно приостановить.</span><span class="sxs-lookup"><span data-stu-id="aecf3-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aecf3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aecf3-125">-ResourceGroupName</span></span>
<span data-ttu-id="aecf3-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="aecf3-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="aecf3-127">Этот cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="aecf3-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aecf3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aecf3-128">-Confirm</span></span>
<span data-ttu-id="aecf3-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="aecf3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aecf3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aecf3-130">-WhatIf</span></span>
<span data-ttu-id="aecf3-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aecf3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aecf3-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aecf3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aecf3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecf3-133">CommonParameters</span></span>
<span data-ttu-id="aecf3-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aecf3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecf3-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aecf3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecf3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aecf3-136">INPUTS</span></span>

### <span data-ttu-id="aecf3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="aecf3-137">System.String</span></span>

### <span data-ttu-id="aecf3-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="aecf3-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="aecf3-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aecf3-139">OUTPUTS</span></span>

### <span data-ttu-id="aecf3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aecf3-140">System.Boolean</span></span>

## <span data-ttu-id="aecf3-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aecf3-141">NOTES</span></span>
* <span data-ttu-id="aecf3-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="aecf3-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aecf3-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aecf3-143">RELATED LINKS</span></span>

[<span data-ttu-id="aecf3-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="aecf3-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="aecf3-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="aecf3-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="aecf3-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="aecf3-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="aecf3-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="aecf3-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="aecf3-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="aecf3-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


