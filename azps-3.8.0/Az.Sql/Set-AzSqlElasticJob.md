---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: a53a982e13b84bb401389e5edb5294ef1d094a49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912527"
---
# <span data-ttu-id="e458a-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="e458a-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="e458a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e458a-102">SYNOPSIS</span></span>
<span data-ttu-id="e458a-103">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="e458a-103">Updates a job</span></span>

## <span data-ttu-id="e458a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e458a-104">SYNTAX</span></span>

### <span data-ttu-id="e458a-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e458a-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e458a-106">Run</span><span class="sxs-lookup"><span data-stu-id="e458a-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e458a-107">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="e458a-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e458a-108">Объект</span><span class="sxs-lookup"><span data-stu-id="e458a-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e458a-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e458a-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e458a-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e458a-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e458a-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e458a-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e458a-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e458a-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e458a-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e458a-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e458a-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e458a-114">DESCRIPTION</span></span>
<span data-ttu-id="e458a-115">Командлет Set-AzSqlElasticJob обновляет задание.</span><span class="sxs-lookup"><span data-stu-id="e458a-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="e458a-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e458a-116">EXAMPLES</span></span>

### <span data-ttu-id="e458a-117">Пример 1: обновление задания для начала часа и повтор каждые 1 час.</span><span class="sxs-lookup"><span data-stu-id="e458a-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="e458a-118">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="e458a-118">Updates a job</span></span>

## <span data-ttu-id="e458a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e458a-119">PARAMETERS</span></span>

### <span data-ttu-id="e458a-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e458a-120">-AgentName</span></span>
<span data-ttu-id="e458a-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="e458a-121">The agent name</span></span>

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

### <span data-ttu-id="e458a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e458a-122">-DefaultProfile</span></span>
<span data-ttu-id="e458a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e458a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e458a-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="e458a-124">-Description</span></span>
<span data-ttu-id="e458a-125">Описание задания</span><span class="sxs-lookup"><span data-stu-id="e458a-125">The job description</span></span>

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

### <span data-ttu-id="e458a-126">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="e458a-126">-Enable</span></span>
<span data-ttu-id="e458a-127">Пометка, показывающая, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="e458a-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="e458a-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e458a-128">-EndTime</span></span>
<span data-ttu-id="e458a-129">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="e458a-129">The job schedule end time</span></span>

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

### <span data-ttu-id="e458a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e458a-130">-InputObject</span></span>
<span data-ttu-id="e458a-131">Входной объект задания</span><span class="sxs-lookup"><span data-stu-id="e458a-131">The job input object</span></span>

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

### <span data-ttu-id="e458a-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="e458a-132">-IntervalCount</span></span>
<span data-ttu-id="e458a-133">Количество повторяющихся интервалов расписания</span><span class="sxs-lookup"><span data-stu-id="e458a-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="e458a-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="e458a-134">-IntervalType</span></span>
<span data-ttu-id="e458a-135">Тип интервала повторения расписания — может быть: минуты, часы, дни, недели, месяцы</span><span class="sxs-lookup"><span data-stu-id="e458a-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="e458a-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e458a-136">-Name</span></span>
<span data-ttu-id="e458a-137">Имя задания</span><span class="sxs-lookup"><span data-stu-id="e458a-137">The job name</span></span>

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

### <span data-ttu-id="e458a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e458a-138">-ResourceGroupName</span></span>
<span data-ttu-id="e458a-139">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e458a-139">The resource group name</span></span>

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

### <span data-ttu-id="e458a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e458a-140">-ResourceId</span></span>
<span data-ttu-id="e458a-141">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="e458a-141">The job resource id</span></span>

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

### <span data-ttu-id="e458a-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="e458a-142">-RunOnce</span></span>
<span data-ttu-id="e458a-143">Флаг, указывающий, что задание будет выполняться один раз</span><span class="sxs-lookup"><span data-stu-id="e458a-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="e458a-144">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e458a-144">-ServerName</span></span>
<span data-ttu-id="e458a-145">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="e458a-145">The server name</span></span>

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

### <span data-ttu-id="e458a-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e458a-146">-StartTime</span></span>
<span data-ttu-id="e458a-147">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="e458a-147">The job schedule start time</span></span>

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

### <span data-ttu-id="e458a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e458a-148">-Confirm</span></span>
<span data-ttu-id="e458a-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e458a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e458a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e458a-150">-WhatIf</span></span>
<span data-ttu-id="e458a-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e458a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e458a-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e458a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e458a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e458a-153">CommonParameters</span></span>
<span data-ttu-id="e458a-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e458a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e458a-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e458a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e458a-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e458a-156">INPUTS</span></span>

### <span data-ttu-id="e458a-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="e458a-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="e458a-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e458a-158">OUTPUTS</span></span>

### <span data-ttu-id="e458a-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="e458a-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="e458a-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="e458a-160">NOTES</span></span>

## <span data-ttu-id="e458a-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e458a-161">RELATED LINKS</span></span>
