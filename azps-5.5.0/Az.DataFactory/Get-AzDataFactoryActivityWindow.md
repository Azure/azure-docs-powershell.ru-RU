---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222721"
---
# <span data-ttu-id="6590f-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="6590f-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="6590f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6590f-102">SYNOPSIS</span></span>
<span data-ttu-id="6590f-103">Получает сведения о окнах действий, связанных с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="6590f-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="6590f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6590f-104">SYNTAX</span></span>

### <span data-ttu-id="6590f-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6590f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6590f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6590f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6590f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6590f-107">DESCRIPTION</span></span>
<span data-ttu-id="6590f-108">С **помощью cmdlet get-AzDataFactoryActivityWindow** можно получить сведения о окнах действий, связанных с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="6590f-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="6590f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6590f-109">EXAMPLES</span></span>

### <span data-ttu-id="6590f-110">Пример 1. Получите окна действий, связанные с фабрикой данных</span><span class="sxs-lookup"><span data-stu-id="6590f-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="6590f-111">Эта команда получает сведения обо всех окнах действий, связанных с фабрикой данных WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6590f-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="6590f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6590f-112">PARAMETERS</span></span>

### <span data-ttu-id="6590f-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="6590f-113">-ActivityName</span></span>
<span data-ttu-id="6590f-114">Указывает имя действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="6590f-115">Этот cmdlet получает окна действий для действия, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6590f-116">-DataFactory</span></span>
<span data-ttu-id="6590f-117">Определяет объект **PSDataFactory,** возвращаемый cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6590f-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="6590f-118">Этот cmdlet получает окна действий, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6590f-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6590f-119">-DataFactoryName</span></span>
<span data-ttu-id="6590f-120">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6590f-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="6590f-121">Этот cmdlet получает окна действий, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6590f-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="6590f-122">-DatasetName</span></span>
<span data-ttu-id="6590f-123">Указывает имя наборов данных.</span><span class="sxs-lookup"><span data-stu-id="6590f-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="6590f-124">Этот cmdlet возвращает окна действий, которые относятся к набору данных, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6590f-125">-DefaultProfile</span></span>
<span data-ttu-id="6590f-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6590f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6590f-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="6590f-127">-Filter</span></span>
<span data-ttu-id="6590f-128">Окно действия, выраженное с помощью грамматики фильтра поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="6590f-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="6590f-129">Сведения о грамматике см. в синтаксис выражения OData для Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) (в MSDN).</span><span class="sxs-lookup"><span data-stu-id="6590f-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="6590f-130">Список окон действий фильтруется по строке поиска, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="6590f-131">-OrderBy</span></span>
<span data-ttu-id="6590f-132">Указывает, что ответ нужно заказать с помощью одного из параметров списка в окне действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="6590f-133">Это список свойств, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="6590f-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="6590f-134">Например: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="6590f-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="6590f-135">По умолчанию порядок — по возрастанию (ASC).</span><span class="sxs-lookup"><span data-stu-id="6590f-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="6590f-136">Укажите DESC, если вы хотите, чтобы список был упорядочен по убытию.</span><span class="sxs-lookup"><span data-stu-id="6590f-136">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="6590f-137">-PipelineName</span></span>
<span data-ttu-id="6590f-138">Указывает имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="6590f-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="6590f-139">Этот cmdlet получает окна действий, которые относятся к конвейеру, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6590f-140">-ResourceGroupName</span></span>
<span data-ttu-id="6590f-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6590f-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="6590f-142">Этот cmdlet получает окна действий, которые относятся к группе ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6590f-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="6590f-143">-RunEnd</span></span>
<span data-ttu-id="6590f-144">Время окончания окна действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="6590f-145">Этот cmdlet возвращает окна действий, время их запуска которых попадает в период между *запуском RunStart* *и RunEnd* Times.</span><span class="sxs-lookup"><span data-stu-id="6590f-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="6590f-146">-RunStart</span></span>
<span data-ttu-id="6590f-147">Время запуска окна действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="6590f-148">Этот cmdlet возвращает окна действий, время их запуска которых попадает в период между *запуском RunStart* *и RunEnd* Times.</span><span class="sxs-lookup"><span data-stu-id="6590f-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-149">-Top</span><span class="sxs-lookup"><span data-stu-id="6590f-149">-Top</span></span>
<span data-ttu-id="6590f-150">Указывает максимальное количество окон действий, которые возвращает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6590f-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="6590f-151">-WindowEnd</span></span>
<span data-ttu-id="6590f-152">Время окончания действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="6590f-153">Этот cmdlet возвращает окна действий, время которых попадает в период между *WindowStart* и *WindowEnd* Times.</span><span class="sxs-lookup"><span data-stu-id="6590f-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="6590f-154">-WindowStart</span></span>
<span data-ttu-id="6590f-155">Время начала действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="6590f-156">Этот cmdlet возвращает окна действий, время которых попадает в период между *WindowStart* и *WindowEnd* Times.</span><span class="sxs-lookup"><span data-stu-id="6590f-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="6590f-157">-WindowState</span></span>
<span data-ttu-id="6590f-158">Определяет состояние окна действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="6590f-159">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="6590f-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6590f-160">Нет</span><span class="sxs-lookup"><span data-stu-id="6590f-160">None</span></span>
- <span data-ttu-id="6590f-161">Ожидание</span><span class="sxs-lookup"><span data-stu-id="6590f-161">Waiting</span></span>
- <span data-ttu-id="6590f-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="6590f-162">InProgress</span></span>
- <span data-ttu-id="6590f-163">"Готово"</span><span class="sxs-lookup"><span data-stu-id="6590f-163">Ready</span></span>
- <span data-ttu-id="6590f-164">Сбой</span><span class="sxs-lookup"><span data-stu-id="6590f-164">Failed</span></span>
- <span data-ttu-id="6590f-165">Пропущенный этот cmdlet возвращает окна действий, которые находятся в состоянии, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="6590f-166">-WindowSubstate</span></span>
<span data-ttu-id="6590f-167">Указывает подстатет окна действия.</span><span class="sxs-lookup"><span data-stu-id="6590f-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="6590f-168">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="6590f-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6590f-169">Отменено</span><span class="sxs-lookup"><span data-stu-id="6590f-169">Canceled</span></span>
- <span data-ttu-id="6590f-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="6590f-170">timedOut</span></span>
- <span data-ttu-id="6590f-171">При проверке этого cmdlet получаются окна действий, указанные в подстате, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6590f-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6590f-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6590f-172">CommonParameters</span></span>
<span data-ttu-id="6590f-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6590f-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6590f-174">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6590f-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6590f-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6590f-175">INPUTS</span></span>

### <span data-ttu-id="6590f-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6590f-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="6590f-177">System.String</span><span class="sxs-lookup"><span data-stu-id="6590f-177">System.String</span></span>

### <span data-ttu-id="6590f-178">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6590f-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6590f-179">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6590f-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6590f-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6590f-180">OUTPUTS</span></span>

### <span data-ttu-id="6590f-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="6590f-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="6590f-182">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6590f-182">NOTES</span></span>

## <span data-ttu-id="6590f-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6590f-183">RELATED LINKS</span></span>

[<span data-ttu-id="6590f-184">Azure Data Factories Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6590f-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


