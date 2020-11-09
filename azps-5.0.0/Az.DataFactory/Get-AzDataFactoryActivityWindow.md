---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314120"
---
# <span data-ttu-id="20be0-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="20be0-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="20be0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20be0-102">SYNOPSIS</span></span>
<span data-ttu-id="20be0-103">Получает сведения о окнах активности, связанных с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="20be0-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="20be0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20be0-104">SYNTAX</span></span>

### <span data-ttu-id="20be0-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20be0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20be0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="20be0-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20be0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20be0-107">DESCRIPTION</span></span>
<span data-ttu-id="20be0-108">Командлет **Get-AzDataFactoryActivityWindow** получает сведения о окнах действий, связанных с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="20be0-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="20be0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20be0-109">EXAMPLES</span></span>

### <span data-ttu-id="20be0-110">Пример 1: получение окон действий, связанных с фабрикой данных</span><span class="sxs-lookup"><span data-stu-id="20be0-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="20be0-111">Эта команда получает сведения о всех окнах действий, связанных с фабрикой данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="20be0-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="20be0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20be0-112">PARAMETERS</span></span>

### <span data-ttu-id="20be0-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="20be0-113">-ActivityName</span></span>
<span data-ttu-id="20be0-114">Указывает имя действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="20be0-115">Этот командлет получает окна действия для действия, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="20be0-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-116">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="20be0-116">-DataFactory</span></span>
<span data-ttu-id="20be0-117">Указывает объект **PSDataFactory** , возвращаемый командлетом.</span><span class="sxs-lookup"><span data-stu-id="20be0-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="20be0-118">Этот командлет получает окна действия, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="20be0-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="20be0-119">-DataFactoryName</span></span>
<span data-ttu-id="20be0-120">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="20be0-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="20be0-121">Этот командлет получает окна действия, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="20be0-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="20be0-122">-DatasetName</span></span>
<span data-ttu-id="20be0-123">Указывает имя набора данных.</span><span class="sxs-lookup"><span data-stu-id="20be0-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="20be0-124">Этот командлет получает окна действия, которые относятся к набору данных, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="20be0-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20be0-125">-DefaultProfile</span></span>
<span data-ttu-id="20be0-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="20be0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20be0-127">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="20be0-127">-Filter</span></span>
<span data-ttu-id="20be0-128">Указывает окно действия, выраженное с помощью грамматики фильтра поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="20be0-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="20be0-129">Сведения о грамматике можно найти в статье синтаксис выражения OData для службы поиска Azure https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) в MSDN).</span><span class="sxs-lookup"><span data-stu-id="20be0-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="20be0-130">Список окон "действия" фильтруется по строке поиска, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="20be0-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="20be0-131">-OrderBy</span></span>
<span data-ttu-id="20be0-132">Определяет порядок ответа одним из параметров списка окна действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="20be0-133">Это список свойств, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="20be0-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="20be0-134">Например: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="20be0-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="20be0-135">По умолчанию порядок сортировки по возрастанию (ASC).</span><span class="sxs-lookup"><span data-stu-id="20be0-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="20be0-136">Укажите DESC, если вы хотите упорядочить список в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="20be0-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="20be0-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="20be0-137">-PipelineName</span></span>
<span data-ttu-id="20be0-138">Указывает имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="20be0-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="20be0-139">Этот командлет получает окна действия, которые относятся к конвейеру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="20be0-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20be0-140">-ResourceGroupName</span></span>
<span data-ttu-id="20be0-141">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20be0-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="20be0-142">Этот командлет получает окна действия, которые относятся к группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="20be0-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="20be0-143">-RunEnd</span></span>
<span data-ttu-id="20be0-144">Указывает время окончания работы окна действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="20be0-145">Этот командлет получает окна действия, время запуска которых выходит за *RunStart* и *RunEnd* время.</span><span class="sxs-lookup"><span data-stu-id="20be0-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="20be0-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="20be0-146">-RunStart</span></span>
<span data-ttu-id="20be0-147">Указывает время запуска окна действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="20be0-148">Этот командлет получает окна действия, время запуска которых выходит за *RunStart* и *RunEnd* время.</span><span class="sxs-lookup"><span data-stu-id="20be0-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="20be0-149">-Top</span><span class="sxs-lookup"><span data-stu-id="20be0-149">-Top</span></span>
<span data-ttu-id="20be0-150">Указывает максимальное количество окон действий, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="20be0-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="20be0-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="20be0-151">-WindowEnd</span></span>
<span data-ttu-id="20be0-152">Указывает время завершения периода действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="20be0-153">Этот командлет получает окна действия, которые находятся в интервале между *WindowStart* и *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="20be0-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="20be0-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="20be0-154">-WindowStart</span></span>
<span data-ttu-id="20be0-155">Указывает время запуска окна действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="20be0-156">Этот командлет получает окна действия, которые находятся в интервале между *WindowStart* и *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="20be0-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="20be0-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="20be0-157">-WindowState</span></span>
<span data-ttu-id="20be0-158">Задает состояние окна действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="20be0-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="20be0-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20be0-160">Ничего</span><span class="sxs-lookup"><span data-stu-id="20be0-160">None</span></span>
- <span data-ttu-id="20be0-161">Ожида</span><span class="sxs-lookup"><span data-stu-id="20be0-161">Waiting</span></span>
- <span data-ttu-id="20be0-162">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="20be0-162">InProgress</span></span>
- <span data-ttu-id="20be0-163">Начать</span><span class="sxs-lookup"><span data-stu-id="20be0-163">Ready</span></span>
- <span data-ttu-id="20be0-164">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="20be0-164">Failed</span></span>
- <span data-ttu-id="20be0-165">Пропущен этот командлет получает окна действия, которые находятся в состоянии, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="20be0-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="20be0-166">-WindowSubstate</span></span>
<span data-ttu-id="20be0-167">Задает подсостояние окна действия.</span><span class="sxs-lookup"><span data-stu-id="20be0-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="20be0-168">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="20be0-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20be0-169">Cancel</span><span class="sxs-lookup"><span data-stu-id="20be0-169">Canceled</span></span>
- <span data-ttu-id="20be0-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="20be0-170">timedOut</span></span>
- <span data-ttu-id="20be0-171">Проверка этого командлета получает окна действия, которые находятся в подсостоянии, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="20be0-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="20be0-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20be0-172">CommonParameters</span></span>
<span data-ttu-id="20be0-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20be0-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20be0-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20be0-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20be0-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20be0-175">INPUTS</span></span>

### <span data-ttu-id="20be0-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="20be0-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="20be0-177">System. String</span><span class="sxs-lookup"><span data-stu-id="20be0-177">System.String</span></span>

### <span data-ttu-id="20be0-178">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20be0-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="20be0-179">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20be0-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="20be0-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20be0-180">OUTPUTS</span></span>

### <span data-ttu-id="20be0-181">Microsoft. Azure. Commands. Factoring. Models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="20be0-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="20be0-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="20be0-182">NOTES</span></span>

## <span data-ttu-id="20be0-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20be0-183">RELATED LINKS</span></span>

[<span data-ttu-id="20be0-184">Командлеты фабрики данных Azure</span><span class="sxs-lookup"><span data-stu-id="20be0-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


