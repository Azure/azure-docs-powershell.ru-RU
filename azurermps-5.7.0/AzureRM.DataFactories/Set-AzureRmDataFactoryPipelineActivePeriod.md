---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 1c6290f21693f599925f34f950256005df8be670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559108"
---
# <span data-ttu-id="a9fe0-101">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a9fe0-101">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="a9fe0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fe0-103">Настраивает активный период для срезов данных.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-103">Configures the active period for data slices.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9fe0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9fe0-104">SYNTAX</span></span>

### <span data-ttu-id="a9fe0-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9fe0-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9fe0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a9fe0-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9fe0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9fe0-107">DESCRIPTION</span></span>
<span data-ttu-id="a9fe0-108">Командлет **Set-AzureRmDataFactoryPipelineActivePeriod** настраивает активный период для срезов данных, которые обрабатываются конвейером в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-108">The **Set-AzureRmDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="a9fe0-109">Если для изменения состояния срезов набора данных используется командлет Set-AzureRmDataFactorySliceStatus, убедитесь, что время начала и время окончания для среза находятся в активном периоде конвейера.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-109">If you use the Set-AzureRmDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>

<span data-ttu-id="a9fe0-110">После создания конвейера вы можете указать период, в котором будет выполняться обработка данных.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="a9fe0-111">Указание активного периода для конвейера определяет период времени, в течение которого срезы данных обрабатываются на основе свойств **доступности** , определенных для каждого набора данных фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="a9fe0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9fe0-112">EXAMPLES</span></span>

### <span data-ttu-id="a9fe0-113">Пример 1: Настройка активного периода</span><span class="sxs-lookup"><span data-stu-id="a9fe0-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="a9fe0-114">Эта команда настраивает активный период для срезов данных, которые обрабатываются с помощью процесса DPWikisample.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="a9fe0-115">Команда обеспечивает начальную и конечную точки для срезов данных в виде значений.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="a9fe0-116">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="a9fe0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9fe0-117">PARAMETERS</span></span>

### <span data-ttu-id="a9fe0-118">-Автоматическое разрешение</span><span class="sxs-lookup"><span data-stu-id="a9fe0-118">-AutoResolve</span></span>
<span data-ttu-id="a9fe0-119">Указывает на то, что этот командлет использует автоматическое разрешение.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="a9fe0-120">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-120">-DataFactory</span></span>
<span data-ttu-id="a9fe0-121">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a9fe0-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a9fe0-122">Этот командлет изменяет активный период для конвейера, относящегося к фабрике данных, которая указана в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe0-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a9fe0-123">-DataFactoryName</span></span>
<span data-ttu-id="a9fe0-124">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a9fe0-125">Этот командлет изменяет активный период для конвейера, относящегося к фабрике данных, которая указана в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9fe0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe0-126">-DefaultProfile</span></span>
<span data-ttu-id="a9fe0-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a9fe0-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9fe0-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="a9fe0-128">-EndDateTime</span></span>
<span data-ttu-id="a9fe0-129">Указывает конец периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a9fe0-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a9fe0-130">Обработка данных или срезы данных обрабатываются в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="a9fe0-131">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a9fe0-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="a9fe0-132">*EndDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="a9fe0-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="a9fe0-133">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское стандартное время)</span><span class="sxs-lookup"><span data-stu-id="a9fe0-133">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="a9fe0-134">Обозначение часового пояса по умолчанию — UTC.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-134">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe0-135">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="a9fe0-135">-ForceRecalculate</span></span>
<span data-ttu-id="a9fe0-136">Указывает на то, что этот командлет использует принудительное повторное вычисление.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-136">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="a9fe0-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a9fe0-137">-PipelineName</span></span>
<span data-ttu-id="a9fe0-138">Указывает имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="a9fe0-139">Этот командлет задает активный период для конвейера, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-139">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fe0-140">-ResourceGroupName</span></span>
<span data-ttu-id="a9fe0-141">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-141">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a9fe0-142">Этот командлет изменяет активный период для конвейера, принадлежащего к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-142">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9fe0-143">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a9fe0-143">-StartDateTime</span></span>
<span data-ttu-id="a9fe0-144">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a9fe0-144">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a9fe0-145">Обработка данных или срезы данных обрабатываются в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-145">Data processing occurs or data slices are processed within this period.</span></span>

<span data-ttu-id="a9fe0-146">*StartDateTime* должен быть указан в формате ISO8601.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-146">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe0-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9fe0-147">-Confirm</span></span>
<span data-ttu-id="a9fe0-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9fe0-149">-WhatIf</span></span>
<span data-ttu-id="a9fe0-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9fe0-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fe0-152">CommonParameters</span></span>
<span data-ttu-id="a9fe0-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fe0-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fe0-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fe0-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9fe0-155">INPUTS</span></span>

### <span data-ttu-id="a9fe0-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="a9fe0-156">None</span></span>
<span data-ttu-id="a9fe0-157">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a9fe0-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9fe0-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9fe0-158">OUTPUTS</span></span>

### <span data-ttu-id="a9fe0-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9fe0-159">System.Boolean</span></span>

## <span data-ttu-id="a9fe0-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9fe0-160">NOTES</span></span>
* <span data-ttu-id="a9fe0-161">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="a9fe0-161">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a9fe0-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9fe0-162">RELATED LINKS</span></span>

[<span data-ttu-id="a9fe0-163">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a9fe0-163">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a9fe0-164">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="a9fe0-164">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)


