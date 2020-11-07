---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911920"
---
# <span data-ttu-id="a2c77-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="a2c77-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="a2c77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2c77-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c77-103">Создание нового задания</span><span class="sxs-lookup"><span data-stu-id="a2c77-103">Creates a new job</span></span>

## <span data-ttu-id="a2c77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2c77-104">SYNTAX</span></span>

### <span data-ttu-id="a2c77-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2c77-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c77-106">Run</span><span class="sxs-lookup"><span data-stu-id="a2c77-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c77-107">Повторяющегося</span><span class="sxs-lookup"><span data-stu-id="a2c77-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c77-108">Объект</span><span class="sxs-lookup"><span data-stu-id="a2c77-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c77-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a2c77-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c77-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a2c77-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c77-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2c77-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c77-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c77-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c77-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c77-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c77-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2c77-114">DESCRIPTION</span></span>
<span data-ttu-id="a2c77-115">Командлет New-AzSqlElasticJob создает новое задание.</span><span class="sxs-lookup"><span data-stu-id="a2c77-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="a2c77-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2c77-116">EXAMPLES</span></span>

### <span data-ttu-id="a2c77-117">Пример 1: создание нового задания</span><span class="sxs-lookup"><span data-stu-id="a2c77-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="a2c77-118">Создание нового задания</span><span class="sxs-lookup"><span data-stu-id="a2c77-118">Creates a new job</span></span>

## <span data-ttu-id="a2c77-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2c77-119">PARAMETERS</span></span>

### <span data-ttu-id="a2c77-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a2c77-120">-AgentName</span></span>
<span data-ttu-id="a2c77-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="a2c77-121">The agent name</span></span>

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

### <span data-ttu-id="a2c77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c77-122">-DefaultProfile</span></span>
<span data-ttu-id="a2c77-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c77-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c77-124">-Описание</span><span class="sxs-lookup"><span data-stu-id="a2c77-124">-Description</span></span>
<span data-ttu-id="a2c77-125">Описание задания</span><span class="sxs-lookup"><span data-stu-id="a2c77-125">The job description</span></span>

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

### <span data-ttu-id="a2c77-126">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="a2c77-126">-Enable</span></span>
<span data-ttu-id="a2c77-127">Пометка, показывающая, что клиент хочет включить это задание.</span><span class="sxs-lookup"><span data-stu-id="a2c77-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="a2c77-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a2c77-128">-EndTime</span></span>
<span data-ttu-id="a2c77-129">Время окончания расписания задания</span><span class="sxs-lookup"><span data-stu-id="a2c77-129">The job schedule end time</span></span>

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

### <span data-ttu-id="a2c77-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="a2c77-130">-IntervalCount</span></span>
<span data-ttu-id="a2c77-131">Количество повторяющихся интервалов расписания</span><span class="sxs-lookup"><span data-stu-id="a2c77-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="a2c77-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="a2c77-132">-IntervalType</span></span>
<span data-ttu-id="a2c77-133">Тип интервала повторения расписания — может быть: минуты, часы, дни, недели, месяцы</span><span class="sxs-lookup"><span data-stu-id="a2c77-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="a2c77-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2c77-134">-Name</span></span>
<span data-ttu-id="a2c77-135">Имя задания</span><span class="sxs-lookup"><span data-stu-id="a2c77-135">The job name</span></span>

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

### <span data-ttu-id="a2c77-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a2c77-136">-ParentObject</span></span>
<span data-ttu-id="a2c77-137">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="a2c77-137">The agent input object</span></span>

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

### <span data-ttu-id="a2c77-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c77-138">-ParentResourceId</span></span>
<span data-ttu-id="a2c77-139">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="a2c77-139">The agent resource id</span></span>

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

### <span data-ttu-id="a2c77-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c77-140">-ResourceGroupName</span></span>
<span data-ttu-id="a2c77-141">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2c77-141">The resource group name</span></span>

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

### <span data-ttu-id="a2c77-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="a2c77-142">-RunOnce</span></span>
<span data-ttu-id="a2c77-143">Флаг, указывающий, что задание будет выполняться один раз</span><span class="sxs-lookup"><span data-stu-id="a2c77-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="a2c77-144">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a2c77-144">-ServerName</span></span>
<span data-ttu-id="a2c77-145">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="a2c77-145">The server name</span></span>

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

### <span data-ttu-id="a2c77-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a2c77-146">-StartTime</span></span>
<span data-ttu-id="a2c77-147">Время начала расписания задания</span><span class="sxs-lookup"><span data-stu-id="a2c77-147">The job schedule start time</span></span>

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

### <span data-ttu-id="a2c77-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2c77-148">-Confirm</span></span>
<span data-ttu-id="a2c77-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2c77-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c77-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c77-150">-WhatIf</span></span>
<span data-ttu-id="a2c77-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2c77-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c77-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2c77-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c77-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c77-153">CommonParameters</span></span>
<span data-ttu-id="a2c77-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2c77-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c77-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2c77-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c77-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2c77-156">INPUTS</span></span>

### <span data-ttu-id="a2c77-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a2c77-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a2c77-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2c77-158">OUTPUTS</span></span>

### <span data-ttu-id="a2c77-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="a2c77-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a2c77-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2c77-160">NOTES</span></span>

## <span data-ttu-id="a2c77-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2c77-161">RELATED LINKS</span></span>
