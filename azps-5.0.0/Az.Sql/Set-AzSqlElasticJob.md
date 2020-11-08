---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249591"
---
# <span data-ttu-id="cef27-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="cef27-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="cef27-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cef27-102">SYNOPSIS</span></span>
<span data-ttu-id="cef27-103">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="cef27-103">Updates a job</span></span>

## <span data-ttu-id="cef27-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cef27-104">SYNTAX</span></span>

### <span data-ttu-id="cef27-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cef27-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef27-106">Run</span><span class="sxs-lookup"><span data-stu-id="cef27-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef27-107">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="cef27-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef27-108">Объект</span><span class="sxs-lookup"><span data-stu-id="cef27-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cef27-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cef27-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef27-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cef27-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef27-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cef27-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef27-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cef27-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef27-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cef27-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef27-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef27-114">DESCRIPTION</span></span>
<span data-ttu-id="cef27-115">Командлет Set-AzSqlElasticJob обновляет задание.</span><span class="sxs-lookup"><span data-stu-id="cef27-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="cef27-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cef27-116">EXAMPLES</span></span>

### <span data-ttu-id="cef27-117">Пример 1: обновление задания, чтобы начать час, и Повтор выполняется каждый 1 час.</span><span class="sxs-lookup"><span data-stu-id="cef27-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="cef27-118">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="cef27-118">Updates a job</span></span>

### <span data-ttu-id="cef27-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cef27-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="cef27-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cef27-120">PARAMETERS</span></span>

### <span data-ttu-id="cef27-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="cef27-121">-AgentName</span></span>
<span data-ttu-id="cef27-122">Имя агента</span><span class="sxs-lookup"><span data-stu-id="cef27-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef27-123">-DefaultProfile</span></span>
<span data-ttu-id="cef27-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cef27-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef27-125">-Описание</span><span class="sxs-lookup"><span data-stu-id="cef27-125">-Description</span></span>
<span data-ttu-id="cef27-126">Описание задания</span><span class="sxs-lookup"><span data-stu-id="cef27-126">The job description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-127">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="cef27-127">-Enable</span></span>
<span data-ttu-id="cef27-128">Пометка, показывающая, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="cef27-128">The flag to indicate customer wants this job to be enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="cef27-129">-EndTime</span></span>
<span data-ttu-id="cef27-130">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="cef27-130">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cef27-131">-InputObject</span></span>
<span data-ttu-id="cef27-132">Входной объект задания</span><span class="sxs-lookup"><span data-stu-id="cef27-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="cef27-133">-IntervalCount</span></span>
<span data-ttu-id="cef27-134">Количество повторяющихся интервалов расписания</span><span class="sxs-lookup"><span data-stu-id="cef27-134">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="cef27-135">-IntervalType</span></span>
<span data-ttu-id="cef27-136">Тип интервала повторения расписания — может быть: минуты, часы, дни, недели, месяцы</span><span class="sxs-lookup"><span data-stu-id="cef27-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cef27-137">-Name</span></span>
<span data-ttu-id="cef27-138">Имя задания</span><span class="sxs-lookup"><span data-stu-id="cef27-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef27-139">-ResourceGroupName</span></span>
<span data-ttu-id="cef27-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cef27-140">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cef27-141">-ResourceId</span></span>
<span data-ttu-id="cef27-142">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="cef27-142">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="cef27-143">-RunOnce</span></span>
<span data-ttu-id="cef27-144">Флаг, указывающий, что задание будет выполняться один раз</span><span class="sxs-lookup"><span data-stu-id="cef27-144">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-145">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="cef27-145">-ServerName</span></span>
<span data-ttu-id="cef27-146">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="cef27-146">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cef27-147">-StartTime</span></span>
<span data-ttu-id="cef27-148">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="cef27-148">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef27-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef27-149">-Confirm</span></span>
<span data-ttu-id="cef27-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cef27-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef27-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef27-151">-WhatIf</span></span>
<span data-ttu-id="cef27-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cef27-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef27-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cef27-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef27-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef27-154">CommonParameters</span></span>
<span data-ttu-id="cef27-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cef27-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef27-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cef27-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef27-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cef27-157">INPUTS</span></span>

### <span data-ttu-id="cef27-158">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="cef27-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="cef27-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef27-159">OUTPUTS</span></span>

### <span data-ttu-id="cef27-160">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="cef27-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="cef27-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="cef27-161">NOTES</span></span>

## <span data-ttu-id="cef27-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef27-162">RELATED LINKS</span></span>
