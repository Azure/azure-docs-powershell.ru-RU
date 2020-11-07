---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906322"
---
# <span data-ttu-id="6c96e-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="6c96e-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="6c96e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c96e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c96e-103">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-103">Updates a job</span></span>

## <span data-ttu-id="6c96e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c96e-104">SYNTAX</span></span>

### <span data-ttu-id="6c96e-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c96e-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c96e-106">Run</span><span class="sxs-lookup"><span data-stu-id="6c96e-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c96e-107">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="6c96e-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c96e-108">Объект</span><span class="sxs-lookup"><span data-stu-id="6c96e-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c96e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6c96e-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c96e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6c96e-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c96e-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6c96e-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c96e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6c96e-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c96e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6c96e-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c96e-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c96e-114">DESCRIPTION</span></span>
<span data-ttu-id="6c96e-115">Командлет Set-AzSqlElasticJob обновляет задание.</span><span class="sxs-lookup"><span data-stu-id="6c96e-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="6c96e-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c96e-116">EXAMPLES</span></span>

### <span data-ttu-id="6c96e-117">Пример 1: обновление задания для начала часа и повтор каждые 1 час.</span><span class="sxs-lookup"><span data-stu-id="6c96e-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="6c96e-118">Обновление задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-118">Updates a job</span></span>

## <span data-ttu-id="6c96e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c96e-119">PARAMETERS</span></span>

### <span data-ttu-id="6c96e-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6c96e-120">-AgentName</span></span>
<span data-ttu-id="6c96e-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="6c96e-121">The agent name</span></span>

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

### <span data-ttu-id="6c96e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c96e-122">-DefaultProfile</span></span>
<span data-ttu-id="6c96e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c96e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c96e-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="6c96e-124">-Description</span></span>
<span data-ttu-id="6c96e-125">Описание задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-125">The job description</span></span>

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

### <span data-ttu-id="6c96e-126">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="6c96e-126">-Enable</span></span>
<span data-ttu-id="6c96e-127">Пометка, показывающая, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="6c96e-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="6c96e-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6c96e-128">-EndTime</span></span>
<span data-ttu-id="6c96e-129">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-129">The job schedule end time</span></span>

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

### <span data-ttu-id="6c96e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c96e-130">-InputObject</span></span>
<span data-ttu-id="6c96e-131">Входной объект задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-131">The job input object</span></span>

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

### <span data-ttu-id="6c96e-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="6c96e-132">-IntervalCount</span></span>
<span data-ttu-id="6c96e-133">Количество повторяющихся интервалов расписания</span><span class="sxs-lookup"><span data-stu-id="6c96e-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="6c96e-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="6c96e-134">-IntervalType</span></span>
<span data-ttu-id="6c96e-135">Тип интервала повторения расписания — может быть: минуты, часы, дни, недели, месяцы</span><span class="sxs-lookup"><span data-stu-id="6c96e-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="6c96e-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c96e-136">-Name</span></span>
<span data-ttu-id="6c96e-137">Имя задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-137">The job name</span></span>

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

### <span data-ttu-id="6c96e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c96e-138">-ResourceGroupName</span></span>
<span data-ttu-id="6c96e-139">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6c96e-139">The resource group name</span></span>

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

### <span data-ttu-id="6c96e-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c96e-140">-ResourceId</span></span>
<span data-ttu-id="6c96e-141">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-141">The job resource id</span></span>

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

### <span data-ttu-id="6c96e-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="6c96e-142">-RunOnce</span></span>
<span data-ttu-id="6c96e-143">Флаг, указывающий, что задание будет выполняться один раз</span><span class="sxs-lookup"><span data-stu-id="6c96e-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="6c96e-144">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6c96e-144">-ServerName</span></span>
<span data-ttu-id="6c96e-145">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="6c96e-145">The server name</span></span>

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

### <span data-ttu-id="6c96e-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6c96e-146">-StartTime</span></span>
<span data-ttu-id="6c96e-147">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="6c96e-147">The job schedule start time</span></span>

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

### <span data-ttu-id="6c96e-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c96e-148">-Confirm</span></span>
<span data-ttu-id="6c96e-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6c96e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c96e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c96e-150">-WhatIf</span></span>
<span data-ttu-id="6c96e-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6c96e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c96e-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6c96e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c96e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c96e-153">CommonParameters</span></span>
<span data-ttu-id="6c96e-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c96e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c96e-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c96e-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c96e-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c96e-156">INPUTS</span></span>

### <span data-ttu-id="6c96e-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6c96e-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6c96e-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c96e-158">OUTPUTS</span></span>

### <span data-ttu-id="6c96e-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6c96e-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6c96e-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c96e-160">NOTES</span></span>

## <span data-ttu-id="6c96e-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c96e-161">RELATED LINKS</span></span>
