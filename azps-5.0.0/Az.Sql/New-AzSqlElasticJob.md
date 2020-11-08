---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246685"
---
# <span data-ttu-id="80b57-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="80b57-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="80b57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80b57-102">SYNOPSIS</span></span>
<span data-ttu-id="80b57-103">Создание нового задания</span><span class="sxs-lookup"><span data-stu-id="80b57-103">Creates a new job</span></span>

## <span data-ttu-id="80b57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80b57-104">SYNTAX</span></span>

### <span data-ttu-id="80b57-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80b57-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80b57-106">Run</span><span class="sxs-lookup"><span data-stu-id="80b57-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b57-107">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="80b57-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80b57-108">Объект</span><span class="sxs-lookup"><span data-stu-id="80b57-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b57-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="80b57-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b57-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="80b57-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b57-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="80b57-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b57-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80b57-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80b57-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80b57-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80b57-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80b57-114">DESCRIPTION</span></span>
<span data-ttu-id="80b57-115">Командлет New-AzSqlElasticJob создает новое задание.</span><span class="sxs-lookup"><span data-stu-id="80b57-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="80b57-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80b57-116">EXAMPLES</span></span>

### <span data-ttu-id="80b57-117">Пример 1: создание нового задания</span><span class="sxs-lookup"><span data-stu-id="80b57-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="80b57-118">Создание нового задания</span><span class="sxs-lookup"><span data-stu-id="80b57-118">Creates a new job</span></span>

### <span data-ttu-id="80b57-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="80b57-119">Example 2</span></span>

<span data-ttu-id="80b57-120">Создает новое задание.</span><span class="sxs-lookup"><span data-stu-id="80b57-120">Creates a new job.</span></span> <span data-ttu-id="80b57-121">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="80b57-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="80b57-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80b57-122">PARAMETERS</span></span>

### <span data-ttu-id="80b57-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="80b57-123">-AgentName</span></span>
<span data-ttu-id="80b57-124">Имя агента</span><span class="sxs-lookup"><span data-stu-id="80b57-124">The agent name</span></span>

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

### <span data-ttu-id="80b57-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b57-125">-DefaultProfile</span></span>
<span data-ttu-id="80b57-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80b57-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80b57-127">-Описание</span><span class="sxs-lookup"><span data-stu-id="80b57-127">-Description</span></span>
<span data-ttu-id="80b57-128">Описание задания</span><span class="sxs-lookup"><span data-stu-id="80b57-128">The job description</span></span>

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

### <span data-ttu-id="80b57-129">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="80b57-129">-Enable</span></span>
<span data-ttu-id="80b57-130">Пометка, показывающая, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="80b57-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="80b57-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="80b57-131">-EndTime</span></span>
<span data-ttu-id="80b57-132">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="80b57-132">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b57-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="80b57-133">-IntervalCount</span></span>
<span data-ttu-id="80b57-134">Количество повторяющихся интервалов расписания</span><span class="sxs-lookup"><span data-stu-id="80b57-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="80b57-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="80b57-135">-IntervalType</span></span>
<span data-ttu-id="80b57-136">Тип интервала повторения расписания — может быть: минуты, часы, дни, недели, месяцы</span><span class="sxs-lookup"><span data-stu-id="80b57-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="80b57-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80b57-137">-Name</span></span>
<span data-ttu-id="80b57-138">Имя задания</span><span class="sxs-lookup"><span data-stu-id="80b57-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b57-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="80b57-139">-ParentObject</span></span>
<span data-ttu-id="80b57-140">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="80b57-140">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80b57-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80b57-141">-ParentResourceId</span></span>
<span data-ttu-id="80b57-142">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="80b57-142">The agent resource id</span></span>

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

### <span data-ttu-id="80b57-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b57-143">-ResourceGroupName</span></span>
<span data-ttu-id="80b57-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="80b57-144">The resource group name</span></span>

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

### <span data-ttu-id="80b57-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="80b57-145">-RunOnce</span></span>
<span data-ttu-id="80b57-146">Флаг, указывающий, что задание будет выполняться один раз</span><span class="sxs-lookup"><span data-stu-id="80b57-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="80b57-147">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="80b57-147">-ServerName</span></span>
<span data-ttu-id="80b57-148">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="80b57-148">The server name</span></span>

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

### <span data-ttu-id="80b57-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="80b57-149">-StartTime</span></span>
<span data-ttu-id="80b57-150">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="80b57-150">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b57-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80b57-151">-Confirm</span></span>
<span data-ttu-id="80b57-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80b57-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b57-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b57-153">-WhatIf</span></span>
<span data-ttu-id="80b57-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80b57-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b57-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80b57-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b57-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b57-156">CommonParameters</span></span>
<span data-ttu-id="80b57-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80b57-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b57-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80b57-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b57-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80b57-159">INPUTS</span></span>

### <span data-ttu-id="80b57-160">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="80b57-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="80b57-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80b57-161">OUTPUTS</span></span>

### <span data-ttu-id="80b57-162">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="80b57-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="80b57-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="80b57-163">NOTES</span></span>

## <span data-ttu-id="80b57-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80b57-164">RELATED LINKS</span></span>
