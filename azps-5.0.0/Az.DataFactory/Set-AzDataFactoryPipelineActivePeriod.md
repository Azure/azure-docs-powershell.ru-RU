---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 903e375c1272023d2d9b606325cae62103fbbc75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313790"
---
# <span data-ttu-id="d2e5d-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d2e5d-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="d2e5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e5d-103">Настраивает активный период для срезов данных.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="d2e5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2e5d-104">SYNTAX</span></span>

### <span data-ttu-id="d2e5d-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2e5d-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2e5d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d2e5d-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e5d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2e5d-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e5d-108">Командлет **Set-AzDataFactoryPipelineActivePeriod** настраивает активный период для срезов данных, которые обрабатываются конвейером в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="d2e5d-109">Если для изменения состояния срезов набора данных используется командлет Set-AzDataFactorySliceStatus, убедитесь, что время начала и время окончания для среза находятся в активном периоде конвейера.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="d2e5d-110">После создания конвейера вы можете указать период, в котором будет выполняться обработка данных.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="d2e5d-111">Указание активного периода для конвейера определяет период времени, в течение которого срезы данных обрабатываются на основе свойств **доступности** , определенных для каждого набора данных фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="d2e5d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2e5d-112">EXAMPLES</span></span>

### <span data-ttu-id="d2e5d-113">Пример 1: Настройка активного периода</span><span class="sxs-lookup"><span data-stu-id="d2e5d-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="d2e5d-114">Эта команда настраивает активный период для срезов данных, которые обрабатываются с помощью процесса DPWikisample.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="d2e5d-115">Команда обеспечивает начальную и конечную точки для срезов данных в виде значений.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="d2e5d-116">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="d2e5d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2e5d-117">PARAMETERS</span></span>

### <span data-ttu-id="d2e5d-118">-Автоматическое разрешение</span><span class="sxs-lookup"><span data-stu-id="d2e5d-118">-AutoResolve</span></span>
<span data-ttu-id="d2e5d-119">Указывает на то, что этот командлет использует автоматическое разрешение.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="d2e5d-120">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-120">-DataFactory</span></span>
<span data-ttu-id="d2e5d-121">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d2e5d-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d2e5d-122">Этот командлет изменяет активный период для конвейера, относящегося к фабрике данных, которая указана в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2e5d-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d2e5d-123">-DataFactoryName</span></span>
<span data-ttu-id="d2e5d-124">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d2e5d-125">Этот командлет изменяет активный период для конвейера, относящегося к фабрике данных, которая указана в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2e5d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e5d-126">-DefaultProfile</span></span>
<span data-ttu-id="d2e5d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2e5d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2e5d-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="d2e5d-128">-EndDateTime</span></span>
<span data-ttu-id="d2e5d-129">Указывает конец периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d2e5d-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d2e5d-130">Обработка данных или срезы данных обрабатываются в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="d2e5d-131">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d2e5d-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="d2e5d-132">*EndDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах: 2015-01-01Z 2015-01-01T00:00-1-01:00Z 1:00:01T00 z (UTC) 2015-0,01-: 00.00 – 8 – 00.000</span><span class="sxs-lookup"><span data-stu-id="d2e5d-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="d2e5d-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="d2e5d-133">-ForceRecalculate</span></span>
<span data-ttu-id="d2e5d-134">Указывает на то, что этот командлет использует принудительное повторное вычисление.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="d2e5d-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d2e5d-135">-PipelineName</span></span>
<span data-ttu-id="d2e5d-136">Указывает имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="d2e5d-137">Этот командлет задает активный период для конвейера, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2e5d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e5d-138">-ResourceGroupName</span></span>
<span data-ttu-id="d2e5d-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d2e5d-140">Этот командлет изменяет активный период для конвейера, принадлежащего к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2e5d-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d2e5d-141">-StartDateTime</span></span>
<span data-ttu-id="d2e5d-142">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d2e5d-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d2e5d-143">Обработка данных или срезы данных обрабатываются в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="d2e5d-144">*StartDateTime* должен быть указан в формате ISO8601.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="d2e5d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2e5d-145">-Confirm</span></span>
<span data-ttu-id="d2e5d-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e5d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e5d-147">-WhatIf</span></span>
<span data-ttu-id="d2e5d-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e5d-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e5d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e5d-150">CommonParameters</span></span>
<span data-ttu-id="d2e5d-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2e5d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e5d-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e5d-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e5d-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2e5d-153">INPUTS</span></span>

### <span data-ttu-id="d2e5d-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e5d-154">System.String</span></span>

### <span data-ttu-id="d2e5d-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d2e5d-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d2e5d-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2e5d-156">OUTPUTS</span></span>

### <span data-ttu-id="d2e5d-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2e5d-157">System.Boolean</span></span>

## <span data-ttu-id="d2e5d-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2e5d-158">NOTES</span></span>
* <span data-ttu-id="d2e5d-159">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="d2e5d-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d2e5d-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2e5d-160">RELATED LINKS</span></span>

[<span data-ttu-id="d2e5d-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d2e5d-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="d2e5d-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="d2e5d-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

