---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 903e375c1272023d2d9b606325cae62103fbbc75
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328974"
---
# <span data-ttu-id="ba096-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ba096-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="ba096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba096-102">SYNOPSIS</span></span>
<span data-ttu-id="ba096-103">Настраивает активный период для срезов данных.</span><span class="sxs-lookup"><span data-stu-id="ba096-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="ba096-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba096-104">SYNTAX</span></span>

### <span data-ttu-id="ba096-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba096-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba096-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ba096-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba096-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba096-107">DESCRIPTION</span></span>
<span data-ttu-id="ba096-108">**Cmdlet Set-AzDataFactoryPipelineActivePeriod** настраивает период активности для срезов данных, обрабатываемых конвейером в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ba096-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="ba096-109">Если вы используете Set-AzDataFactorySliceStatus для изменения состояния срезов для наборов данных, убедитесь, что время начала и время окончания для среза находятся в активном периоде конвейера.</span><span class="sxs-lookup"><span data-stu-id="ba096-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="ba096-110">После создания конвейера можно указать период обработки данных.</span><span class="sxs-lookup"><span data-stu-id="ba096-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="ba096-111">При указании активного периода для конвейера длительность обработки срезов  данных определяется на основе свойств доступности, определенных для каждого из наборов данных фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ba096-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="ba096-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba096-112">EXAMPLES</span></span>

### <span data-ttu-id="ba096-113">Пример 1. Настройка активного периода</span><span class="sxs-lookup"><span data-stu-id="ba096-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ba096-114">Эта команда настраивает период активности для срезов данных, которые обрабатывает конвейер под названием DPWikisample.</span><span class="sxs-lookup"><span data-stu-id="ba096-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="ba096-115">Команда предоставляет точки начала и окончания для срезов данных в качестве значений.</span><span class="sxs-lookup"><span data-stu-id="ba096-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="ba096-116">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="ba096-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="ba096-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba096-117">PARAMETERS</span></span>

### <span data-ttu-id="ba096-118">-AutoResolve</span><span class="sxs-lookup"><span data-stu-id="ba096-118">-AutoResolve</span></span>
<span data-ttu-id="ba096-119">Указывает на то, что этот cmdlet использует автоматическое разрешение.</span><span class="sxs-lookup"><span data-stu-id="ba096-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="ba096-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba096-120">-DataFactory</span></span>
<span data-ttu-id="ba096-121">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="ba096-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ba096-122">Этот cmdlet изменяет период активности для конвейера, который принадлежит фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ba096-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba096-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ba096-123">-DataFactoryName</span></span>
<span data-ttu-id="ba096-124">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ba096-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ba096-125">Этот cmdlet изменяет период активности для конвейера, который принадлежит фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ba096-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba096-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba096-126">-DefaultProfile</span></span>
<span data-ttu-id="ba096-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba096-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba096-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="ba096-128">-EndDateTime</span></span>
<span data-ttu-id="ba096-129">Окончание периода времени в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="ba096-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ba096-130">В течение этого периода происходит обработка данных или срезы данных.</span><span class="sxs-lookup"><span data-stu-id="ba096-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="ba096-131">Чтобы получить дополнительные сведения об **объектах даты и времени,** введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ba096-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ba096-132">В формате ISO8601 необходимо указать *endDateTime,* как в следующих примерах: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское время) По умолчанию часовой пояс имеет значение UTC.</span><span class="sxs-lookup"><span data-stu-id="ba096-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba096-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="ba096-133">-ForceRecalculate</span></span>
<span data-ttu-id="ba096-134">Указывает на то, что этот cmdlet использует принудительное пересчет.</span><span class="sxs-lookup"><span data-stu-id="ba096-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="ba096-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="ba096-135">-PipelineName</span></span>
<span data-ttu-id="ba096-136">Указывает имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="ba096-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="ba096-137">Этот cmdlet задает активный период для конвейера, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ba096-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba096-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba096-138">-ResourceGroupName</span></span>
<span data-ttu-id="ba096-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ba096-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ba096-140">Этот cmdlet изменяет активный период для конвейера, который принадлежит группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ba096-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba096-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="ba096-141">-StartDateTime</span></span>
<span data-ttu-id="ba096-142">Начало периода времени в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="ba096-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ba096-143">В течение этого периода происходит обработка данных или срезы данных.</span><span class="sxs-lookup"><span data-stu-id="ba096-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="ba096-144">*Формат StartDateTime* должен быть указан в формате ISO8601.</span><span class="sxs-lookup"><span data-stu-id="ba096-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba096-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba096-145">-Confirm</span></span>
<span data-ttu-id="ba096-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ba096-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba096-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba096-147">-WhatIf</span></span>
<span data-ttu-id="ba096-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba096-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba096-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba096-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba096-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba096-150">CommonParameters</span></span>
<span data-ttu-id="ba096-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba096-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba096-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba096-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba096-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba096-153">INPUTS</span></span>

### <span data-ttu-id="ba096-154">System.String</span><span class="sxs-lookup"><span data-stu-id="ba096-154">System.String</span></span>

### <span data-ttu-id="ba096-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ba096-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ba096-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba096-156">OUTPUTS</span></span>

### <span data-ttu-id="ba096-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba096-157">System.Boolean</span></span>

## <span data-ttu-id="ba096-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba096-158">NOTES</span></span>
* <span data-ttu-id="ba096-159">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="ba096-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ba096-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba096-160">RELATED LINKS</span></span>

[<span data-ttu-id="ba096-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ba096-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="ba096-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="ba096-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


